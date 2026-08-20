# Miniguia aprofundado — Fundamentos de Análise de Dados com Power BI, SQL e Python

## 1. Objetivo do guia

Este material apresenta uma visão integrada do trabalho inicial de análise de dados. Ele mostra como uma pergunta de negócio pode ser transformada em tarefas de extração, preparação, análise e comunicação, utilizando Power BI, SQL e Python como ferramentas complementares.

Os exemplos são didáticos. Eles não representam respostas executadas no NotebookLM nem substituem a validação nas fontes oficiais listadas no final.

## 2. Da pergunta à decisão

Uma análise útil começa com uma pergunta específica. “Quero analisar as entregas” é amplo demais. Uma versão melhor seria:

> Qual foi a evolução semanal da quantidade de entregas concluídas e do valor recebido, e quais categorias apresentaram maior participação no período?

Essa formulação permite identificar:

- Período de análise;
- Métricas necessárias;
- Dimensões de comparação;
- Filtros aplicáveis;
- Visualizações prováveis;
- Critérios para validar o resultado.

## 3. Etapas fundamentais

### 3.1 Definição do problema

Antes de acessar os dados, registre:

- Decisão que precisa ser apoiada;
- Público que utilizará o resultado;
- Métricas e dimensões;
- Período;
- Restrições conhecidas;
- Critério de sucesso da análise.

### 3.2 Obtenção dos dados

Os dados podem estar em bancos relacionais, planilhas, arquivos CSV, sistemas operacionais ou outras fontes. A extração deve coletar apenas os campos necessários e preservar a possibilidade de rastrear a origem.

### 3.3 Preparação

Perguntas de qualidade:

- Há identificadores duplicados?
- Existem datas inválidas?
- Valores numéricos foram importados como texto?
- Há categorias escritas de maneiras diferentes?
- Valores ausentes significam erro, ausência real ou “não se aplica”?
- A granularidade é uma linha por entrega ou uma linha por item?

### 3.4 Exploração

Nesta etapa, o analista observa o comportamento dos dados por meio de contagens, somas, médias, valores mínimos e máximos, distribuições e comparações entre grupos.

### 3.5 Modelagem e análise

Modelar significa organizar os dados e suas relações para responder às perguntas com consistência. O analista define cálculos, regras e contextos de comparação.

### 3.6 Visualização e comunicação

Uma visualização deve destacar a mensagem principal. O relatório final também deve explicar:

- O que foi encontrado;
- Como o resultado foi calculado;
- Que limitações existem;
- Qual decisão pode ser considerada;
- Que nova pergunta surgiu.

## 4. SQL para extração e agregação

### 4.1 Operações essenciais

| Operação | Finalidade |
|---|---|
| `SELECT` | Escolher colunas ou expressões retornadas |
| `FROM` | Informar a tabela de origem |
| `WHERE` | Filtrar registros antes da agregação |
| `JOIN` | Combinar tabelas relacionadas |
| `GROUP BY` | Agrupar registros para cálculos |
| `HAVING` | Filtrar grupos após a agregação |
| `ORDER BY` | Ordenar o resultado |

### 4.2 Exemplo progressivo

```sql
SELECT
    DATE_TRUNC('week', data_entrega) AS semana,
    COUNT(*) AS quantidade,
    SUM(valor_recebido) AS receita
FROM entregas
WHERE status = 'Concluída'
GROUP BY DATE_TRUNC('week', data_entrega)
ORDER BY semana;
```

Leitura do exemplo:

1. Seleciona a semana, a quantidade e a soma recebida;
2. Consulta a tabela `entregas`;
3. Mantém apenas entregas concluídas;
4. Agrupa os registros por semana;
5. Ordena cronologicamente.

### 4.3 Verificações antes de aceitar o resultado

- O filtro de status corresponde à regra de negócio?
- A data usada é a de criação ou conclusão?
- O valor pode aparecer repetido após um `JOIN`?
- Registros cancelados devem ser excluídos?
- O fuso horário interfere na data?

## 5. pandas para preparação e exploração

### 5.1 DataFrame

Um `DataFrame` representa dados tabulares com linhas e colunas identificadas. Ele permite aplicar operações de leitura, seleção, transformação, combinação, agregação e exportação.

### 5.2 Exemplo de preparação

```python
import pandas as pd

df = pd.read_csv("entregas.csv")

# Padroniza tipos
df["data_entrega"] = pd.to_datetime(df["data_entrega"], errors="coerce")
df["valor_recebido"] = pd.to_numeric(df["valor_recebido"], errors="coerce")

# Remove duplicidades pelo identificador
df = df.drop_duplicates(subset=["id_entrega"])

# Mantém registros válidos para a pergunta definida
df_validas = df.loc[
    (df["status"] == "Concluída")
    & df["data_entrega"].notna()
    & df["valor_recebido"].notna()
].copy()

# Cria uma variável de período
df_validas["semana"] = df_validas["data_entrega"].dt.to_period("W").astype(str)
```

### 5.3 Exemplo de agregação

```python
resumo_semanal = (
    df_validas.groupby("semana", as_index=False)
    .agg(
        quantidade=("id_entrega", "count"),
        receita=("valor_recebido", "sum")
    )
    .sort_values("semana")
)
```

### 5.4 Cuidados

- `errors="coerce"` transforma conversões inválidas em valores ausentes; eles precisam ser investigados;
- Remover duplicidades exige definir quais colunas identificam um registro único;
- Preencher valores ausentes com zero pode alterar o significado dos dados;
- Alterações devem ser registradas para que a análise seja reproduzível.

## 6. Power BI para modelagem e comunicação

### 6.1 Preparação com Power Query

Power Query pode conectar, limpar e transformar dados antes de carregá-los no modelo. As etapas aplicadas ficam registradas, o que facilita a atualização do processo.

### 6.2 Modelo

Um modelo bem organizado pode separar:

- **Tabela fato:** registros de entregas ou transações;
- **Dimensão de data:** calendário utilizado para análises temporais;
- **Dimensão de categoria:** descrição e agrupamento de tipos;
- **Medidas:** cálculos como quantidade, receita e média por entrega.

### 6.3 Visualizações sugeridas

| Pergunta | Visual possível | Motivo |
|---|---|---|
| Qual foi o total? | Cartão | Destaca um indicador único |
| Como evoluiu por semana? | Linha | Evidencia mudança ao longo do tempo |
| Qual categoria teve maior valor? | Barras | Facilita comparação entre categorias |
| Quais registros formam o resultado? | Tabela | Permite detalhamento |

### 6.4 Perguntas antes de publicar

- O título informa claramente o que está sendo mostrado?
- Período e filtros estão visíveis?
- Unidades monetárias e casas decimais estão consistentes?
- As cores têm significado ou são apenas decorativas?
- O gráfico permite interpretar a mensagem sem explicação longa?
- O indicador foi validado contra a fonte?

## 7. Integração das três ferramentas

Um fluxo possível:

1. Consultar no banco, com SQL, apenas dados do período e das colunas necessárias;
2. Exportar o resultado ou conectá-lo a um processo de tratamento;
3. Usar pandas para inspeções, testes e transformações reproduzíveis;
4. Carregar os dados preparados no Power BI;
5. Criar relacionamentos e medidas;
6. Construir visualizações alinhadas às perguntas de negócio;
7. Validar os totais entre banco, processamento e relatório;
8. Documentar regras, limitações e data de atualização.

Nem todo projeto precisa usar as três ferramentas. Em bases pequenas, parte do tratamento pode ocorrer no Power Query. Em ambientes com grande volume, pode ser melhor realizar filtros e agregações no banco. A decisão deve considerar contexto, desempenho, governança e manutenção.

## 8. Estudo de caso didático: entregas

### Cenário

Uma pessoa realiza entregas e deseja acompanhar produtividade e receita. A base possui:

- `id_entrega`;
- `data_entrega`;
- `bairro`;
- `categoria`;
- `status`;
- `valor_recebido`;
- `distancia_km`.

### Perguntas

1. Quantas entregas foram concluídas por semana?
2. Qual foi a receita total e a média por entrega?
3. Que bairros concentraram mais entregas?
4. A distância apresenta relação aparente com o valor recebido?
5. Em quais dias houve maior produtividade?

### Plano de solução

| Etapa | Ação |
|---|---|
| Regra de negócio | Definir quando uma entrega conta como concluída |
| Qualidade | Verificar duplicados, ausências, datas e valores inválidos |
| SQL | Extrair período, colunas e registros necessários |
| pandas | Explorar valores, tratar problemas e criar resumos |
| Power BI | Modelar datas, criar medidas e montar relatório |
| Validação | Comparar totais com registros de origem |
| Comunicação | Apresentar resultado, limitações e próximos passos |

## 9. Perguntas de autoavaliação

1. Por que uma análise deve começar por uma pergunta de negócio?
2. Qual é a diferença entre filtrar registros e agrupar registros?
3. Em que situação um `JOIN` pode duplicar valores?
4. O que um `DataFrame` representa?
5. Por que conversões inválidas não devem ser ignoradas?
6. Qual é a diferença entre dado bruto e dado preparado?
7. Que função o Power Query exerce no fluxo?
8. Quando um gráfico de linhas é mais adequado que um gráfico de barras?
9. Por que a granularidade precisa ser conhecida?
10. Como validar se um indicador do relatório está correto?

## 10. Plano de revisão em sete dias

| Dia | Atividade | Evidência de aprendizagem |
|---:|---|---|
| 1 | Ler o fluxo analítico e explicar com palavras próprias | Resumo de cinco linhas |
| 2 | Revisar `SELECT`, `WHERE`, `GROUP BY` e `ORDER BY` | Quatro consultas simples |
| 3 | Estudar `JOIN` e agregações | Uma consulta comentada |
| 4 | Ler e tratar um CSV com pandas | Notebook ou script curto |
| 5 | Criar um resumo agrupado no pandas | Tabela de resultado validada |
| 6 | Planejar uma página de relatório no Power BI | Esboço com métricas e visuais |
| 7 | Responder à autoavaliação e revisar erros | Registro das respostas corrigidas |

## 11. Glossário essencial

- **Agregação:** cálculo que resume um conjunto de registros;
- **Chave:** campo usado para identificar ou relacionar registros;
- **DataFrame:** estrutura tabular principal do pandas;
- **Dimensão:** tabela ou atributo usado para descrever e segmentar fatos;
- **ETL:** extração, transformação e carregamento;
- **Granularidade:** nível de detalhe de cada registro;
- **JOIN:** combinação de tabelas por uma condição de relacionamento;
- **Medida:** cálculo avaliado no contexto de uma análise;
- **Modelo semântico:** organização de dados, relacionamentos e cálculos para consumo analítico;
- **Power Query:** mecanismo de conexão e transformação de dados;
- **SQL:** linguagem de consulta e manipulação de dados relacionais;
- **Tabela fato:** estrutura que registra eventos ou transações;
- **Valor ausente:** dado que não está disponível em um campo;
- **Visualização:** representação gráfica de informações.

## 12. Fontes

1. [PostgreSQL — Tutorial oficial](https://www.postgresql.org/docs/current/tutorial.html)
2. [PostgreSQL — A linguagem SQL](https://www.postgresql.org/docs/current/tutorial-sql.html)
3. [pandas — Tutoriais introdutórios](https://pandas.pydata.org/docs/getting_started/intro_tutorials/)
4. [Microsoft Learn — Descubra a análise de dados](https://learn.microsoft.com/en-us/training/modules/data-analytics-microsoft/)
5. [Microsoft Learn — Preparar dados para análise com Power BI](https://learn.microsoft.com/en-us/training/paths/prepare-data-power-bi/)

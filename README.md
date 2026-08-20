# Caderno Temático com NotebookLM: Fundamentos de Análise de Dados com Power BI, SQL e Python

![Status](https://img.shields.io/badge/status-conclu%C3%ADdo-brightgreen)
![DIO](https://img.shields.io/badge/projeto-DIO-6C2BD9)
![NotebookLM](https://img.shields.io/badge/IA-NotebookLM-4285F4)
![Área](https://img.shields.io/badge/área-Análise%20de%20Dados-0A66C2)

> Projeto desenvolvido para o desafio da DIO sobre aprendizagem ativa com Inteligência Artificial, curadoria de fontes e organização do conhecimento no NotebookLM.

### Materiais do repositório

- [Guia de execução passo a passo](GUIA_DE_EXECUCAO.md);
- [Prompt mestre para comparar outra IA](PROMPT_MESTRE_OUTRA_IA.md);
- [Modelo de registro de experimentos](registros/MODELO_REGISTRO_PROMPT.md);
- [Miniguia aprofundado](docs/MINIGUIA_APROFUNDADO.md).

## Sumário

1. [Contexto](#1-contexto)
2. [Objetivos](#2-objetivos)
3. [Curadoria de fontes](#3-curadoria-de-fontes)
4. [Metodologia](#4-metodologia)
5. [Engenharia de prompts](#5-engenharia-de-prompts)
6. [Cicatrizes e troubleshooting](#6-cicatrizes-e-troubleshooting)
7. [Miniguia de estudo](#7-miniguia-de-estudo)
8. [Glossário](#8-glossário)
9. [Prompts reutilizáveis](#9-prompts-reutilizáveis)
10. [Checklist do projeto](#10-checklist-do-projeto)
11. [Conclusão](#11-conclusão)

## 1. Contexto

O tema escolhido para este caderno temático foi **Fundamentos de Análise de Dados com Power BI, SQL e Python**. A escolha está relacionada ao meu objetivo de desenvolver competências para atuar como analista de dados, compreendendo não apenas ferramentas isoladas, mas o fluxo completo que transforma dados brutos em informações úteis para a tomada de decisão.

O projeto utiliza o NotebookLM como ambiente de aprendizagem ativa. Em vez de solicitar respostas genéricas à Inteligência Artificial, foram selecionadas fontes oficiais, criadas perguntas estratégicas e planejadas revisões progressivas das respostas. O foco é aprender a consultar, comparar, resumir e validar informações com base em referências rastreáveis.

### Pergunta norteadora

> Como Power BI, SQL e Python podem ser utilizados de forma integrada nas etapas de coleta, preparação, análise e comunicação de dados?

### Escopo do caderno

- Papel do analista de dados;
- Etapas de um processo de análise;
- Fundamentos de consultas SQL;
- Manipulação de dados tabulares com pandas;
- Preparação, modelagem e visualização no Power BI;
- Boas práticas para transformar resultados técnicos em decisões de negócio.

## 2. Objetivos

### Objetivo geral

Construir um material de estudo confiável e reutilizável sobre os fundamentos da análise de dados, utilizando o NotebookLM para organizar fontes, formular perguntas, comparar conceitos e consolidar o aprendizado.

### Objetivos específicos

- Compreender as principais etapas de um projeto de análise de dados;
- Identificar o papel de Power BI, SQL e Python em um fluxo analítico;
- Aprender conceitos básicos de consulta, limpeza, transformação, modelagem e visualização;
- Praticar engenharia de prompts com perguntas progressivamente mais específicas;
- Verificar se as respostas da IA são sustentadas pelas fontes selecionadas;
- Registrar dificuldades, ajustes e aprendizados obtidos durante os testes;
- Produzir um miniguia que possa ser utilizado em revisões futuras;
- Demonstrar organização, pensamento crítico e documentação técnica no GitHub.

## 3. Curadoria de fontes

Foram priorizadas fontes oficiais, abertas, técnicas e adequadas ao nível iniciante/intermediário. Antes de adicioná-las ao NotebookLM, é importante abrir cada link e confirmar se a página está acessível.

| Nº | Fonte | Instituição | Formato | Motivo da escolha |
|---:|---|---|---|---|
| 1 | [PostgreSQL — Tutorial oficial](https://www.postgresql.org/docs/current/tutorial.html) | PostgreSQL Global Development Group | Texto web | Apresenta bancos relacionais e SQL com exemplos práticos. |
| 2 | [PostgreSQL — A linguagem SQL](https://www.postgresql.org/docs/current/tutorial-sql.html) | PostgreSQL Global Development Group | Texto web | Cobre criação e consulta de tabelas, filtros, junções e agregações. |
| 3 | [pandas — Tutoriais introdutórios](https://pandas.pydata.org/docs/getting_started/intro_tutorials/) | pandas / NumFOCUS | Texto web | Ensina leitura, seleção, transformação, combinação e resumo de dados tabulares. |
| 4 | [Microsoft Learn — Descubra a análise de dados](https://learn.microsoft.com/en-us/training/modules/data-analytics-microsoft/) | Microsoft | Texto web | Explica funções e responsabilidades relacionadas à análise de dados. |
| 5 | [Microsoft Learn — Preparar dados para análise com Power BI](https://learn.microsoft.com/en-us/training/paths/prepare-data-power-bi/) | Microsoft | Texto web | Aborda extração, perfil, limpeza e carregamento de dados no Power BI. |

**Data de acesso:** 19 de agosto de 2026.

### Critérios utilizados na curadoria

1. **Autoridade:** preferência por documentação oficial das tecnologias estudadas;
2. **Acesso aberto:** materiais disponíveis sem pagamento;
3. **Relevância:** relação direta com a pergunta norteadora;
4. **Complementaridade:** cada fonte cobre uma parte diferente do fluxo analítico;
5. **Aplicabilidade:** presença de conceitos e exemplos que podem ser usados nos estudos.

### Como adicionar as fontes ao NotebookLM

1. Criar um novo notebook com o nome `Caderno Temático — Fundamentos de Análise de Dados com Power BI, SQL e Python`;
2. Selecionar a opção de adicionar fontes;
3. Inserir cada endereço eletrônico individualmente;
4. Confirmar se o NotebookLM conseguiu processar cada fonte;
5. Renomear as fontes com títulos curtos e identificáveis, se necessário;
6. Não prosseguir com uma fonte que apresente erro de leitura: substituir por uma página equivalente da mesma documentação.

## 4. Metodologia

O estudo foi organizado como um processo iterativo:

1. **Definição do tema e da pergunta norteadora;**
2. **Seleção de fontes confiáveis;**
3. **Importação e validação das fontes no NotebookLM;**
4. **Aplicação de prompts exploratórios para mapear o tema;**
5. **Aplicação de prompts analíticos para comparar conceitos e ferramentas;**
6. **Refinamento dos prompts após respostas vagas ou incompletas;**
7. **Conferência das referências apresentadas pelo NotebookLM;**
8. **Consolidação do aprendizado em resumo, glossário e prompts de revisão.**

### Regra de validação

Uma resposta só deve ser incorporada ao miniguia quando:

- estiver apoiada por uma ou mais fontes do notebook;
- responder diretamente ao que foi perguntado;
- diferenciar claramente conceitos que podem ser confundidos;
- não apresentar exemplos como se fossem fatos documentados;
- puder ser reescrita com compreensão própria, sem simples cópia.

## 5. Engenharia de prompts

Os prompts abaixo devem ser executados no NotebookLM na ordem indicada. Após cada teste, a resposta, as referências e a avaliação devem ser registradas na tabela de experimentos.

### Etapa 1 — Exploração do assunto

**Prompt 1 — Visão geral**

```text
Com base exclusivamente nas fontes deste notebook, explique o que é análise de dados e quais são suas principais etapas. Organize a resposta em uma sequência lógica, use linguagem adequada para um estudante iniciante e cite as fontes utilizadas em cada etapa. Não acrescente informações que não estejam sustentadas pelas fontes.
```

**Prompt 2 — Papel das ferramentas**

```text
Com base nas fontes, explique qual é o papel de SQL, pandas e Power BI em um projeto de análise de dados. Para cada ferramenta, informe: finalidade principal, etapa do fluxo em que pode ser utilizada, exemplo de tarefa e limitações do que pode ser concluído apenas a partir das fontes disponíveis. Termine mostrando como as três ferramentas podem funcionar de forma integrada.
```

### Etapa 2 — Aprofundamento e comparação

**Prompt 3 — Fluxo integrado**

```text
Crie um fluxo de trabalho hipotético para analisar dados de vendas. Use SQL para extração e agregação, pandas para inspeção e tratamento dos dados e Power BI para modelagem e visualização. Separe claramente: problema de negócio, dados necessários, etapas técnicas, verificações de qualidade e resultado esperado. Identifique o que é fundamentado pelas fontes e o que é apenas um exemplo didático.
```

**Prompt 4 — Conceitos que podem ser confundidos**

```text
Compare os seguintes pares de conceitos com base nas fontes: tabela e DataFrame; filtro SQL e seleção no pandas; limpeza e transformação; relatório e dashboard. Use uma tabela com definição, diferença principal, exemplo e fonte de apoio. Se algum conceito não estiver suficientemente coberto, informe a limitação em vez de completar com conhecimento externo.
```

### Etapa 3 — Aprendizagem ativa

**Prompt 5 — Perguntas de revisão**

```text
Crie 10 perguntas de revisão em ordem crescente de dificuldade sobre SQL, pandas, Power BI e fluxo de análise de dados. Não mostre as respostas imediatamente. Depois que eu responder, corrija cada item com base nas fontes, explique os erros e indique qual trecho ou fonte deve ser revisado.
```

**Prompt 6 — Estudo de caso**

```text
Atue como orientador de estudos. Apresente um pequeno estudo de caso de análise de dados de entregas, contendo uma pergunta de negócio, uma tabela fictícia descrita por suas colunas e cinco tarefas progressivas. As tarefas devem exigir raciocínio sobre SQL, pandas e Power BI, mas não devem depender de conceitos ausentes nas fontes. Não forneça a solução até que eu tente responder.
```

### Etapa 4 — Consolidação

**Prompt 7 — Miniguia final**

```text
Com base exclusivamente nas fontes e nos conceitos discutidos nesta conversa, produza um miniguia de estudo em português do Brasil. Inclua: resumo estruturado, fluxo analítico, papel de SQL, pandas e Power BI, boas práticas, erros comuns, glossário e cinco perguntas de autoavaliação. Insira referências junto às afirmações relevantes e sinalize qualquer ponto com evidência insuficiente.
```

### Registro dos experimentos

> Preencha esta tabela depois de executar os prompts. Não apresente como realizado um teste que ainda não aconteceu.

| Teste | Prompt usado | Síntese da resposta | Referências indicadas | Avaliação | Ajuste necessário |
|---:|---|---|---|---|---|
| 1 | Visão geral | Definiu análise de dados e organizou o processo em seis etapas: definição do problema, obtenção, preparação, exploração, modelagem e análise, visualização e comunicação. | `README.md` e `MINIGUIA_APROFUNDADO.md` | Resposta clara, lógica e adequada para iniciantes. | Como melhoria futura, comparar o resultado com uma rodada baseada diretamente nas fontes oficiais. |
| 2 | Papel das ferramentas | Explicou finalidade, etapa de uso, exemplo e limitações de SQL, pandas e Power BI, encerrando com um fluxo integrado. | `README.md` e `MINIGUIA_APROFUNDADO.md` | Comparação completa e bem organizada. | Como melhoria futura, validar as definições diretamente nas documentações oficiais. |
| 3 | Fluxo integrado | Criou um caso hipotético de vendas com pergunta de negócio, dados necessários, SQL, pandas, Power BI, verificações de qualidade e resultado esperado. | `README.md` e `MINIGUIA_APROFUNDADO.md` | Atendeu ao formato pedido e diferenciou fundamentos de exemplos didáticos. | Conferir, em uma evolução posterior, o apoio direto das fontes primárias. |
| 4 | Conceitos comparados | Comparou tabela e DataFrame, filtro SQL e seleção no pandas, limpeza e transformação, relatório e dashboard. | `README.md` e `MINIGUIA_APROFUNDADO.md` | A tabela facilitou a comparação e a resposta reconheceu limitações das fontes. | Ampliar futuramente a cobertura com definições oficiais mais específicas. |
| 5 | Perguntas de revisão | Gerou dez perguntas em três níveis sobre fluxo analítico, SQL, pandas, Power BI, qualidade e tomada de decisão. | Não foram exibidas citações na resposta gravada. | O teste foi concluído conforme o prompt: a IA gerou as questões e aguardou as respostas do estudante. | A correção interativa pode ser realizada como exercício complementar. |
| 6 | Estudo de caso | Propôs um estudo de caso de entregas urbanas com tabela fictícia e cinco tarefas progressivas envolvendo SQL, pandas e Power BI. | `README.md` e `MINIGUIA_APROFUNDADO.md` | O teste foi concluído e respeitou a orientação de não apresentar a solução antes da tentativa do estudante. | A resolução das tarefas pode ser adicionada posteriormente como aprofundamento. |
| 7 | Miniguia final | Consolidou resumo, fluxo analítico, ferramentas, boas práticas, erros comuns, glossário, integração e autoavaliação. | `README.md` e `MINIGUIA_APROFUNDADO.md` | Síntese básica registrada como evidência da consolidação produzida no NotebookLM. | Manter a circularidade identificada como limitação metodológica e oportunidade de evolução. |

### Análise detalhada da primeira rodada

> Esta rodada registra a execução dos sete prompts no NotebookLM. Os vídeos mostraram que o painel continha materiais produzidos para o próprio projeto. Por transparência, a circularidade das referências foi mantida como limitação metodológica e oportunidade de melhoria futura.

#### Teste 1 — Visão geral

O NotebookLM definiu análise de dados como um processo para examinar informações, responder perguntas, identificar padrões e apoiar decisões. A resposta foi organizada em:

1. Definição do problema;
2. Obtenção dos dados;
3. Preparação dos dados;
4. Exploração;
5. Modelagem e análise;
6. Visualização e comunicação.

**Avaliação:** a explicação foi clara, progressiva e apropriada para iniciantes. Os marcadores de citação apontaram principalmente para `README.md` e `MINIGUIA_APROFUNDADO.md`. Uma comparação futura com as fontes oficiais poderá fortalecer a validação.

#### Teste 2 — Papel das ferramentas

A resposta atribuiu os seguintes papéis às ferramentas:

- **SQL:** extração, filtragem, combinação e agregação de dados relacionais;
- **pandas:** inspeção, limpeza, transformação e exploração de dados tabulares;
- **Power BI:** modelagem, criação de medidas, visualização e comunicação dos resultados.

Também foi apresentado um fluxo em que SQL seleciona os dados necessários, pandas realiza tratamentos e testes e Power BI organiza o modelo e o relatório.

**Avaliação:** o formato solicitado foi atendido, incluindo finalidade, etapa, exemplo e limitação. A principal restrição foi a ausência de fontes primárias no painel do notebook.

#### Teste 3 — Fluxo integrado

O NotebookLM criou um cenário de análise de vendas com:

- Pergunta de negócio sobre evolução mensal da receita e desempenho por categoria;
- Tabelas de vendas, produtos e categorias;
- Extração e agregação com SQL;
- Preparação e exploração com pandas;
- Modelo e visualizações no Power BI;
- Conferências de filtros, datas, duplicidades, totais e medidas;
- Dashboard como resultado esperado.

A resposta separou os papéis fundamentados das ferramentas dos elementos fictícios do exemplo, como nomes de tabelas, métricas e gráficos.

**Avaliação:** foi uma resposta aplicável e bem dividida. A rastreabilidade ainda deve ser refeita com as documentações oficiais.

#### Teste 4 — Conceitos que podem ser confundidos

A resposta comparou os quatro pares em uma tabela com definição, diferença, exemplo e apoio:

- Tabela e DataFrame;
- Filtro SQL e seleção no pandas;
- Limpeza e transformação;
- Relatório e dashboard.

**Avaliação:** a organização visual ajudou a distinguir os conceitos. O próprio NotebookLM reconheceu que as fontes disponíveis eram suficientes para uma visão integrada, mas não detalhavam profundamente todos os termos. Esse reconhecimento foi preservado como uma limitação real da primeira rodada.

#### Teste 5 — Perguntas de revisão

Foram geradas dez questões em dificuldade crescente. Entre os assuntos estavam:

- Primeiro passo de uma análise;
- Conceito de DataFrame;
- Função da cláusula `WHERE`;
- Diferença entre tabela fato e dimensão;
- Qualidade e preparação dos dados;
- Diferença entre `WHERE` e `HAVING`;
- Risco de preencher valores ausentes com zero;
- Integração de SQL, pandas e Power BI;
- Definição de regras antes da construção do dashboard;
- Investigação de divergências entre banco de dados e Power BI.

**Avaliação:** as perguntas apresentaram boa progressão. Como o prompt pede que a IA aguarde as respostas do estudante, a gravação comprova que o comportamento esperado foi atendido. A etapa de correção é um exercício complementar e não impede a conclusão deste projeto.

#### Teste 6 — Estudo de caso

O caso proposto tratou da otimização de entregas urbanas. A base fictícia incluía identificador, data, categoria, status, valor recebido e distância. As cinco tarefas abordaram:

1. Extração estruturada com SQL;
2. Preparação e exploração com pandas;
3. Cálculos e comparação de categorias;
4. Modelagem no Power BI;
5. Comunicação por meio de um dashboard.

**Avaliação:** o NotebookLM cumpriu corretamente a ordem de não fornecer a solução antes da tentativa do estudante. A resolução e a avaliação das tarefas poderão ser acrescentadas em uma evolução futura do caderno.

#### Teste 7 — Miniguia final

O resultado consolidado apresentou:

- Resumo estruturado do processo de análise;
- Fluxo da pergunta de negócio até a comunicação;
- Papel de SQL, pandas e Power BI;
- Boas práticas e erros comuns;
- Glossário essencial;
- Perguntas de autoavaliação;
- Integração das ferramentas;
- Observação sobre pontos com evidência insuficiente.

**Avaliação:** a estrutura básica ficou útil para revisão e foi registrada como evidência do Prompt 7. Como uma das fontes citadas já era um miniguia produzido anteriormente, houve circularidade entre fonte e resultado. Essa condição foi documentada com transparência e poderá ser corrigida em uma versão futura.

## 6. Cicatrizes e troubleshooting

Nesta seção devem ser documentadas as dificuldades reais encontradas. O objetivo não é esconder respostas ruins, mas demonstrar como os prompts foram melhorados.

### Cicatrizes reais observadas na primeira rodada

#### 1. Circularidade das fontes

**Problema observado:** o painel do NotebookLM continha os arquivos `GUIA_DE_EXECUCAO.md`, `MINIGUIA_APROFUNDADO.md`, `MODELO_REGISTRO_PROMPT.md`, `PROMPT_MESTRE_OUTRA_IA.md` e `README.md`. As citações abertas nos vídeos apontaram principalmente para `README.md` e `MINIGUIA_APROFUNDADO.md`.

**Por que isso é uma dificuldade:** esses arquivos já apresentavam resumos, definições e exemplos produzidos para o projeto. Assim, o NotebookLM respondeu com base em materiais que continham previamente parte das respostas, criando referência circular e não validando diretamente as cinco fontes oficiais declaradas na curadoria.

**Melhoria futura sugerida:** criar uma nova rodada no NotebookLM utilizando diretamente os cinco links oficiais da seção de curadoria. No painel de fontes deverão aparecer as páginas do PostgreSQL, pandas e Microsoft Learn, e não apenas os documentos do repositório.

**Critério de validação:** abrir as citações da nova resposta e confirmar que os títulos e trechos pertencem às documentações oficiais.

#### 2. Atividade de revisão incompleta

**Problema observado:** o Prompt 5 gerou as dez perguntas e aguardou as respostas, conforme solicitado, mas a etapa de correção ainda não foi executada. Além disso, não apareceram marcadores de citação na lista de perguntas gravada.

**Melhoria opcional:** responder às questões e enviar o seguinte prompt de continuidade:

```text
Agora corrija minhas respostas uma por uma. Para cada item, informe se acertei, explique o ponto que precisa ser corrigido e cite a fonte oficial e o trecho que sustentam o feedback. Se as fontes não forem suficientes, sinalize a limitação.
```

**Critério de validação:** receber feedback individualizado e referências verificáveis para cada correção.

#### 3. Estudo de caso aguardando tentativa

**Problema observado:** o Prompt 6 respeitou a regra de não entregar as soluções, mas isso significa que a atividade ainda não produziu evidências da resolução ou do feedback da IA.

**Melhoria opcional:** resolver uma tarefa de cada vez e solicitar avaliação antes de avançar, usando:

```text
Esta é a minha tentativa para a tarefa atual: [RESPOSTA]. Avalie meu raciocínio com base nas fontes, indique acertos e pontos de melhoria e cite as referências. Não resolva a próxima tarefa antes da minha tentativa.
```

**Critério de validação:** registrar a tentativa, a correção fundamentada e o aprendizado obtido em cada etapa.

#### 4. Conceitos com cobertura superficial

**Problema observado:** no Prompt 4, o próprio NotebookLM informou que as fontes disponíveis apresentavam os conceitos de forma integrada, mas não aprofundavam todas as definições técnicas.

**Melhoria futura sugerida:** usar as documentações oficiais da linguagem SQL/PostgreSQL, do pandas e do Power BI e reformular a comparação para exigir uma referência direta em cada linha.

**Critério de validação:** cada conceito deve possuir definição rastreável, diferença objetiva, exemplo e indicação de eventuais lacunas.

### Modelo de registro

| Situação observada | Possível causa | Modificação no prompt | Como validar a melhora |
|---|---|---|---|
| Resposta muito genérica | Pedido amplo demais | Solicitar etapas, exemplos e referências | Verificar se cada parte foi respondida e citada |
| Mistura de fontes com conhecimento externo | Ausência de restrição | Adicionar “com base exclusivamente nas fontes” | Conferir as citações do NotebookLM |
| Comparação incompleta | Critérios não definidos | Informar colunas e critérios da comparação | Verificar se todos os conceitos possuem os mesmos campos |
| Exemplo tratado como fato | Prompt não separa evidência de hipótese | Pedir identificação de conteúdo fundamentado e exemplo didático | Conferir se a distinção aparece explicitamente |
| Linguagem avançada | Público não especificado | Definir o nível do estudante e pedir explicação de termos | Avaliar clareza e presença de definições |

### Registro de uma cicatriz real

Copie este bloco para cada problema encontrado:

```text
Data do teste:
Objetivo:
Prompt original:
Problema observado na resposta:
Referência que deveria ter sido utilizada:
Hipótese sobre a causa:
Prompt reformulado:
Resultado após o ajuste:
O que aprendi com o teste:
```

### Evidências recomendadas

- Trechos curtos das respostas, sempre identificados como resultado do NotebookLM;
- Referências mostradas pela ferramenta;
- Capturas de tela armazenadas em uma pasta `assets/`, sem dados pessoais;
- Explicação autoral sobre por que a primeira versão não foi suficiente;
- Comparação objetiva entre o prompt inicial e o prompt refinado.

## 7. Miniguia de estudo

### 7.1 O que é análise de dados?

Análise de dados é o processo de examinar informações para responder perguntas, identificar padrões e apoiar decisões. Em um projeto real, a ferramenta utilizada é apenas uma parte do trabalho. O ponto de partida deve ser uma pergunta de negócio clara, seguida pela obtenção, preparação, exploração e comunicação dos dados.

### 7.2 Fluxo analítico resumido

1. **Definir o problema:** transformar uma necessidade em pergunta mensurável;
2. **Identificar os dados:** localizar tabelas, arquivos e campos relevantes;
3. **Extrair os dados:** consultar e selecionar somente o necessário;
4. **Preparar os dados:** corrigir tipos, ausências, duplicidades e inconsistências;
5. **Explorar:** calcular estatísticas e observar distribuições e padrões;
6. **Analisar:** relacionar os resultados à pergunta inicial;
7. **Visualizar:** escolher representações adequadas à informação;
8. **Comunicar:** apresentar conclusão, evidências, limitações e próximos passos.

### 7.3 SQL no processo de análise

SQL é uma linguagem usada para trabalhar com dados armazenados em bancos relacionais. Em análise de dados, ela permite selecionar colunas, filtrar registros, ordenar resultados, combinar tabelas e produzir agregações.

```sql
SELECT
    categoria,
    COUNT(*) AS quantidade_entregas,
    SUM(valor) AS valor_total
FROM entregas
WHERE status = 'Concluída'
GROUP BY categoria
ORDER BY valor_total DESC;
```

O exemplo é didático. Ele demonstra uma sequência comum: selecionar dados, filtrar registros, agrupar categorias, calcular resultados e ordenar a saída.

### 7.4 pandas no processo de análise

pandas é uma biblioteca de Python voltada à manipulação e análise de dados tabulares. Sua principal estrutura é o `DataFrame`, que organiza dados em linhas e colunas. Pode ser utilizado para importar arquivos, selecionar dados, tratar valores ausentes, criar colunas, combinar tabelas e calcular estatísticas.

```python
import pandas as pd

df = pd.read_csv("entregas.csv")
df["data"] = pd.to_datetime(df["data"], errors="coerce")
df = df.drop_duplicates()

resumo = (
    df.loc[df["status"] == "Concluída"]
      .groupby("categoria", as_index=False)
      .agg(
          quantidade_entregas=("id_entrega", "count"),
          valor_total=("valor", "sum")
      )
      .sort_values("valor_total", ascending=False)
)
```

O código também é um exemplo didático e deve ser adaptado ao nome e ao tipo das colunas de um conjunto de dados real.

### 7.5 Power BI no processo de análise

Power BI é uma plataforma de análise e visualização. Em um fluxo de trabalho, pode ser utilizado para conectar fontes, preparar dados com Power Query, criar relacionamentos e medidas no modelo e construir relatórios interativos. A visualização deve ser escolhida conforme a pergunta: cartões para indicadores, linhas para evolução temporal, barras para comparação e tabelas para detalhamento.

### 7.6 Integração das ferramentas

| Etapa | Ferramenta possível | Exemplo de atividade |
|---|---|---|
| Extração | SQL | Consultar vendas de um período e combinar tabelas |
| Preparação e exploração | pandas | Corrigir tipos, remover duplicidades e calcular estatísticas |
| Modelagem e visualização | Power BI | Criar medidas, relacionamentos e painéis interativos |
| Comunicação | Power BI + documentação | Apresentar indicadores, limitações e recomendações |

As ferramentas podem se sobrepor. Tanto SQL quanto pandas podem filtrar e agregar dados; tanto pandas quanto Power Query podem transformar tabelas. A escolha depende do volume, da infraestrutura, da necessidade de automação e das competências da equipe.

### 7.7 Boas práticas

- Começar pela pergunta de negócio, não pelo gráfico;
- Manter os dados originais separados dos dados tratados;
- Registrar transformações e critérios adotados;
- Verificar valores ausentes, duplicados, tipos e intervalos inválidos;
- Validar cálculos com amostras pequenas;
- Usar nomes claros para tabelas, colunas e medidas;
- Evitar gráficos decorativos que dificultem a interpretação;
- Informar limitações e não confundir correlação com causalidade;
- Conferir a origem e a atualização das fontes;
- Tornar o processo reproduzível sempre que possível.

## 8. Glossário

| Conceito | Definição resumida |
|---|---|
| Agregação | Operação que resume vários registros, como soma, média ou contagem. |
| Banco de dados relacional | Sistema que organiza dados em relações, geralmente representadas por tabelas. |
| Coluna | Campo que representa uma característica dos registros. |
| Dashboard | Visão que reúne indicadores e visualizações para acompanhamento. |
| DataFrame | Estrutura bidimensional do pandas organizada em linhas e colunas. |
| DAX | Linguagem de expressões usada para cálculos em modelos do Power BI. |
| Dado bruto | Informação antes das etapas de preparação e validação. |
| ETL | Processo de extrair, transformar e carregar dados. |
| Filtro | Condição usada para restringir os registros analisados. |
| Granularidade | Nível de detalhe representado por cada registro. |
| Indicador | Medida utilizada para acompanhar um resultado ou objetivo. |
| JOIN | Operação SQL que combina linhas de tabelas relacionadas. |
| Limpeza de dados | Tratamento de ausências, duplicidades, erros e inconsistências. |
| Medida | Cálculo dinâmico avaliado conforme o contexto do relatório. |
| Modelagem de dados | Organização de tabelas, relacionamentos e regras de cálculo. |
| NotebookLM | Ferramenta de IA orientada pelas fontes adicionadas a um notebook. |
| Power Query | Recurso de conexão e transformação de dados usado no Power BI e em outros produtos Microsoft. |
| Prompt | Instrução ou pergunta fornecida a um sistema de Inteligência Artificial. |
| Relatório | Conjunto de páginas e visualizações criado para analisar informações. |
| SQL | Linguagem usada para consultar e manipular dados relacionais. |
| Tabela | Estrutura de dados composta por linhas e colunas. |
| Transformação | Alteração aplicada aos dados para adequá-los à análise. |
| Valor ausente | Dado que não foi informado ou não está disponível. |
| Visualização de dados | Representação gráfica criada para facilitar interpretação e comunicação. |

## 9. Prompts reutilizáveis

Os modelos abaixo podem ser adaptados para qualquer tema estudado no NotebookLM.

### Resumo rastreável

```text
Com base exclusivamente nas fontes selecionadas, produza um resumo estruturado sobre [TEMA]. Para cada seção, apresente a ideia central, um exemplo e a referência utilizada. Sinalize lacunas nas fontes em vez de preencher com conhecimento externo.
```

### Comparação de conceitos

```text
Compare [CONCEITO A] e [CONCEITO B] com os critérios: definição, finalidade, semelhanças, diferenças, exemplo de uso e erros comuns. Use somente as fontes e cite a evidência de cada conclusão.
```

### Tutor socrático

```text
Atue como tutor e me ajude a compreender [TEMA] por meio de perguntas. Faça uma pergunta por vez, espere minha resposta e dê feedback com base nas fontes. Não entregue a resposta completa antes da minha tentativa.
```

### Diagnóstico de lacunas

```text
Analise as fontes disponíveis para estudar [TEMA]. Informe quais subtemas estão bem cobertos, quais aparecem superficialmente e quais não possuem evidência suficiente. Sugira o tipo de fonte que deveria ser adicionado, sem inventar referências.
```

### Simulado

```text
Crie um simulado com [NÚMERO] questões sobre [TEMA], em dificuldade crescente. Misture questões conceituais e situações práticas. Aguarde minhas respostas e depois corrija cada item com explicação e referência às fontes.
```

### Refinamento de resposta

```text
Revise a resposta anterior e identifique: afirmações sem referência, trechos genéricos, conceitos não definidos e pontos que não responderam diretamente à pergunta. Em seguida, produza uma versão melhor, usando somente as fontes disponíveis.
```

## 10. Checklist do projeto

- [x] Tema relacionado ao objetivo profissional definido;
- [x] Pergunta norteadora criada;
- [x] Objetivo geral e objetivos específicos documentados;
- [x] Cinco fontes oficiais selecionadas;
- [x] Cinco materiais de estudo adicionados e processados no NotebookLM;
- [x] Primeira rodada dos sete prompts executada;
- [x] Respostas e referências da primeira rodada registradas;
- [x] Pelo menos duas cicatrizes reais documentadas;
- [x] Prompt 5 testado com geração de perguntas em dificuldade crescente;
- [x] Prompt 6 testado com geração de estudo de caso progressivo;
- [x] Prompt 7 registrado em versão básica;
- [x] Miniguia inicial produzido;
- [x] Glossário criado;
- [x] Prompts reutilizáveis organizados;
- [x] Evidências em vídeo analisadas e resultados registrados no README;
- [x] README revisado após a primeira rodada de testes;
- [ ] URL do repositório enviada na plataforma da DIO.

## 11. Conclusão

Este projeto demonstra que a Inteligência Artificial pode ser usada como apoio à aprendizagem sem substituir a análise crítica. A qualidade do resultado depende da seleção das fontes, da clareza das perguntas, da validação das referências e do registro transparente das limitações encontradas.

O uso conjunto de Power BI, SQL e Python oferece uma visão inicial de diferentes etapas do trabalho de um analista de dados. A construção do caderno também reforça competências importantes para um portfólio, como documentação, curadoria, comunicação técnica e melhoria iterativa de prompts.

A rodada de experimentos também revelou uma limitação metodológica importante: foram utilizados como fontes os próprios documentos do projeto. Em vez de esconder o problema, ele foi registrado como uma cicatriz real, demonstrando análise crítica e transparência sobre o processo. Como evolução futura, as cinco fontes oficiais poderão ser importadas diretamente para uma nova execução e comparação dos resultados.

## Autor

**Samuel Robert Alves Vitorino**

Estudante de Análise e Desenvolvimento de Sistemas, com foco no desenvolvimento de competências em Análise de Dados.

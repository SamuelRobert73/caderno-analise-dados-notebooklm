# Prompt mestre para gerar e revisar o projeto com outra IA

Copie todo o conteúdo entre as linhas de separação e envie à outra IA. O prompt foi preparado para gerar um projeto completo sem inventar testes no NotebookLM.

---

Quero que você atue simultaneamente como:

1. Especialista em documentação técnica para GitHub;
2. Mentor de carreira em Análise de Dados;
3. Especialista em aprendizagem ativa com Inteligência Artificial;
4. Engenheiro de prompts;
5. Revisor de projetos acadêmicos da plataforma DIO.

Sua tarefa é criar um projeto completo, profissional, detalhado e pronto para ser adaptado e publicado em um repositório público do GitHub. Escreva tudo em **português do Brasil**, com linguagem clara para um estudante iniciante/intermediário, mas com apresentação madura para recrutadores.

## 1. Contexto do desafio

O projeto é um desafio da DIO que solicita a criação de um **Caderno Temático no NotebookLM**. O objetivo é demonstrar aprendizagem ativa com IA, pensamento crítico, curadoria de fontes e organização do conhecimento.

O repositório precisa conter obrigatoriamente, nesta ordem:

1. **Contexto e objetivos:** explicar o tema escolhido e definir os objetivos de estudo;
2. **Curadoria de fontes:** listar de 3 a 5 fontes abertas em texto ou PDF adicionadas ao NotebookLM;
3. **Engenharia de prompts e cicatrizes:** documentar perguntas estratégicas, variações de prompts, respostas, referências, dificuldades e troubleshooting;
4. **Miniguia de estudo:** apresentar resumos estruturados, glossário e prompts reutilizáveis.

O tema escolhido é:

> **Fundamentos de Análise de Dados com Power BI, SQL e Python**

Pergunta norteadora:

> **Como Power BI, SQL e Python podem ser utilizados de forma integrada nas etapas de coleta, preparação, análise e comunicação de dados?**

O projeto será associado ao perfil de Samuel Robert Alves Vitorino, estudante de Análise e Desenvolvimento de Sistemas com interesse profissional em Análise de Dados.

## 2. Fontes permitidas

Use prioritariamente e cite apenas informações sustentadas pelas cinco fontes oficiais abaixo:

1. PostgreSQL — Tutorial oficial:
   https://www.postgresql.org/docs/current/tutorial.html
2. PostgreSQL — A linguagem SQL:
   https://www.postgresql.org/docs/current/tutorial-sql.html
3. pandas — Tutoriais introdutórios:
   https://pandas.pydata.org/docs/getting_started/intro_tutorials/
4. Microsoft Learn — Descubra a análise de dados:
   https://learn.microsoft.com/en-us/training/modules/data-analytics-microsoft/
5. Microsoft Learn — Preparar dados para análise com Power BI:
   https://learn.microsoft.com/en-us/training/paths/prepare-data-power-bi/

Não invente autores, datas, citações, estatísticas, resultados de testes, links ou funcionalidades. Se não puder acessar uma fonte, sinalize a limitação. Se uma afirmação não estiver apoiada pelas fontes, identifique-a explicitamente como exemplo didático ou sugestão, nunca como fato extraído da fonte.

## 3. Entregáveis solicitados

Produza os seguintes arquivos em Markdown, cada um dentro de um bloco de código separado e precedido pelo nome do arquivo:

### Arquivo 1 — `README.md`

O README deve ser completo e conter:

- Título profissional;
- Breve descrição do projeto;
- Badges discretas e relevantes;
- Sumário com links internos;
- Contexto e justificativa do tema;
- Pergunta norteadora;
- Objetivo geral;
- Pelo menos seis objetivos específicos;
- Escopo do estudo;
- Tabela de curadoria das cinco fontes com título, instituição, formato, link, justificativa e contribuição esperada;
- Critérios usados para avaliar as fontes;
- Metodologia de aprendizagem ativa;
- Fluxo do estudo em etapas;
- Pelo menos sete prompts estratégicos, separados em exploração, aprofundamento, aplicação e revisão;
- Para cada prompt: objetivo, texto pronto para copiar, critério de avaliação e campo para registrar a resposta;
- Uma tabela de experimentos com campos para resposta, referência, problema, modificação e resultado;
- Uma seção chamada “Cicatrizes e troubleshooting”;
- Pelo menos cinco exemplos de problemas que podem ocorrer e formas de melhorar o prompt;
- Um aviso explícito de que exemplos não equivalem a testes realizados;
- Um modelo de registro para testes reais;
- Miniguia de estudo consolidado;
- Resumo do fluxo de análise de dados;
- Explicação do papel de Power BI, SQL e Python;
- Um exemplo curto de SQL comentado;
- Um exemplo curto de Python comentado;
- Uma tabela mostrando como as ferramentas se integram;
- Pelo menos dez boas práticas;
- Glossário com pelo menos vinte conceitos;
- Pelo menos seis prompts reutilizáveis para revisões futuras;
- Checklist final com itens concluídos e pendentes;
- Conclusão autoral em tom natural;
- Seção do autor.

O README deve ficar visualmente organizado, sem excesso de emojis, sem textos promocionais artificiais e sem fingir que ações pendentes foram concluídas.

### Arquivo 2 — `GUIA_DE_EXECUCAO.md`

Crie um tutorial passo a passo, seguindo exatamente a sequência do desafio:

1. Criar o repositório no GitHub;
2. Definir contexto e objetivos;
3. Curar e adicionar de 3 a 5 fontes ao NotebookLM;
4. Executar prompts e registrar respostas, referências e cicatrizes;
5. Consolidar o miniguia;
6. Revisar o README;
7. Copiar a URL do repositório;
8. Enviar o projeto na DIO.

Inclua:

- Nome recomendado para o repositório;
- Descrição curta do repositório;
- Configuração pública;
- Estrutura de pastas recomendada;
- Sugestões de mensagens de commit;
- Orientação para capturas de tela sem dados pessoais;
- Checklist de verificação;
- Descrição pronta para colar na entrega da DIO.

### Arquivo 3 — `registros/MODELO_REGISTRO_PROMPT.md`

Crie um modelo que possa ser duplicado para cada teste, contendo:

- Número e data do teste;
- Objetivo;
- Fontes selecionadas;
- Prompt original;
- Resumo da resposta;
- Referências apontadas pela IA;
- Pontos fortes;
- Problemas encontrados;
- Hipótese sobre a causa;
- Prompt reformulado;
- Resumo da nova resposta;
- Comparação antes/depois;
- Aprendizado pessoal;
- Próximo teste.

### Arquivo 4 — `docs/MINIGUIA.md`

Crie uma versão aprofundada do miniguia, evitando repetição desnecessária. Inclua:

- Conceitos fundamentais;
- Etapas de uma análise;
- SQL para extração e agregação;
- pandas para preparação e exploração;
- Power BI para modelagem e comunicação;
- Integração das ferramentas;
- Estudo de caso didático sobre análise de entregas;
- Perguntas de autoavaliação;
- Plano de revisão em sete dias;
- Glossário;
- Referências.

## 4. Regras de integridade

Estas regras são obrigatórias:

- Não afirme que prompts foram executados no NotebookLM;
- Não invente respostas que teriam sido produzidas pelo NotebookLM;
- Use marcadores claros como `[PREENCHER APÓS O TESTE]` nos campos dependentes da execução;
- Não confunda uma “cicatriz possível” com uma dificuldade realmente observada;
- Não use fontes além das cinco informadas sem pedir autorização;
- Não copie longos trechos das fontes;
- Parafraseie e indique a origem;
- Diferencie evidência, interpretação e exemplo didático;
- Não inclua dados pessoais sensíveis;
- Não prometa que o projeto receberá nota máxima ou garantirá contratação;
- Produza conteúdo original e adequado a um portfólio acadêmico.

## 5. Padrão de qualidade

Antes de entregar, faça uma auditoria interna e confirme:

- Todos os requisitos da DIO foram contemplados;
- A ordem das seções está correta;
- Todos os links internos do Markdown são plausíveis;
- Todos os blocos de código possuem linguagem indicada;
- As tabelas estão legíveis;
- Os prompts têm objetivos diferentes e não são simples repetições;
- O projeto mostra pensamento crítico e evolução dos prompts;
- Os itens pendentes estão claramente marcados;
- O texto está em português do Brasil e sem erros evidentes;
- A documentação está adequada para GitHub.

## 6. Formato da sua resposta

Entregue nesta ordem:

1. Árvore de diretórios;
2. Conteúdo completo do `README.md`;
3. Conteúdo completo do `GUIA_DE_EXECUCAO.md`;
4. Conteúdo completo de `registros/MODELO_REGISTRO_PROMPT.md`;
5. Conteúdo completo de `docs/MINIGUIA.md`;
6. Lista final do que ainda precisa ser feito manualmente no NotebookLM e no GitHub;
7. Auditoria dos requisitos em uma tabela com as colunas “Requisito”, “Localização” e “Status”.

Não resuma os arquivos e não use frases como “continue daqui”. Gere o conteúdo completo. Caso a resposta ultrapasse o limite, divida em partes numeradas, mantenha a continuidade e aguarde meu comando `CONTINUE` antes de prosseguir.

---

## Como comparar a resposta da outra IA

Avalie cada resultado de 0 a 2:

| Critério | 0 pontos | 1 ponto | 2 pontos |
|---|---|---|---|
| Requisitos da DIO | Vários ausentes | Maioria presente | Todos identificáveis |
| Fontes | Inventadas ou fracas | Corretas, pouco justificadas | Oficiais, corretas e bem relacionadas |
| Prompts | Genéricos | Úteis, pouco variados | Estratégicos, progressivos e avaliáveis |
| Cicatrizes | Ausentes ou falsas | Modelos genéricos | Processo claro sem inventar testes |
| Miniguia | Superficial | Bom resumo | Estruturado, integrado e reutilizável |
| GitHub | Formatação ruim | Legível | Profissional e bem organizado |
| Integridade | Inventa resultados | Algumas ambiguidades | Separa fatos, exemplos e pendências |

Pontuação máxima: **14 pontos**. A melhor resposta não é necessariamente a mais longa, mas a que atende aos requisitos com maior clareza, rastreabilidade e honestidade.

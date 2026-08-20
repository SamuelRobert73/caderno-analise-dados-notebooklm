# Guia de execução do desafio DIO — Caderno Temático no NotebookLM

Este roteiro segue a sequência apresentada no enunciado da DIO e separa o que já está pronto do que depende da execução no NotebookLM e no GitHub.

## Visão geral do que será entregue

O resultado principal será um repositório público no GitHub contendo um `README.md` com:

1. Contexto e objetivos;
2. Curadoria de 3 a 5 fontes;
3. Prompts testados, respostas, referências e cicatrizes;
4. Miniguia com resumo, glossário e prompts reutilizáveis.

## Antes de começar

Tenha acesso a:

- Uma conta do GitHub;
- Uma conta que permita utilizar o NotebookLM;
- Os cinco links listados no `README.md`;
- Um editor de texto, como o editor do próprio GitHub ou o Visual Studio Code.

## Parte 1 — Entender a proposta do desafio

O trabalho não consiste apenas em pedir um resumo a uma IA. Ele avalia quatro capacidades:

- Escolher um tema com objetivo definido;
- Selecionar fontes confiáveis;
- Formular e melhorar prompts;
- Consolidar e documentar o aprendizado.

O tema sugerido é **Fundamentos de Análise de Dados com Power BI, SQL e Python**, por sua relação com a carreira de analista de dados.

## Parte 2 — Criar o repositório no GitHub

1. Entre em [github.com](https://github.com/);
2. Clique no sinal `+` no canto superior e em **New repository**;
3. Use o nome `caderno-analise-dados-notebooklm`;
4. Na descrição, escreva:

   > Caderno temático sobre fundamentos de análise de dados, desenvolvido com curadoria de fontes e engenharia de prompts no NotebookLM para um desafio da DIO.

5. Marque o repositório como **Public**;
6. Marque a opção para adicionar um arquivo `README`;
7. Selecione a licença MIT apenas se quiser permitir formalmente o reaproveitamento do material;
8. Clique em **Create repository**.

### O que copiar para o repositório

- Substitua o conteúdo do `README.md` do GitHub pelo conteúdo do arquivo `README.md` deste projeto;
- Adicione o arquivo `GUIA_DE_EXECUCAO.md` se quiser mostrar seu processo;
- Adicione o arquivo `PROMPT_MESTRE_OUTRA_IA.md` apenas se desejar demonstrar como comparou resultados entre IAs;
- Opcionalmente, crie a pasta `assets/` para capturas de tela.

## Parte 3 — Contexto e objetivos

Esta é a primeira seção exigida para o repositório “Nota 10”. Ela já está redigida no `README.md`.

Antes de publicar, confirme se o texto representa verdadeiramente seus objetivos. Altere qualquer frase que não corresponda à sua experiência.

Resultado esperado:

- Tema claramente identificado;
- Justificativa pessoal e profissional;
- Pergunta norteadora;
- Objetivo geral;
- Objetivos específicos verificáveis.

## Parte 4 — Curadoria das fontes

Esta é a segunda seção exigida.

1. Abra cada um dos cinco links do `README.md`;
2. Confirme que a fonte pertence ao site oficial indicado;
3. Leia o título, a introdução e o sumário de cada material;
4. Entre no NotebookLM e crie um novo notebook;
5. Dê o nome `Caderno Temático — Fundamentos de Análise de Dados com Power BI, SQL e Python`;
6. Adicione os links um de cada vez;
7. Confirme se cada fonte foi processada corretamente;
8. Caso uma página não seja aceita, utilize outra página equivalente da mesma documentação e atualize o README;
9. Não adicione dezenas de páginas: a DIO pede curadoria, portanto 3 a 5 fontes bem justificadas são melhores do que uma coleção sem critério.

Resultado esperado:

- Cinco fontes processadas;
- Lista com título, link, instituição, formato e justificativa;
- Data de acesso documentada.

## Parte 5 — Engenharia de prompts e cicatrizes

Esta é a terceira seção exigida e a que mais diferencia o projeto.

### Execução dos testes

1. No NotebookLM, execute o Prompt 1 do README;
2. Leia a resposta por completo;
3. Abra as referências citadas pela ferramenta;
4. Registre no README uma síntese com suas próprias palavras;
5. Avalie se a resposta foi completa, clara e sustentada pelas fontes;
6. Se houver problema, copie o prompt original e descreva a dificuldade;
7. Reformule o prompt para corrigir o problema;
8. Execute a nova versão;
9. Compare as duas respostas;
10. Repita o processo com os demais prompts.

### O que deve ser registrado em cada teste

- Data;
- Objetivo da pergunta;
- Prompt utilizado;
- Síntese da resposta;
- Fontes citadas pelo NotebookLM;
- Pontos fortes;
- Problemas ou ausências;
- Alteração feita no prompt;
- Resultado obtido depois da alteração;
- Aprendizado pessoal.

### Como documentar uma resposta sem deixar o README enorme

Use uma síntese de um ou dois parágrafos no README. Caso deseje preservar a resposta completa, crie um arquivo dentro de `registros/`, por exemplo:

```text
registros/
├── teste-01-visao-geral.md
├── teste-02-papel-ferramentas.md
└── teste-03-fluxo-integrado.md
```

No README, adicione um link para o registro completo.

### Quantidade recomendada

- Execute ao menos cinco prompts;
- Documente pelo menos duas reformulações reais;
- Inclua evidências de que verificou as referências;
- Nunca diga que um teste foi realizado sem tê-lo executado.

## Parte 6 — Miniguia de estudo

Esta é a quarta seção exigida. Uma versão inicial já foi preparada no `README.md`.

Depois dos testes no NotebookLM:

1. Compare o miniguia inicial com as respostas obtidas;
2. Corrija trechos que não estiverem bem sustentados;
3. Acrescente exemplos que tenham sido validados;
4. Mantenha o resumo dividido em seções curtas;
5. Revise o glossário;
6. Confirme se os prompts reutilizáveis servem para futuras revisões;
7. Escreva a conclusão com suas próprias palavras.

Resultado esperado:

- Resumo estruturado;
- Glossário com conceitos principais;
- Conjunto de prompts reutilizáveis;
- Relação clara entre as fontes e o conteúdo final.

## Parte 7 — Revisar e publicar o README

1. Verifique se todas as caixas do checklist foram marcadas honestamente;
2. Teste todos os links;
3. Corrija erros de português;
4. Remova observações como “A preencher” somente quando houver conteúdo real;
5. Confirme se nenhuma captura expõe e-mail, dados pessoais ou outras informações sensíveis;
6. Faça o commit com uma mensagem clara, como:

```text
docs: finaliza caderno temático de análise de dados
```

7. Abra a página inicial do repositório e confira a apresentação final.

## Parte 8 — Entregar na DIO exatamente na sequência solicitada

1. Acesse o repositório final no GitHub;
2. Copie a URL principal, semelhante a `https://github.com/seu-usuario/caderno-analise-dados-notebooklm`;
3. Volte à página do desafio de projeto na DIO;
4. Clique no botão para entregar o projeto;
5. Cole a URL do repositório;
6. Use a descrição sugerida abaixo;
7. Confirme a entrega.

### Descrição sugerida para a DIO

> Desenvolvi um caderno temático sobre Fundamentos de Análise de Dados com Power BI, SQL e Python. O projeto reúne curadoria de fontes oficiais, experimentos de engenharia de prompts no NotebookLM, registro de dificuldades e refinamentos, além de um miniguia com resumo, glossário e prompts reutilizáveis para futuras revisões.

## Estrutura recomendada do repositório

```text
caderno-analise-dados-notebooklm/
├── README.md
├── GUIA_DE_EXECUCAO.md
├── PROMPT_MESTRE_OUTRA_IA.md
├── assets/
│   ├── notebook-fontes.png
│   └── exemplo-prompt.png
└── registros/
    ├── teste-01-visao-geral.md
    └── teste-02-prompt-refinado.md
```

As pastas `assets/` e `registros/` só precisam ser criadas quando houver arquivos reais para colocar nelas.

## Critérios de revisão final

| Critério | Pergunta de conferência |
|---|---|
| Clareza | Um visitante entende o tema nos primeiros parágrafos? |
| Curadoria | As fontes são oficiais, abertas e justificadas? |
| Rastreabilidade | As conclusões importantes apontam para fontes? |
| Pensamento crítico | Há registro de respostas insuficientes e refinamentos? |
| Honestidade | O repositório diferencia o que foi testado do que é modelo? |
| Reutilização | O glossário e os prompts servem para revisões futuras? |
| Apresentação | Títulos, tabelas, links e códigos estão bem formatados? |

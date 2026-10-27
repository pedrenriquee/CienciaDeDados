<img src="assets/logo-udf.jpg" alt="UDF Centro Universitário" width="230">

**Profa. Kadidja Valéria | UDF**  
Ciência de Dados e Aprendizado de Máquina · Sistemas de Informação · 2026.2

# PBL integrador — Apoio à Permanência

## Identificação

- Estudante ou equipe: **Pedro Henrique Matos Lopes**
- Turma: **Ciencia de Dados**
- Data de realização: **27/10/2026**
- Integrantes e contribuições (se em equipe): **Pedro Henrique Matos Lopes**

## Contexto

Uma instituição quer compreender sinais associados à evasão e oferecer apoio antes do fim do semestre. Público-alvo: estudantes matriculados e equipe de apoio acadêmico. O cenário é didático e a prática usa dados sintéticos.

**Questão norteadora:** como identificar situações que merecem atenção e oferecer apoio, reconhecendo erros do modelo e dificuldades que os dados não capturam?

## Proposta da equipe

### 1. Delimitação

- Problema e público: **Parte dos estudantes de graduação deixa o curso sem que a instituição perceba a tempo de oferecer apoio. O público-alvo do estudo são os estudantes matriculados em cursos de graduação presenciais. O público-alvo do uso do resultado é a equipe de apoio acadêmico (coordenação, tutoria e serviço de acolhimento).**
- Decisão que o resultado pode apoiar: **O resultado pode trazer uma base para a (coordenação, tutoria e serviço de acolhimento) conseguia assim decidir que estudantes precisam de apoio mais rapidamente**
- Definição de evasão, unidade e horizonte: **Evasão (variável-alvo): o estudante não renovar a matrícula no semestre seguinte, sem ter concluído o curso (valor 1). Quem renova a matrícula recebe valor 0. Não se distingue aqui entre desistência, transferência ou trancamento, e essa é uma limitação reconhecida.
Unidade de análise: estudante-semestre. Cada linha representa um estudante em um semestre letivo. O mesmo estudante pode aparecer em mais de um semestre.
Horizonte de previsão: os sinais são medidos até a semana 8 do semestre corrente e o desfecho é observado na rematrícula do semestre seguinte.**

### 2. Perguntas de negócio

1. **Quais sinais observáveis até a oitava semana (frequência, notas parciais, acessos ao AVA, entrega de atividades, trancamento prévio) estão associados à não renovação de matrícula,**
2. **O desempenho do modelo (recall, precisão e taxa de falsos positivos) é semelhante entre subgrupos (turno, tipo de bolsa, trabalho, distância do campus), ou há grupos para os quais ele erra mais, de modo que o apoio fique desigual?**

### 3. Dados necessários

| Dado | Papel no projeto | Disponível quando? | Origem pretendida | Necessidade e risco |
| --- | --- | --- | --- | --- |
| id_estudante | Identificador para agrupar linhas do mesmo estudante | Na Matricula | Sistema Academico | Necessário para o agrupamento |
| evadiu_proximo_semestre | é o que o modelo tenta prever (1 = não renovou a matrícula, 0 = renovou) | só na rematrícula do semestre seguinte. | sistema acadêmico. | como é um resultado só fica conhecida ao final do processo |
Diferencie dados usados na simulação e dados que seriam necessários para uma investigação real: **Os dados necessários para simulação são ainda menores do que o necessário para uma investigação real que podem incluir coisas não relacionadas a vida pessoal do estudantes como nucleo pessoal e etc. **

### 4. Abordagem e algoritmo

- Classificação, regressão ou outra formulação, com justificativa: **Usaremos classificação binária supervisionada. A equipe de apoio precisa decidir, para cada estudante, se vale a pena convidá-lo para uma conversa de apoio, o que é uma pergunta de sim ou não. O modelo aprende com dados em que já se sabe quem evadiu e quem permaneceu**
- Algoritmo introdutório escolhido: **Regressão logistica, algoritmo escolhido pois com ele é possivel realizar uma analise de maior ou menor probabilidade de estudante evadir ou não**
- Referência simples: **Utilizada duas referencias **

### 5. Avaliação

- Preparação, divisão e validação: **PREENCHER**
- Métricas e razão da escolha: **PREENCHER**
- Resultados efetivamente calculados e link da evidência: **PREENCHER**
- Erros relevantes e consequências: **PREENCHER**

### 6. Limites e proteção

- Por que os resultados não demonstram causalidade? **PREENCHER**
- Por que dados sintéticos não validam uso institucional? **PREENCHER**
- Que grupos podem ser mal representados? Como investigar isso com evidências apropriadas? **PREENCHER**
- Como minimizar dados, restringir acesso e definir retenção? **PREENCHER**
- Como garantir revisão humana e contestação? **PREENCHER**

### 7. Recomendações de apoio

- Ação voluntária proposta: **PREENCHER**
- Como acolher estudantes não sinalizados pelo modelo: **PREENCHER**
- O que precisa ser verificado antes de aplicação real: **PREENCHER**

Previsões não são certezas. Priorize apoio e revisão humana, sem punições ou decisões automáticas prejudiciais.

## Apresentação de cinco minutos

| Tempo | Conteúdo | Responsável |
| --- | --- | --- |
| 1 minuto | Problema e dados | PREENCHER |
| 2 minutos | Método e resultados | PREENCHER |
| 1 minuto | Limitações | PREENCHER |
| 1 minuto | Recomendações de apoio | PREENCHER |

## Contribuições

| Integrante | Contribuição verificável |
| --- | --- |
| PREENCHER | PREENCHER |

[Voltar ao início](README.md).

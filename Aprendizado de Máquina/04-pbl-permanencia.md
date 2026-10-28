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
- Referência simples: **Utilizada duas referencias em que ambas são calculadas no mesmo conjunto de testes que são a classe majoritaria e uma regra de frenquencia, a primeira para prever se todos os alunos vão permanecer e a segunda é uma regra por frequência: sinalizar os estudantes com frequência média abaixo de 75% **

### 5. Avaliação

- Preparação, divisão e validação: **antes do treino, os valores faltantes das variáveis numéricas são preenchidos com a mediana e depois todas são colocadas na mesma escala (padronização). Essas etapas ficam dentro de um Pipeline, que as calcula usando apenas os dados de treino e depois as aplica ao teste.**
- Métricas e razão da escolha: **Usar recall, precisão, F1, PR-AUC e matriz de confusão. A métrica principal é o recall, porque deixar de identificar um estudante que precisava de apoio custa mais do que convidar quem não precisava. A acurácia não é a principal, porque a evasão é minoria e ela engana**
- Resultados efetivamente calculados e link da evidência: **https://colab.research.google.com/drive/1Nu8iotSPSJjz29LK4u0TzcPd04SLhetq?usp=sharing base tem 6123 linhas (3000 estudantes) e 23,3% de evasão. O treino ficou com 4899 linhas e o teste com 1224. Na validação cruzada, a regressão logística teve recall médio de 0,762 e a árvore de decisão teve 0,746. A PR-AUC foi 0,620 para a logística e 0,533 para a árvore, então escolhi a regressão logística. O limiar escolhido no treino foi 0,467. No teste, a matriz de confusão foi: 677 estudantes que permaneceram e foram previstos corretamente, 262 falsos positivos, 70 falsos negativos e 215 evasões encontradas.**
- Erros relevantes e consequências: **O falso negativo é quando o modelo não sinaliza um estudante que depois evade. É o erro mais grave, porque ele fica sem apoio. No teste foram 70 casos.**

### 6. Limites e proteção

- Por que os resultados não demonstram causalidade? **O modelo só mostra associação entre os sinais e a evasão, e não explica o motivo da saída. A frequência baixa, por exemplo, pode ser consequência de um problema de saúde ou de trabalho, e não a causa da evasão..**
- Por que dados sintéticos não validam uso institucional? **Porque foram gerados por código e as regras foram definidas por nós, então o modelo só descobre o que já colocamos. Eles servem para aprender o método, mas não para decidir sobre estudantes reais.**
- Que grupos podem ser mal representados? Como investigar isso com evidências apropriadas? **Podem ser mal representados ingressantes, estudantes que trabalham, quem tem internet limitada e quem mora longe do campus. Para investigar, calculamos recall, precisão e falsos positivos separadamente por subgrupo no teste, olhando também o tamanho de cada grupo.**
- Como minimizar dados, restringir acesso e definir retenção? **Usaremos só os dados necessários, sem nome, CPF ou endereço, e com o identificador pseudonimizado. Só a equipe técnica acessa a base completa, e a equipe de apoio vê apenas a lista de convites. Os dados são guardados por um prazo definido antes e depois eliminados, conforme a LGPD.**
- Como garantir revisão humana e contestação? **O modelo só sugere, e a equipe de apoio revisa cada caso antes de qualquer contato. O estudante deve ter um canal simples para perguntar se foi sinalizado, pedir revisão ou corrigir dados, e uma pessoa responde.**

### 7. Recomendações de apoio

- Ação voluntária proposta: **Enviar um convite individual e acolhedor para uma conversa opcional com a equipe de apoio, em que o estudante pode conhecer opções como monitoria e orientação sobre bolsas. O convite não cita o modelo e pode ser recusado sem consequência. Como o modelo sinaliza 39% dos estudantes, a equipe pode começar pelos de maior probabilidade, conforme sua capacidade.**
- Como acolher estudantes não sinalizados pelo modelo: **O apoio deve ser divulgado para todos, com um canal aberto para quem quiser procurar ajuda. Isso é importante porque o modelo deixou passar 70 estudantes que evadiram no teste. Professores e tutores também podem encaminhar estudantes em que perceberam dificuldades.**
- O que precisa ser verificado antes de aplicação real: **Seria preciso ter aprovação do comitê de ética e do responsável por dados (LGPD) e testar com dados reais de semestres diferentes. Também seria preciso melhorar o recall, que ficou abaixo da meta, analisar o desempenho por subgrupo com mais dados, ver se a quantidade de sinalizados cabe na equipe e acompanhar o modelo ao longo do tempo.**

Previsões não são certezas. Priorize apoio e revisão humana, sem punições ou decisões automáticas prejudiciais.

## Apresentação de cinco minutos

| Tempo | Conteúdo | Responsável |
| --- | --- | --- |
| 1 minuto | Problema e dados | Pedro Henrique |
| 2 minutos | Método e resultados | Pedro Henrique |
| 1 minuto | Limitações | Pedro Henrique |
| 1 minuto | Recomendações de apoio | Pedro Henrique |

## Contribuições

| Integrante | Contribuição verificável |
| --- | --- |
| Pedro Henrique Matos Lopes | Definição do problema, geração dos dados sintéticos, execução do código, análise dos resultados, escrita do documento e apresentação |

[Voltar ao início](README.md).

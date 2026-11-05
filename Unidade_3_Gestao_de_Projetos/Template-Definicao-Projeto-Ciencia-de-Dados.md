# Template - Definição do Projeto de Ciência de Dados

**Unidade:** III - Gestão de Projetos  
**Metodologia:** PBL + trabalho em equipes  
**Entregável:** Documento de definição do projeto

> **Finalidade:** delimitar um problema real e orientar o desenvolvimento do projeto de Ciência de Dados. Preencha todos os campos com informações objetivas, verificáveis e coerentes entre si.

## 1. Identificação do projeto

| Campo | Preenchimento |
|---|---|
| Título provisório do projeto | |
| Curso / disciplina | Ciência de Dados |
| Turma | Noturno |
| Equipe | Pedro Henrique Matos Lopes |
| Integrantes e funções iniciais |Pedro Henrique Matos Lopes função: obter dados e realizar analise e preencher formulário |
| Professor(a) | Kadidja |
| Data de elaboração | 04/11|
| Versão do documento | 1.0 |

## 2. Visão geral

### 2.1 Resumo do projeto

Em até 100 palavras, apresente o problema, o público-alvo, a proposta de análise e o resultado esperado.

**Preenchimento:**
Este projeto analisa os microdados públicos do ENEM, divulgados pelo INEP, para entender como renda familiar, tipo de escola e escolaridade dos pais se relacionam com as notas dos candidatos. O público-alvo são gestores e professores da educação básica pública, que precisam decidir onde concentrar ações de apoio. Faremos análise exploratória, visualizações e, se der tempo, uma regressão simples. Esperamos entregar uma base tratada, gráficos comparando grupos e um relatório curto com os principais achados e suas limitações.

### 2.2 Declaração do projeto em uma frase
Nosso projeto utilizará os microdados do **ENEM** para compreender como **renda e tipo** de escola se relacionam com as notas.

## 3. Contexto e definição do problema

### 3.1 Contexto

Descreva a situação atual, o ambiente em que o problema ocorre e as evidências iniciais que demonstram sua relevância.

- Onde o problema ocorre? No sistema de ensino básico brasileiro
- Quem é afetado? Os estudantes da escola publica. 
- Quais sinais, dados ou relatos indicam sua existência? Os microdados do ENEM trazem, para cada candidato, as notas e as respostas de um questionário socioeconômico. Isso permite comparar grupos. Ainda não calculamos nada, então qualquer diferença entre grupos é uma expectativa nossa, a ser verificada.
- Por que é importante investigá-lo agora? O ENEM é a principal porta de entrada para o ensino superior, e entender quais fatores estão associados a notas mais baixas pode ajudar a direcionar apoio

### 3.2 Problema central

Gestores e professores da educação básica pública enfrentam dificuldade para saber quais condições socioeconômicas mais se associam a notas baixas no contexto do ENEM, produzindo ações de apoio pouco direcionadas e a persistência de diferenças de desempenho entre grupos de estudantes.
### 3.3 Evidências iniciais

| Evidência | Fonte | O que ela indica? | Confiabilidade / limitação |
|---|---|---|---|
| 1. |Microdados do ENEM (notas e questionário socioeconômico) |INEP (portal de dados abertos) | Permite comparar notas entre grupos de renda, tipo de escola e escolaridade dos pais|Fonte oficial e anonimizada. Informações socioeconômicas são autodeclaradas e só incluem quem fez a prova
| 2. | Relatórios e sínteses de resultados do ENEM | INEP [documentos específicos a confirmar]| Resultados agregados por tipo de escola e região, úteis para conferir nossos números | Dependem de qual edição for usada. Precisamos localizar e citar corretamente

## 4. Público-alvo e partes interessadas

### 4.1 Público-alvo principal

| Aspecto | Descrição |
|---|---|
| Quem são os usuários ou beneficiários? | Gestores de escolas e redes públicas, professores do ensino médio e, indiretamente, os estudantes |
| Quais necessidades possuem? | Entender com clareza quais grupos têm mais dificuldade, para planejar reforço, orientação e uso de recursos |
| Como são afetados pelo problema? |Tem recursos limitados e poucas informações organizadas para decidir onde agir primeiro |
| Que decisão ou ação poderão tomar com os resultados? | Priorizar grupos ou tipos de apoio (reforço, orientação para o exame) com base em padrões observados|

### 4.2 Partes interessadas

| Parte interessada | Interesse no projeto | Influência | Forma de envolvimento |
|---|---|---|---|
|Gestores e professores da educação básica | Usar os resultados para planejar apoio| Média | Público de referência dos resultados. Não haverá contato direto, só a visão deles na redação |
|Professor(a) / orientador(a) da disciplina | Avaliar o rigor e a coerência do projeto|  Alta | Validação do escopo, feedback nas entregas |
## 5. Objetivos do projeto

### 5.1 Objetivo geral
Analisar os microdados do ENEM de uma edição recente para descrever como renda familiar, tipo de escola e escolaridade dos pais se relacionam com o desempenho dos candidatos, de modo a apoiar decisões de gestores e professores da educação básica pública.

### 5.2 Objetivos específicos

Defina de três a cinco objetivos mensuráveis e compatíveis com o prazo do projeto.

| Nº | Objetivo específico | Evidência de conclusão |
|---:|---|---|
| 1 | Obter e preparar uma base tratada com as variáveis de interesse, documentando as decisões de limpeza | Base tratada e dicionário de variáveis com o registro dos tratamentos|
| 2 |Descrever o desempenho dos candidatos nas áreas do exame e o perfil socioeconômico da amostra | Análise exploratória com tabelas de resumo e pelo menos 5 gráficos|
| 3 |Comparar as notas entre grupos de renda, tipo de escola e escolaridade dos pais | Tabelas e gráficos comparativos, com as diferenças observadas descritas no relatório|

### 5.3 Verificação dos objetivos

Marque após revisar:

- [x ] São específicos e escritos com clareza.
- [ x] Podem ser verificados por meio de entregáveis ou métricas.
- [ ] São viáveis com os dados, recursos e tempo disponíveis.
- [x ] Estão diretamente relacionados ao problema central.
- [ x] Consideram os usuários e a decisão que será apoiada.

## 6. Perguntas de negócio

As perguntas de negócio orientam a coleta, a análise e a comunicação dos resultados. Evite perguntas que possam ser respondidas apenas com “sim” ou “não”.

| Nº | Pergunta de negócio | Decisão apoiada | Dados necessários | Análise ou indicador possível |
|---:|---|---|---|---|
| 1 | Como as notas se distribuem entre os candidatos de diferentes faixas de renda familiar? | Quais faixas de renda priorizar em ações de apoio| Notas por área, faixa de renda | Média e mediana por faixa; boxplot |
| 2 | 	De que maneira o desempenho varia entre candidatos de escolas públicas e privadas? | Onde reforçar a preparação para o exame|Notas por área, tipo de escola | Diferença de médias entre grupos; gráfico de barras |
| 3 |Como a escolaridade dos pais se relaciona com a nota dos filhos? | Se vale incluir as famílias em ações de orientação | Notas, escolaridade do pai e da mãe| Média por nível de escolaridade; tabela cruzada|

## 7. Hipóteses iniciais

Registre suposições que serão investigadas, sem apresentá-las como conclusões.

| Hipótese | Como poderá ser testada? | Resultado que a refutaria? |
|---|---|---|
| H1. Candidatos de faixas de renda mais altas têm notas médias maiores do que os de faixas mais baixas. | Comparar médias e medianas por faixa de renda e verificar a tendência nos gráficos| Médias parecidas entre as faixas, ou sem tendência de crescimento |
| H2. A diferença de desempenho entre escolas públicas e privadas é maior na redação do que nas demais áreas. | Calcular a diferença de médias entre os dois tipos de escola em cada área|Diferença na redação igual ou menor que nas outras áreas |
| H3. Quanto maior a escolaridade da mãe, maior a nota média do candidato. | Calcular a média por nível de escolaridade da mãe e observar se há aumento progressivo| Notas sem relação aparente com a escolaridade da mãe |

## 8. Dados necessários e viabilidade

| Conjunto ou fonte de dados | Variáveis principais | Formato | Acesso / responsável | Qualidade esperada |
|---|---|---|---|---|
| Microdados do ENEM, de uma edição recente [ano a confirmar]|Notas por área e redação, renda familiar, tipo de escola, escolaridade dos pais, presença nas provas |CSV | Download no portal do INEP| Boa, por ser fonte oficial, mas com campos vazios e faltantes|
|Dicionário de variáveis do ENEM | Descrição e códigos de cada coluna | Planilha ou PDF | Mesmo pacote de download| Boa. Será conferido antes de qualquer análise|

### 8.1 Avaliação inicial dos dados

- **Disponibilidade:** Dados públicos e gratuitos, disponíveis no portal do INEP. Ainda vamos confirmar a edição mais recente e o link.
- - **Volume e período coberto:** Base grande, com milhões de linhas e muitas colunas, ao que sabemos. Vamos verificar o tamanho real e decidir se usamos uma única edição ou uma amostra, para o computador aguentar.
- **Dados ausentes, duplicados ou inconsistentes previstos:** Esperamos muitas notas vazias (quem faltou à prova)
- **Necessidade de integração entre fontes:** : Em princípio não. Usaremos uma única base, com o dicionário como apoio.
- **Restrições legais, contratuais ou institucionais:** Os dados são públicos e anonimizados

- [ ] A equipe verificou se há dados pessoais ou sensíveis.
- [ x] A coleta e o uso dos dados possuem finalidade legítima e explícita.
- [x ] O acesso será limitado às pessoas autorizadas.
- [ x] Dados pessoais serão minimizados, anonimizados ou pseudonimizados quando necessário.
- [ x] Possíveis vieses e impactos sobre grupos serão analisados.
- [ x] A divulgação dos resultados evitará reidentificação ou exposição indevida.



## 9. Escopo do projeto

| Dentro do escopo | Fora do escopo |
|---|---|
|Uso de uma edição do ENEM (ou amostra) | Comparação entre várias edições ao longo dos anos|
| Limpeza e documentação da base| 	Análises por município ou escola individual |
| Análise exploratória e comparação entre grupos| Afirmar relações de causa e efeito |

**Restrições conhecidas:** tempo, acesso a dados, ferramentas, infraestrutura, conhecimento técnico ou normas.
base grande, que pode exigir amostra ou mais tempo de processamento; pouca experiência da equipe em estatística para modelagem, então o modelo será simples e opcional; ferramentas ainda a confirmar com a equipe.


## 10. Resultados e entregáveis previstos

| Entregável | Descrição | Formato | Responsável | Critério de aceite |
|---|---|---|---|---|
| Base tratada | Base com colunas selecionadas, valores faltantes tratados e dicionário de decisões de limpeza | CSV + documento de apoio | [integrante a definir] | Regras de limpeza documentadas e repetíveis; nenhuma coluna usada sem descrição |
| Análise exploratória | Resumo estatístico e gráficos de distribuição do perfil dos candidatos e das notas | Notebook ou planilha organizada | [integrante a definir] | Cobre as perguntas 1 a 4, com pelo menos 5 gráficos legíveis |
| Visualizações / painel | Gráficos comparativos por renda, tipo de escola e escolaridade dos pais | Imagens e/ou painel simples | [integrante a definir] | Títulos, eixos e legendas claros; fontes citadas |
| Relatório ou apresentação | Texto curto com contexto, método, resultados, limitações e conclusões | PDF e slides | [integrante a definir] | Responde às 5 perguntas, retoma as hipóteses e inclui a seção de limitações |
| Outro: modelo de regressão simples | Modelo com poucas variáveis e interpretação básica (opcional) | Notebook | [integrante a definir] | Variáveis justificadas; o relatório explica o que o modelo não mostra |

## 11. Critérios de sucesso

Defina como a equipe saberá se o projeto alcançou seus objetivos.

| Critério | Indicador ou evidência | Meta | Forma de verificação |
|---|---|---|---|
| Relevância para o problema | Cada pergunta de negócio respondida com gráfico ou tabela | 5 de 5 perguntas respondidas | Conferência da equipe com a lista do item 6 |
| Qualidade dos dados | Tratamentos de valores ausentes e duplicados registrados | 100% das colunas usadas descritas e tratadas | Revisão cruzada entre dois integrantes |
| Qualidade da análise | Hipóteses H1 a H3 testadas e resultados reproduzíveis | 3 de 3 hipóteses com conclusão (confirmada, refutada ou inconclusiva) | Reexecução do código/planilha por outro integrante |
| Utilidade para o público-alvo | Resultados traduzidos em implicações para quem decide | Pelo menos uma implicação prática por pergunta | Feedback do(a) professor(a) ou de um colega fora da equipe |
| Comunicação dos resultados | Relatório e apresentação claros e dentro do prazo | Entregues na data combinada, com limitações explicitadas | Avaliação do(a) professor(a) |

## 12. Plano inicial de trabalho

*Os prazos usam semanas relativas, porque o prazo total ainda não está confirmado.*

| Etapa | Atividades principais | Responsável(is) | Prazo | Dependências |
|---|---|---|---|---|
| 1. Definição | Fechar este documento, rever com o(a) professor(a), distribuir funções | Equipe toda | Semana 1 | Retorno do(a) professor(a) |
| 2. Obtenção dos dados | Baixar a base e o dicionário, ler os termos de uso, definir a edição e a amostra | [a definir] | Semanas 1–2 | Acesso ao portal; espaço no computador |
| 3. Preparação dos dados | Selecionar colunas, tratar vazios e duplicados, criar categorias de renda | [a definir] | Semanas 2–3 | Etapa 2 concluída |
| 4. Análise / modelagem | Análise exploratória, comparação entre grupos, teste das hipóteses, regressão simples (opcional) | [a definir] | Semanas 3–5 | Base tratada |
| 5. Validação | Revisão cruzada dos cálculos e conferência com dados agregados oficiais do INEP | [a definir] | Semana 5 | Resultados da etapa 4 |
| 6. Comunicação | Gráficos finais, relatório, slides e ensaio da apresentação | Equipe toda | Semanas 5–6 | Etapas 4 e 5 |

## 13. Riscos do projeto

| Risco | Probabilidade | Impacto | Estratégia de resposta | Responsável |
|---|---|---|---|---|
| Base muito grande para o computador | Média | Alto | Trabalhar com amostra ou só com as colunas necessárias; testar em um recorte pequeno antes |  |
| Muitos valores ausentes nas variáveis socioeconômicas | Alta | Médio | Definir cedo uma regra clara de tratamento e registrar quantos casos foram excluídos | |
| Pouca experiência da equipe com estatística ou ferramenta de análise | Média | Médio | Manter o modelo simples e opcional; pedir apoio ao(à) professor(a) e treinar em pequenos exemplos |  |

## 14. Organização da equipe

| Integrante | Papel principal | Responsabilidades | Apoio necessário |
|---|---|---|---|
| Pedro Henrique | Coordenação e obtenção dos dados | Organizar prazos, baixar e documentar a base | Orientação sobre os termos de uso |
| Pedro Henrique | Preparação dos dados | Limpeza, tratamento de ausentes, dicionário | Apoio com a ferramenta, se necessário |
| Pedro Henrique | Análise exploratória | Estatísticas descritivas e comparação entre grupos | Revisão de estatística básica |
| Pedro Henrique | Visualizações | Gráficos e painel simples | Orientação sobre boas práticas de gráficos |
| Pedro Henrique | Redação e apresentação | Relatório, slides, revisão de linguagem | Feedback do(a) professor(a) |

## 15. Validação da definição do projeto

Antes da entrega, confirme:

- [x] O problema é real, relevante e delimitado.
- [x] O público-alvo e as partes interessadas estão identificados.
- [x] O objetivo geral e os objetivos específicos são coerentes.
- [x] As perguntas de negócio orientam decisões concretas.
- [x] Há dados potencialmente disponíveis para responder às perguntas.
- [ ] O escopo é compatível com o prazo e os recursos.
- [x] Os critérios de sucesso são mensuráveis.
- [ ] Riscos, privacidade, ética e segurança foram considerados.
- [ ] Funções e responsabilidades foram distribuídas.

## 16. Aprovação e registro de ajustes

| Responsável | Validação / observação | Data |
|---|---|---|
| Representante da equipe | | |
| Professor(a) / orientador(a) | | |

### Ajustes solicitados após a apresentação inicial

________________________________________________________________________________

________________________________________________________________________________

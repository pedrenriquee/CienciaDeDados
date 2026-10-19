<img src="assets/logo-udf.jpg" alt="UDF Centro Universitário" width="230">

**Profa. Kadidja Valéria | UDF**  
Ciência de Dados e Aprendizado de Máquina · Sistemas de Informação · 2026.2

# Aula 1 — Conceitos e classificação de problemas

## Identificação

- Estudante ou equipe: **Pedro Henrique Matos Lopes**
- Turma: **Sistemas de Informação**
- Data de realização: **19/10**
- Integrantes e contribuições (se em equipe): **Pedro Henrique Matos Lopes**

## Objetivos

Distinguir programação tradicional e Machine Learning, identificar atributos e alvo e diferenciar classificação, regressão e agrupamento.

## 1. Explicação com suas palavras

1. Como um modelo aprende com dados? **Um modelo utiliza dados anteriormentes tranformado em informações para analisar-los e observar padrões gerar respostas mais conscientes**
2. Qual diferença entre algoritmo e modelo? **O algoritmo é a forma que o computador vai utilizar pra interpretar os dados, depois de pronto torna-se um modelo pronto para analisar aquele conjunto de dados espercificos**
3. Compare uma regra de bloqueio de palavra com um modelo de spam. **Na regra de bloqueio case alguma afirmação for verdade e cair nessa regra automaticamente vai ser bloqueado, o modelo de spam torna isso mais complexo utilizando o contexto como vários padrões antes de tomar uma decisão**
4. Dê um exemplo de atributo e alvo e defina o momento da previsão. **O exemplo vai ser uma pesquisa sobre evasão escolar, o alvo vai ser se o aluno evadiu ou permanceu. Os atributos vão ser faltas, notas e faltas seguidas o momento da previsão vai ser no final do semestre**

## 2. Quadro comparativo

| Critério | Supervisionado | Não supervisionado |
| --- | --- | --- |
| Presença de alvo no treino | Sim, cada exemplo vem com a resposta fornecida | Não, os dados não tem resposta definida. |
| Pergunta que pode responder | Esse aluno vai evadir ou permanecer | Que grupos ou padrões escondidos existem nesses dados |
| Tipo de saída | Evadiu ou permaneceu | Grupos de alunos parecidos entre si. |
| Tarefas e exemplo | Classificação (prever evasão) e regressão (estimar a nota final). | Agrupar e achar casos fora do padrão |
| Dados necessários | Atributos (faltas, notas, faltas seguidas) | Só os atributos (faltas, nota) sem precisar do rótulo. |
| Forma de avaliação | Verificar se o que o modelo previu foi o que de fato aconteceu | Não tem gabarito, então se olha se os grupos fazem sentido e se um professor ou coordenador consegue interpretar. |
| Limitação | esse metodo é bem trabalhoso de se realizar | Os grupos podem não significar nada útil e não dizem sozinhos quem vai evadir. |

## 3. Situações-problema

Os casos são cenários didáticos. Escolha **pelo menos cinco** e justifique sua classificação pelo significado do alvo ou por sua ausência.

| Caso | Situação-problema |
| --- | --- |
| 1 Educação | Prever evadiu/permaneceu com histórico rotulado de turmas anteriores. | tem alvo, que seria se evadiu ou permaneceu, como á existe histórico de turmas anteriores podemos usar esses dados para atingir o alvo
| 2 Saúde | Estimar o tempo de espera em minutos a partir de registros de atendimento. | o alvo seria o tempo de espera. Supervisionado regressão, o objetivo seria alcançar um valor numerico que seria o target.
| 3 Comércio | Descobrir perfis de compra sem categorias prévias de clientes. | Não tem um alvo espercifico, porque o perfil de clientes podem ser bem diferentes. Não supervisionado já que é o modelo juntar perfis diferentes
| 4 Finanças | Prever inadimplente/adimplente com contratos e desfechos conhecidos. |
| 5 Segurança digital | Distinguir spam/legítima com mensagens já revisadas. | O alvo seria a mensagem ser legitima ou spam. Supervisionado classificação, como as mensagens já foram revisadas então seria pegar os dados da mensagem para o modelo 
| 6 Comércio | Estimar o total de vendas em reais na próxima semana. |
| 7 Educação | Agrupar perfis de acesso ao ambiente virtual sem rótulo de evasão. | Não tem alvo porque não tem um rotulo de evasão. Não supervisionado, agrupamento. Procura padrões de uso do ambiente virtual sem resposta pronta.
| 8 Saúde | Classificar exames em categorias previamente definidas por especialistas. |

| Caso escolhido | Alvo ou ausência de alvo | Categoria, quantidade ou grupos? | Abordagem e justificativa | Dados necessários e limitação |
| --- | --- | --- | --- | --- |
| Educação | Prever evadiu/permaneceu com histórico rotulado de turmas anteriores. | Tem alvo (evadiu ou permaneceu) e histórico para treinar. Supervisionado, classificação.
| Saúde | 	Estimar o tempo de espera em minutos a partir de registros de atendimento. | O alvo é o tempo de espera, um número. Supervisionado, regressão.
| Comércio | Descobrir perfis de compra sem categorias prévias de clientes | Não há alvo, pois não existem categorias prévias. Não supervisionado, agrupamento.
| Segurança digital | digital	Distinguir spam/legítima com mensagens já revisadas. | O alvo é spam ou legítima, e as mensagens revisadas já têm rótulo. Supervisionado, classificação.
| Educação | 	Agrupar perfis de acesso ao ambiente virtual sem rótulo de evasão. | Não há alvo, pois não existe rótulo de evasão. Não supervisionado, agrupamento.

## 4. Raciocínio crítico

“Detectar fraude” define sozinho o tipo de aprendizado? Compare o uso de exemplos rotulados e a busca de operações atípicas sem rótulos. **Não define, pois detectar fraude é o objetivo, para saber se o modelo é supervisionado ou não é ter ou não rotulos nos dados, por exemplo voce pode ter dados legitimos e fraudados e utilizar o modelo pra identificar padrões e conseguir fazer analise corretas posteriomente**

## Entrega

Salve este arquivo preenchido. Critérios: distinção conceitual, pertinência dos dados, justificativa e clareza. [Voltar ao início](README.md).

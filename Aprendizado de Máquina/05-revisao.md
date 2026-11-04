<img src="assets/logo-udf.jpg" alt="UDF Centro Universitário" width="230">

**Profa. Kadidja Valéria | UDF**  
Ciência de Dados e Aprendizado de Máquina · Sistemas de Informação · 2026.2

# Questões de revisão — Registro individual

## Identificação

- Estudante ou equipe: **Pedro Henrique Matos Lopes**
- Turma: **Ciencia de Dados**
- Data de realização: **04/11**
- Integrantes e contribuições (se em equipe): **Pedro Henrique Matos Lopes**

Responda com suas palavras e apresente os cálculos quando solicitados. Os números dos exercícios manuais não são os resultados do laboratório.

## 1. Explique a diferença entre regra programada para bloquear uma palavra e modelo de spam treinado com exemplos.

**Resposta:** Regra programada escreve-se a lógica explícita cobrindo só o que foi previsto. No modelo treinado, o algoritmo aprende a partir de padrões 
## 2. Por que codificar evadiu/permaneceu como 1/0 não transforma classificação em regressão?

**Resposta:** O que define a tarefa é a natureza do alvo, e não os números usados para representá-lo: 1 e 0 apenas identificam categorias, sem noção de distância ou ordem. O modelo segue prevendo uma classe e deve ser medido com métricas de classificação.

## 3. Uma biblioteca quer estimar empréstimos e descobrir perfis. Que tarefas correspondem a cada pergunta?

**Resposta:** Prever o número de empréstimos é regressão (aprendizado supervisionado com alvo numérico). Identificar perfis de leitores, sem categorias definidas de antemão, é agrupamento (clusterização), uma tarefa não supervisionada.

## 4. O que são atributo, alvo e unidade de análise no laboratório educacional?

**Resposta:** Atributos são as informações de entrada do modelo (frequência, notas, horas de estudo); o alvo é a resposta que se deseja prever (evasão ou nota final). A unidade de análise é o elemento que cada linha da tabela descreve, em geral um estudante.

## 5. Por que calcular a mediana antes de dividir os dados pode invalidar a avaliação?

**Resposta:** Isso gera vazamento de dados: ao usar todo o conjunto, a mediana carrega informação do teste para o tratamento do treino, e o desempenho medido fica artificialmente alto. O certo é separar os dados primeiro e obter a mediana apenas do treino.

## 6. Em uma matriz didática com TN=80, FP=5, FN=10, TP=5, calcule acurácia e sensibilidade. O resultado é suficiente para aprovar o modelo?

**Resposta:** Acurácia = (5+80)/100 = 0,85; sensibilidade = 5/(5+10) ≈ 0,33. Não basta: há desbalanceamento de classes e o modelo deixa escapar dois em cada três casos positivos, então convém analisar também precisão, F1 e o custo de cada erro.

## 7. Valores reais 100, 120, 140 e previsões 110, 115, 130. Calcule MAE e informe a unidade se o alvo for vendas em reais.

**Resposta:** Os erros absolutos são 10, 5 e 10, logo MAE = 25/3 ≈ R$ 8,33. Ou seja, a previsão se desvia, em média, R$ 8,33 do valor real, na mesma unidade do alvo.

## 8. Um R² de -0,2 significa “20% de acertos negativos”? Explique.

**Resposta:** Não. O R² compara o desempenho do modelo com o de uma referência que sempre prevê a média; um valor negativo mostra que o modelo é pior do que simplesmente usar a média. Ele não representa percentual de acertos.

## 9. Uma árvore tem acurácia 1,00 no treino e 0,65 na validação. Que hipótese investigar e como?

**Resposta:** A hipótese é de sobreajuste (overfitting): a árvore decorou o treino e não generaliza. Para verificar, variar max_depth e min_samples_leaf, comparar as curvas de treino e validação e aplicar validação cruzada.

## 10. Por que escolher a profundidade pelo teste prejudica a estimativa final?

**Resposta:** Porque o teste passa a influenciar a escolha do modelo, que acaba ajustado a ele, tornando a métrica final otimista. A profundidade deve ser definida por validação ou validação cruzada, reservando o teste para uma única avaliação final.

## 11. Baixa frequência associada à evasão demonstra causa? Proponha explicação alternativa.

**Resposta:** Não, associação não prova causalidade. A baixa frequência pode ser efeito de um desinteresse que já existia, ou ambos podem vir de um fator comum (dificuldade financeira, necessidade de trabalhar, problemas de saúde).

## 12. Um modelo sinaliza um estudante como possível evasão. Que ação responsável pode ser adotada?

**Resposta:** Usar o alerta como indicação para acompanhamento: a equipe pedagógica procura o estudante e oferece apoio (tutoria, auxílio), sem rotulá-lo nem puni-lo. A decisão final cabe a pessoas, lembrando que o modelo pode errar

## Fontes adicionais consultadas

**https://scikit-learn.org/stable/common_pitfalls.html
. https://scikit-learn.org/stable/modules/generated/sklearn.metrics.r2_score
**

[Voltar ao início](README.md).

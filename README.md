analise-diabetes-uci-logistica
Projeto de Classificação de Diabetes usando Regressão Logística e SMOTE no Dataset UCI. 
Projeto de Classificação de Diabetes: Análise e Otimização do UCI Health Indicators

**Trabalho feito para treinamento e estudos na aréa. Utilizei uma IA para me auxiliar e ensinar enquanto fazia o projeto.**

1. Objetivo do Projeto:
  Este projeto consiste na construção de um modelo de Machine Learning (ML) para **prever a presença de Diabetes** (Classificação Binária) em pacientes, utilizando dados de indicadores de saúde do **CDC Diabetes Health Indicators Dataset (UCI)**.  
  Dada a natureza médica do problema, a métrica crítica de sucesso é o **Recall** (Sensibilidade) da classe minoritária (Diabético), visando **minimizar Falsos Negativos** (casos de diabetes perdidos).

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

2. Análise Exploratória de Dados (EDA) e Desafio Principal

 O conjunto de dados inicial, com 253.680 observações e 21 features, apresentou duas características chave:

Qualidade: Não foram encontrados valores faltantes. As features já estavam em formato numérico.
Desafio (Desequilíbrio de Classes): A identificação de um severo desequilíbrio (86% Não Diabético vs. 14% Diabético) levou a um viés no modelo inicial.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

3. Pré-processamento e Estratégia de Otimização

Para preparar os dados e solucionar o viés, foram aplicadas as seguintes técnicas:

Divisão: Dados separados em conjuntos de Treino (70%) e Teste (30%), com estratificação.
Escalonamento: Aplicação do StandardScaler para colocar todas as variáveis na mesma escala.
Balanceamento: Uso do SMOTE (Synthetic Minority Over-sampling Technique)** no *conjunto de treino* para corrigir o desequilíbrio e otimizar o Recall.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------

4. Modelagem e Resultados Finais

O modelo de Regressão Logística foi treinado nos dados balanceados pelo SMOTE.

Resultados Chave do Modelo Otimizado (Conjunto de Teste):

O modelo alcançou um **trade-off estratégico**, trocando Acurácia Geral por Sensibilidade (Recall), o que é ideal para este problema médico.

 Acurácia Geral: *73%  A acurácia geral diminuiu de 86%, mas o modelo é mais honesto. 
Precision (Classe Diabético):31%** Das vezes que o modelo previu diabetes, acertou 31% (aumentamos os Falsos Positivos para ganhar Recall). 
Recall (Classe Diabético):76% O Sucesso do Projeto:** O modelo identifica 76% dos pacientes que realmente têm diabetes. 

Conclusão de Impacto:

O Recall da Classe Diabético saltou de 16% para 76%. O modelo agora tem uma alta capacidade de diagnóstico, reduzindo drasticamente a taxa de Falsos Negativos (casos perdidos). Isso valida a estratégia de balanceamento para problemas onde a detecção da classe minoritária é crítica.[Verifica_versão.ipynb](https://github.com/user-attachments/files/23434282/Verifica_versao.ipynb)

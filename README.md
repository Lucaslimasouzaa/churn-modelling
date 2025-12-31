![Python](https://img.shields.io/badge/Python-blue)
![Jupyter](https://img.shields.io/badge/Jupyter_Notebook-orange)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458)
![Machine Learning](https://img.shields.io/badge/Machine%20learning-3F4F75)
![Status](https://img.shields.io/badge/Status-Concluido-grenn)
# Predição de Churn Bancário com Machine Learning

Este projeto consiste em uma análise preditiva focada na retenção de clientes de uma instituição bancária. O objetivo principal é identificar padrões de comportamento e prever a probabilidade de um cliente deixar o banco (Churn), permitindo a tomada de decisões estratégicas para fidelização.

## 🎯 Objetivo

Desenvolver e comparar modelos de Machine Learning capazes de classificar se um cliente irá encerrar sua conta (Exited = 1) ou permanecer no banco (Exited = 0), com base em dados demográficos, comportamento financeiro e histórico de consumo.

## 🛠 Ferramentas e Tecnologias

* **Linguagem:** Python
* **Manipulação de Dados:** Pandas, NumPy
* **Visualização:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-learn, XGBoost
* **Ambiente:** Jupyter Notebook

## 📊 Metodologia

O projeto foi estruturado nas seguintes etapas:

1. **Análise Exploratória e Pré-processamento:**
    * Tratamento de dados nulos e duplicados.
    * Codificação de variáveis categóricas (Label Encoding para Gênero e One-Hot Encoding para Geografia).
    * Padronização dos dados (StandardScaler) para otimizar a performance dos algoritmos.

2. **Seleção de Modelos (Baseline):**
    * Foram testados diversos algoritmos para estabelecer uma linha de base:
        * Random Forest Classifier
        * Regressão Logística
        * Support Vector Machine (SVC)
        * K-Nearest Neighbors (KNN)
        * XGBoost

3. **Engenharia de Atributos (Feature Engineering):**
    * Criação de novas variáveis para enriquecer o modelo e capturar comportamentos complexos:
        * `BalanceZero`: Indicador binário para saldo zerado.
        * `AgeGroup`: Categorização dos clientes por faixa etária.
        * `BalanceSalaryRatio`: Razão entre saldo bancário e salário estimado.
        * `ProductUsage`: Interação entre número de produtos e atividade do membro.
        * `TenureGroup`: Agrupamento por tempo de permanência.
    * Criação de interações específicas entre Gênero e Geografia.

4. **Avaliação de Desempenho:**
    * Comparação das métricas de Acurácia, Precisão, Recall e F1-Score através da Matriz de Confusão e Relatório de Classificação.

## 📈 Resultados

Após a etapa de engenharia de atributos e refinamento, o modelo **Random Forest** apresentou o melhor desempenho geral, alcançando uma acurácia de aproximadamente **87%**.

A análise de importância das variáveis (*Feature Importance*) destacou que a **Idade (Age)**, o **Salário Estimado (EstimatedSalary)** e a **Pontuação de Crédito (CreditScore)** são os fatores mais determinantes para a previsão do churn neste conjunto de dados.

## 👨‍💻 Créditos

Desenvolvido por **Lucas Lima Souza**.

<a href="https://www.linkedin.com/in/lucaslimasouz" target="_blank">
<img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>

## 📂 Dataset

O conjunto de dados utilizado neste projeto foi retirado do Kaggle:
* [Churn Modelling - Kaggle](https://www.kaggle.com/datasets/shrutimechlearn/churn-modelling)

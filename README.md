# 🏥 Análise e Previsão de Diabetes

**Exploração dos Dados e Otimização de Modelos de Machine Learning (Aprendizado de Máquina)**  
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)  
[![JupyterLab](https://img.shields.io/badge/JupyterLab-Notebook-orange)](https://jupyter.org/)  
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.2.2-green)](https://scikit-learn.org/)  
[![Seaborn](https://img.shields.io/badge/Seaborn-0.11.0-purple)](https://seaborn.pydata.org/)

---

## 🎯 Objetivo  
O presente projeto tem como finalidade desenvolver um **modelo preditivo** robusto para identificar a ocorrência de diabetes com base em dados clínicos e demográficos. A abordagem inclui:  

- **Análise Exploratória de Dados (Exploratory Data Analysis - EDA)**: Entender a distribuição e correlação entre variáveis (ex.: idade, IMC (*Body Mass Index*), níveis de HbA1c e glicose sanguínea).  
- **Preparação de Dados (Data Preparation)**: Aplicação de técnicas de *data wrangling* e *one-hot encoding* para variáveis categóricas (ex.: gênero, histórico de tabagismo).  
- **Treinamento e Otimização de Modelos (Model Training & Optimization)**: Testes iniciais com RandomForestRegressor e, posteriormente, desenvolvimento e ajuste fino com RandomForestClassifier utilizando GridSearchCV para encontrar os melhores hiperparâmetros (*hyperparameters*).

**Destaque para Stakeholders (Parte Interessada):**  
✅ **Habilidades Técnicas**: Análise exploratória, manipulação de dados, machine learning e otimização de modelos.  
✅ **Resultados**: Acurácia inicial de ~96,99% evoluindo para 97,13% após otimização.  

---

## 🛠️ Tecnologias e Dados  
- **Linguagem**: Python  
- **Ambiente**: JupyterLab  
- **Bibliotecas**:  
  - `Pandas` (manipulação de dados)  
  - `Seaborn` (visualizações interativas)  
  - `Matplotlib` (gráficos estáticos)  
  - `Scikit-Learn` (modelos de machine learning)  
- **Dataset**: `diabetes_prediction_dataset.csv` (100k registros com dados clínicos e demográficos)

---

## 📊 Visualizações e Insights  
- **Distribuição das Variáveis**:  
  - Histogramas para variáveis como idade (*age*), IMC (*BMI*) e níveis de HbA1c.  
  - Exemplo visual: ![Histograma](https://via.placeholder.com/500x300.png?text=Histograma)
  
- **Relação entre Indicadores**:  
  - Scatter plot demonstrando a correlação entre níveis de glicose (*blood glucose level*) e HbA1c, diferenciando casos com e sem diabetes.  
  - Exemplo visual: ![Scatter Plot](https://via.placeholder.com/500x300.png?text=Scatter+Plot)
  
- **Insights Relevantes**:  
  - A forte correlação entre níveis de HbA1c e ocorrência de diabetes.  
  - Identificação de padrões demográficos que influenciam o risco de diabetes.

---

## 🤖 Modelos de Machine Learning  
### 1. Modelos Iniciais e Testes  
- **RandomForestRegressor**: Testado para validação de abordagens, mas não ideal para a natureza classificatória do problema.

### 2. Classificação com RandomForestClassifier  
- **Treinamento**: Divisão dos dados em treino e teste com *train_test_split* (70% treino, 30% teste).  
- **Métricas**:  
  - Acurácia de ~96,99% no modelo inicial.  
  - Avaliação via *cross validation* e cálculo do RMSE para insights quantitativos.  

### 3. Otimização do Modelo  
- **GridSearchCV**:  
  - Parâmetros ajustados: `n_estimators`, `max_depth`, `min_samples_split`, `min_samples_leaf`, `max_features` e `bootstrap`.  
  - Resultado: Modelo otimizado com hiperparâmetros que elevaram a acurácia para 97,13%.
- **Análise ROC (Receiver Operating Characteristic)**:  
  - Geração da curva ROC e cálculo da AUC (*Area Under the Curve*) para avaliação da performance do classificador.

---

## 🚀 Conclusão  
A abordagem adotada resultou em um modelo preditivo de alta assertividade para a previsão de diabetes. Os principais pontos estratégicos incluem:  

- **Feature Importance**: A influência marcante dos níveis de HbA1c e glicose no diagnóstico.  
- **Model Optimization**: Uso de GridSearchCV para afinar os parâmetros e melhorar a performance do modelo.  
- **Aplicações Corporativas**:  
  - Suporte à tomada de decisão em saúde (healthcare decision-making).  
  - Possibilidade de integração com sistemas de monitoramento e prevenção de doenças.

---

## 🏗 Melhorias Futuras  
- Investigar modelos avançados como **XGBoost (eXtreme Gradient Boosting)** e **LightGBM (Light Gradient Boosting Machine)**.  
- Refinar técnicas de *feature engineering* para melhor captação dos sinais clínicos.  
- Desenvolver um *dashboard* interativo para monitoramento em tempo real dos indicadores preditivos.

---

## 📬 Contato  
🔗 **GitHub:** [LeonardoMartinho](https://github.com/LeonardoMartinho)  
📧 **Email:** leonardomartinhopro@email.com  
💼 **LinkedIn:** [Leonardo Martinho](https://www.linkedin.com/in/leonardoapmartinho/)

⭐ **Dê uma estrela no projeto se achar útil!** 🚀

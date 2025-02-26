# 🩺 Previsão de Diabetes com Machine Learning

**Análise e Modelagem Preditiva para Diagnóstico de Diabetes**  

<p>
  <img src="https://img.shields.io/badge/Python-3.8%2B-blue" alt="Python">  
  <img src="https://img.shields.io/badge/JupyterLab-Notebook-orange" alt="JupyterLab">  
  <img src="https://img.shields.io/badge/Scikit--Learn-1.2.2-green" alt="Scikit-Learn">  
  <img src="https://img.shields.io/badge/Seaborn-0.11.0-purple" alt="Seaborn">  
  <img src="https://img.shields.io/badge/Plotly-5.10.0-purple" alt="Plotly">  
</p>

---

## 🎯 Objetivo  
O presente projeto tem como finalidade desenvolver um **modelo preditivo** robusto para identificar a ocorrência de diabetes com base em dados clínicos e demográficos. A abordagem inclui:  

- **Análise Exploratória de Dados (Exploratory Data Analysis - EDA)**: Entender a distribuição e correlação entre variáveis (ex.: idade, IMC (*Body Mass Index*), níveis de HbA1c e glicose sanguínea).  
- **Preparação de Dados (Data Preparation)**: Aplicação de técnicas de *data wrangling* e *one-hot encoding* para variáveis categóricas (ex.: gênero, histórico de tabagismo).  
- **Treinamento e Otimização de Modelos (Model Training & Optimization)**: Testes iniciais com RandomForestRegressor e, posteriormente, desenvolvimento e ajuste fino com RandomForestClassifier utilizando GridSearchCV para encontrar os melhores hiperparâmetros (*hyperparameters*).

**Destaque para Stakeholders:**  
✅ **Habilidades Técnicas**: Análise exploratória, manipulação de dados, machine learning e otimização de modelos.  
✅ **Resultados**: Acurácia inicial de ~96,99% evoluindo para 97,13% após otimização.  

---

## 🛠️ Tecnologias e Dados  
- **Linguagem**: Python  
- **Ambiente**: JupyterLab  
- **Bibliotecas**:  
  - `Pandas` (manipulação de dados)  
  - `Seaborn` e `Matplotlib` (visualizações estáticas).
  - `Plotly` (gráficos interativos).
  - `Scikit-Learn` (modelos de machine learning)  
- **Dataset**: `diabetes_prediction_dataset.csv` (100k registros com dados clínicos e demográficos)

---

## 📊 **Visualizações e Análises Principais**  

### 🔍 **Correlação entre Variáveis**  
📌 **Ferramenta:** `Seaborn`  
📌 **Descrição:** Heatmap de correlação destacando variáveis como `blood_glucose_level` e `HbA1c_level` como as mais relacionadas ao diabetes.  
📌 **Insight:** Glicemia elevada e níveis de HbA1c acima de 6.5 são indicadores críticos.  

![Heatmap de Correlação](https://github.com/user-attachments/assets/7a50c69d-eec3-4fb1-95c2-b80aa5f3f1c2)  

**Padrões Identificados**:  
- 🔴 **Glicemia > 200 mg/dL**: Associada a 85% dos casos positivos.  
- 🟡 **Idade > 60 anos**: Aumenta em 2x o risco de diabetes.  

---

### 📈 **Relação entre Glicemia e HbA1c**  
📌 **Ferramenta:** `Plotly`  
📌 **Descrição:** Gráfico de dispersão interativo com cores diferenciando diagnósticos positivos (1) e negativos (0).  
📌 **Insight:** Pacientes com diabetes tendem a se agrupar na região superior direita (glicemia e HbA1c elevados).  

![Scatter Plot Interativo](https://github.com/user-attachments/assets/0ac920b6-c8fe-4673-95dc-9f237b683d39)

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

## 🚀 **Conclusão**  

O modelo **Random Forest otimizado** mostrou alta performance, com **AUC-ROC de 0.96**, indicando excelente capacidade de discriminar entre pacientes diabéticos e não diabéticos. Principais achados:  
- **Variáveis-chave**: `blood_glucose_level`, `HbA1c_level` e `age` são os principais preditores.  
- **Impacto clínico**: O modelo pode auxiliar na triagem precoce de pacientes de alto risco.  

**Aplicações Práticas**:  
- Integração em sistemas de saúde para alertas preventivos.  
- Redução de custos com diagnósticos tardios. 

---

## 🏗 Melhorias Futuras  
- ✅Investigar modelos avançados como **XGBoost (eXtreme Gradient Boosting)** e **LightGBM (Light Gradient Boosting Machine)**.  
- ✅Refinar técnicas de *feature engineering* para melhor captação dos sinais clínicos.  
- ✅Desenvolver um *dashboard* interativo para monitoramento em tempo real dos indicadores preditivos.

---

## 📬 Contato  
🔗 **GitHub:** [LeonardoMartinho](https://github.com/LeonardoMartinho)  
📧 **Email:** leonardomartinhopro@email.com  
💼 **LinkedIn:** [Leonardo Martinho](https://www.linkedin.com/in/leonardoapmartinho/)

⭐ **Dê uma estrela no projeto se achar útil!** 🚀

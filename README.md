# 🚗 Predição de Preços de Carros Usados com Machine Learning  

Este projeto tem como objetivo prever o valor de carros usados com base em características como **marca, ano de fabricação, tipo de combustível, quilometragem**, entre outros. Foram exploradas diferentes técnicas de **Machine Learning** para treinar e avaliar modelos, identificando a melhor abordagem para a estimativa de preços.  

## 📊 Visão Geral  

O pipeline do projeto inclui:  
✔ **Exploração e limpeza dos dados**  
✔ **Análise exploratória e visualização de dados**  
✔ **Feature engineering e seleção de variáveis mais relevantes**  
✔ **Pré-processamento de dados com codificação e normalização**  
✔ **Treinamento e avaliação de 5 modelos de Machine Learning**  
✔ **Comparação de desempenho entre os modelos usando métricas de erro**  
✔ **Otimização de hiperparâmetros com GridSearchCV**  

## 🔧 Tecnologias Utilizadas  

- **Linguagem**: Python  
- **Bibliotecas**:  
  - Manipulação de Dados: `pandas`, `numpy`  
  - Visualização: `matplotlib`, `seaborn`  
  - Modelagem: `scikit-learn`  
  - Pipeline de pré-processamento: `ColumnTransformer`, `StandardScaler`, `OneHotEncoder`  
  - Seleção de atributos: `mutual_info_regression`  
  - Validação e Otimização: `GridSearchCV`, `cross_val_score`  

## 📂 Dataset  

O conjunto de dados foi obtido no **Kaggle** e contém informações detalhadas sobre veículos, incluindo:  
- **Price** (variável alvo)  
- **Manufacturer** e **Model**  
- **Prod. year** (Ano de fabricação)  
- **Category** (Jeep, Hatchback, etc.)  
- **Fuel type** (Petrol, Hybrid, etc.)  
- **Engine volume**, **Mileage**, **Cylinders**, **Airbags**  
- **Gear box type**, **Drive wheels**, **Color**  

📌 O dataset possui **19.237 registros** e foi dividido em **80% para treino e 20% para teste**.  

## 🔍 Análise Exploratória e Feature Engineering  

- **Remoção de colunas irrelevantes** como ID.  
- **Conversão de valores categóricos** em numéricos.  
- **Tratamento de valores ausentes e outliers**.  
- **Estratificação do dataset** com base no preço dos carros.  
- **Análise de correlação e importância das features** usando **Matriz de Correlação** e **Informação Mútua**.  
- **Criação de novas features** para melhorar o desempenho dos modelos.  

## 🏆 Modelos Treinados  

Foram testados **5 modelos de regressão** para prever o preço dos carros:  

1️⃣ **Regressão Linear** 📈  
2️⃣ **Árvore de Decisão (Decision Tree Regressor)** 🌳  
3️⃣ **Random Forest Regressor** 🌲🌲  
4️⃣ **Gradient Boosting Regressor** 🚀  
5️⃣ **K-Nearest Neighbors (KNN) Regressor** 🤖  

Cada modelo foi avaliado com **Validação Cruzada (cross-validation)** e métricas como:  
✔ **MAE** (Erro Médio Absoluto)  
✔ **RMSE** (Raiz do Erro Quadrático Médio)  
✔ **R² Score** (Coeficiente de Determinação)  

Os resultados foram otimizados usando **GridSearchCV** para encontrar os melhores hiperparâmetros.  

## 📈 Resultados  

Os modelos foram comparados em relação ao erro na predição do preço dos carros. Gráficos de **barplot** e **heatmaps** foram gerados para visualizar o desempenho de cada modelo.  

Os melhores modelos identificados foram:  
✅ **Gradient Boosting Regressor** – Melhor desempenho geral com menor erro de previsão.  
✅ **Random Forest Regressor** – Modelo robusto e eficiente.  

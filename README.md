#  Identificação de Ataques DDoS com Machine Learning (PT)

## Descrição
Este projeto tem como objetivo a identificação de ataques DDoS (Distributed Denial of Service) utilizando algoritmos de machine learning. Através da análise da base de dados NSL-KDD, o projeto emprega várias técnicas de pré-processamento, engenharia de recursos e modelagem preditiva para detectar e classificar tipos de ataques na rede.

## Configuração do Ambiente
Para executar este projeto, você precisará de Python e das seguintes bibliotecas:

- pandas
- sklearn
- numpy
- seaborn
- matplotlib

## Estrutura do Projeto
O projeto segue as seguintes etapas principais:

### 1. Importação de Bibliotecas e Carregamento de Dados
O primeiro passo inclui a importação das bibliotecas necessárias e o carregamento dos dados da base [NSL-KDD](https://www.kaggle.com/datasets/hassan06/nslkdd).

### 2. Análise Exploratória de Dados
Realizamos a verificação das características das colunas, incluindo a identificação de colunas categóricas e numéricas, análise de valores faltantes, e análise de correlação entre as variáveis.

### 3. Pré-processamento e Engenharia de Recursos
Nesta etapa, as labels de ataques específicos são substituídas por categorias gerais (Normal, DoS, Privilege, Probe, Access). Também realizamos a divisão dos dados em conjuntos de treino e validação usando train_test_split.

### 4. Treinamento dos Modelos
Utilizamos diferentes modelos de machine learning para treinar sobre os dados:

- RandomForest
- LogisticRegression
- KMeans
- MLPClassifier
- SVC

Os modelos são treinados em quatro subconjuntos de dados distintos:

- Base Completa
- Base sem colunas com correlação redundante
- Base apenas com colunas de alta correlação com a coluna target
- Base PCA (Análise de Componentes Principais)

### 5. Avaliação dos Modelos
Os modelos são avaliados usando as métricas de Accuracia, Precisão, Recall e F1-score para determinar seu desempenho na identificação de diferentes tipos de ataques.

---

# DDoS Attacks Identification with Machine Learning (EN)

## Description
This project aims to identify DDoS (Distributed Denial of Service) attacks using machine learning algorithms. Through the analysis of the NSL-KDD database, the project employs various pre-processing, feature engineering and predictive modeling techniques to detect and classify types of attacks on the network.

## Environment Setting
To run this project, you will need Python and the following libraries:

- pandas
- sklearn
- numpy
- seaborn
- matplotlib

## Project Structure
The project follows the following main steps:

### 1. Importing Libraries and Loading Data
The first step includes importing the necessary libraries and loading the data from the [NSL-KDD](https://www.kaggle.com/datasets/hassan06/nslkdd) database.

### 2. Exploratory Data Analysis
We check the characteristics of the columns, including the identification of categorical and numeric columns, analysis of missing values, and correlation analysis between variables.

### 3. Preprocessing and Feature Engineering
At this stage, specific attack labels are replaced by general categories (Normal, DoS, Privilege, Probe, Access). We also split the data into training and validation sets using train_test_split.

### 4. Model Training
We use different machine learning models to train on the data:

- RandomForest
- LogisticRegression
- KMeans
- MLPClassifier
- SVC

Models are trained on four distinct data subsets:

- Complete Base
- Columnless database with redundant correlation
- Base only with columns with high correlation with the target column
- Base PCA (Principal Component Analysis)

### 5. Model Assessment
The models are evaluated using Accuracy, Precision, Recall and F1-score metrics to determine their performance in identifying different types of attacks.

# ✈️ Tech Challenge 3: Análise e Previsão de Atrasos Aéreos

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-150458?style=for-the-badge&logo=pandas)
![Scikit-Learn](https://img.shields.io/badge/Scikit_Learn-Machine_Learning-orange?style=for-the-badge&logo=scikit-learn)
![XGBoost](https://img.shields.io/badge/XGBoost-Gradient_Boosting-red?style=for-the-badge&logo=xgboost)

Este repositório contém a solução para o **Tech Challenge 3**, focado na análise massiva de dados do setor aéreo (`flights.csv`). O projeto é dividido em duas frentes estratégicas: **Classificação de Atrasos** (Previsão) e **Clusterização de Aeroportos** (Perfilamento).

---

## 🧠 O Que Tem Neste Projeto?

### Parte 1: Classificação e Análise Exploratória
O objetivo aqui é entender o comportamento dos atrasos e criar um modelo capaz de prever se um voo terá atraso significativo na chegada (> 10 min).

* **📊 EDA (Análise Exploratória):**
    * Identificação dos **Top 10 Aeroportos Críticos** com maiores médias de atraso.
    * **Heatmap Temporal:** Cruzamento de *Dia da Semana x Horário* para identificar janelas de congestionamento.
* **🤖 Modelagem (XGBoost):**
    * Tratamento de desbalanceamento de classes (`scale_pos_weight`).
    * Previsão de atrasos com alta precisão.
    * Análise de **Feature Importance** para entender o que mais causa atrasos.

### Parte 2: Clusterização de Aeroportos
O objetivo é agrupar aeroportos com comportamentos semelhantes para tomada de decisão estratégica.

* **📉 Redução de Dimensionalidade (PCA):**
    * Compressão de múltiplas variáveis (Atraso na saída, Taxiamento, Segurança, Clima, etc.) em 2 componentes principais para visualização clara.
* **🧩 K-Means Clustering:**
    * Segmentação dos aeroportos em 4 perfis distintos (clusters).
    * Visualização gráfica da separação dos grupos.

---

## 📂 Estrutura do Projeto

```plaintext
📁 tech-challenge-3
│
├── 📜 README.md              # Documentação do projeto
├── 📓 parte_1_classificacao.ipynb  # Notebook com EDA e XGBoost
├── 📓 parte_2_clusterizacao.ipynb  # Notebook com PCA e K-Means
└── 💾 flights.csv            # Dataset (não incluído no repo devido ao tamanho)


🚀 Como Rodar
Pré-requisitos
Certifique-se de ter as seguintes bibliotecas instaladas:

pip install pandas seaborn matplotlib scikit-learn xgboost

Execução
Dataset: Baixe o arquivo flights.csv (Kaggle 2015 Flight Delays) e coloque na raiz do projeto.

Notebooks: Você pode rodar os arquivos .ipynb localmente via Jupyter Notebook, VS Code ou subir para o Google Colab.

📊 Insights Visuais
1. Mapa de Calor de Atrasos
O código gera um heatmap que revela os piores horários para voar. Geralmente, voos no final da tarde/início da noite de sextas-feiras apresentam maior latência.

2. Clusterização com PCA
Através da técnica de PCA aplicada antes do K-Means, conseguimos uma separação visual perfeita dos perfis de aeroportos, facilitando a identificação de hubs eficientes versus aeroportos problemáticos.

🛠️ Tecnologias Utilizadas
Linguagem: Python

Manipulação de Dados: Pandas, NumPy

Visualização: Seaborn, Matplotlib

Machine Learning: Scikit-Learn (KMeans, PCA, Encoders), XGBoost

Ambiente: Google Colab / Jupyter

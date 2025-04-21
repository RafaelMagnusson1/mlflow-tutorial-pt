# Tutorial de MLflow 🚀

Este repositório contém um tutorial introdutório sobre o uso do **MLflow**, uma plataforma de código aberto para gerenciamento de ciclo de vida de Machine Learning. O objetivo é ajudar profissionais de ciência de dados e MLOps a entenderem como rastrear experimentos, registrar modelos e organizar projetos de ML de forma reprodutível e escalável.

## Objetivo do Projeto 🎯

O objetivo deste projeto é demonstrar, passo a passo, como utilizar o **MLflow** para:

- Rastrear experimentos com diferentes parâmetros e métricas.
- Salvar artefatos e versões de modelos treinados.
- Reproduzir execuções e facilitar o compartilhamento de resultados.
- Implementar uma pipeline básica com registro de modelo e deployment local.

Ao final do tutorial, você será capaz de:

✅ Registrar e versionar modelos automaticamente  
✅ Comparar execuções de modelos e métricas de avaliação  
✅ Servir modelos treinados com MLflow Models  
✅ Integrar MLflow com bibliotecas como `scikit-learn`, `pandas` e `matplotlib`

---

## Conceitos Fundamentais 🧠

### 🔬 Experimentos

Um **experimento** é uma coleção de execuções (runs) que compartilham um objetivo comum. É possível usar experimentos para organizar seus testes, comparando diferentes abordagens ou hiperparâmetros.

### 🏃 Runs

Cada **run** representa uma execução individual de código com parâmetros, métricas e artefatos registrados. O MLflow permite comparar runs visualmente na interface.

### ⚙️ Componentes do MLflow

O MLflow possui quatro componentes principais:

| Componente       | Função                                                                 |
|------------------|------------------------------------------------------------------------|
| **Tracking**     | Registro de execuções, parâmetros, métricas, artefatos e modelos       |
| **Projects**     | Empacotamento de código de ML em formato reutilizável (com `MLproject`)|
| **Models**       | Padronização e deployment de modelos treinados                         |
| **Registry**     | Repositório central para versionamento, aprovação e staging de modelos |

### 🧪 Parâmetros e Métricas

Você pode logar:

- **Parâmetros** (`mlflow.log_param`) — hiperparâmetros usados no treinamento  
- **Métricas** (`mlflow.log_metric`) — acurácia, erro, F1-score etc.  
- **Artefatos** (`mlflow.log_artifact`) — gráficos, arquivos de texto, modelos salvos

---

## Pré-requisitos 📦

- Python 3.8+
- MLflow (`pip install mlflow`)
- Scikit-learn, Pandas, Matplotlib (dependendo dos notebooks)

---

## Estrutura do Projeto 📁

A estrutura de diretórios sugerida para este tutorial é a seguinte:

```
mlflow-tutorial/
├── data/                  # Dados de entrada (CSV, etc.)
│   └── example_data.csv
├── notebooks/             # Tutoriais em Jupyter Notebook
│   └── 01_mlflow_intro.ipynb
├── src/                   # Scripts auxiliares e código reutilizável
│   ├── train_model.py     # Script com treinamento e logging
│   └── utils.py           # Funções auxiliares
├── models/                # Modelos salvos (opcional)
├── mlruns/                # Diretório gerado automaticamente pelo MLflow
├── requirements.txt       # Dependências do projeto
├── MLproject              # (Opcional) Arquivo para MLflow Projects
├── README.md              # Este arquivo
└── .gitignore             # Ignorar arquivos temporários
```

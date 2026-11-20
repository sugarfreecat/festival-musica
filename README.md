<div align="center">

# 🎵 Festival de Música — Sales Data Analysis

**Exploratory Data Analysis of a fictional music festival's ticket sales**

[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Status](https://img.shields.io/badge/Project-In_Progress-orange)](#project-status)
[![License](https://img.shields.io/badge/License-MIT-lightgrey)](LICENSE)

</div>

---

<details open>
<summary><strong>🇺🇸 English</strong></summary>

## Overview

This ongoing data analytics project explores ticket sales data from a fictional music festival. The goal is to turn raw data into business-oriented insights that can support decisions about event programming, ticket allocation, revenue opportunities, and marketing priorities.

The analysis combines sales records with attraction-level information to investigate sales volume, revenue, ticket prices, and patterns across ticket types and music genres.

> **Data disclaimer:** The datasets used in this project are fictional and intended for learning, experimentation, and portfolio demonstration. Findings should not be interpreted as real-world market results.

## Business Question

**Which music genres and ticket types generate the highest sales volume and revenue?**

The analysis aims to support decisions such as:
- Prioritizing music genres when planning event programming and investments.
- Understanding the performance of different ticket categories.
- Identifying ticket categories that lead in sales volume, average ticket value, or revenue.
- Informing marketing and ticket-allocation strategies.

## Project Workflow

1. **Data ingestion** — load datasets and transfer them to Google Sheets for storage and validation.
2. **Data inspection** — review schemas, data types, missing values, duplicates, and key relationships.
3. **Exploratory analysis** — calculate descriptive statistics and compare sales across ticket categories and music genres.
4. **Distribution analysis** — examine skewness, percentiles, value ranges, and potential outliers.
5. **Visualization & interpretation** — use charts to communicate findings.
6. **Business recommendations** — translate analytical results into practical recommendations and document limitations.

## Repository Structure

```text
festival-musica/
├── data/
│   ├── raw/                 # Original datasets
│   └── processed/            # Cleaned / analysis-ready datasets
├── ingestion/
│   └── data_ingestion.ipynb # Data generation, upload and validation workflow
├── notebooks/
│   └── 01_analise_exploratoria_vendas.ipynb
│                               # Ticket-sales exploratory analysis
└── README.md
```

## Notebooks

| Notebook | Description |
|---|---|
| [`ingestion/data_ingestion.ipynb`](ingestion/data_ingestion.ipynb) | Connects to Google Sheets, prepares fictional attraction records, uploads CSV datasets in batches, and validates row counts and column headers. |
| [`notebooks/01_analise_exploratoria_vendas.ipynb`](notebooks/01_analise_exploratoria_vendas.ipynb) | Inspects the datasets, checks data quality and relationships, explores ticket-sale values and compares ticket types and music genres using descriptive statistics and charts. |

## Analysis Topics

- Data types, missing values, duplicate records, and foreign-key consistency.
- Descriptive statistics: count, mean, median, standard deviation, minimum, maximum, and quantiles.
- Sales volume and revenue by ticket type and music genre.
- Ticket-price distribution, skewness, and outlier assessment using the IQR rule.
- Visual exploration with histograms, boxplots, and categorical bar charts.
- Business-oriented interpretation and recommendations.

## Tech Stack

- **Python** — analysis and data preparation
- **Pandas** — data manipulation and aggregation
- **NumPy** — numerical operations
- **Matplotlib & Seaborn** — visualization
- **Jupyter Notebook / Google Colab** — interactive analysis
- **gspread** — Google Sheets integration
- **Faker** — fictional data generation

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/sugarfreecat/festival-musica.git
cd festival-musica
```

### 2. Set up a Python environment

```bash
python -m venv .venv
```

Activate it:

```bash
# Windows
.venv\Scripts\activate

# macOS / Linux
source .venv/bin/activate
```

### 3. Install dependencies

Install the libraries used in the notebooks:

```bash
pip install pandas numpy matplotlib seaborn jupyter gspread faker
```

### 4. Run the notebooks

Start Jupyter:

```bash
jupyter notebook
```

You can also open the notebooks in Google Colab using the **Open in Colab** links embedded in each notebook.

> Some ingestion steps use Google Colab Secrets and Google Sheets credentials. Set up your own credentials and spreadsheet ID before running those cells. Do not commit service-account credentials, tokens, or secret files to this repository.

## Data

The `data/` directory is intended to separate data by lifecycle:

- `raw/` — source files as received or generated, kept as close to their original form as possible.
- `processed/` — data prepared for analysis, with transformations applied where needed.

The notebooks currently use CSV datasets for attractions and ticket sales. Data files and credentials are not included in the repository.

## Project Status

🚧 **In progress**

The project is being developed iteratively. Notebook contents, analytical questions, visualizations, and recommendations may change as the analysis evolves.

## Limitations

- The datasets are fictional and do not represent actual festival transactions or audience behavior.
- Sales performance is analyzed without accounting for event frequency or ticket-category availability, unless those factors are incorporated in a future iteration.
- Outlier flags are treated as analytical signals, not automatic errors; values are assessed in context before deciding whether to exclude them.

## Author

**Giovanna Simões**  
[GitHub — sugarfreecat](https://github.com/sugarfreecat)

</details>

<details>
<summary><strong>🇧🇷 Português</strong></summary>

## Visão Geral

Este projeto de análise de dados, ainda em desenvolvimento, explora dados de vendas de ingressos de um festival de música fictício. O objetivo é transformar dados brutos em insights orientados ao negócio que apoiem decisões sobre programação de eventos, distribuição de ingressos, oportunidades de faturamento e prioridades de marketing.

A análise combina registros de vendas com informações sobre atrações para investigar volume de vendas, faturamento, valores de ingressos e padrões por tipo de ingresso e gênero musical.

> **Aviso sobre os dados:** As bases utilizadas são fictícias e têm finalidade educacional, de experimentação e demonstração de portfólio. Os resultados não devem ser interpretados como dados reais de mercado.

## Pergunta de Negócio

**Quais gêneros musicais e tipos de ingresso apresentam maior volume de vendas e faturamento?**

A análise busca apoiar decisões como:
- Priorizar gêneros musicais no planejamento da programação e dos investimentos.
- Compreender o desempenho de diferentes categorias de ingresso.
- Identificar categorias que se destacam em volume de vendas, valor médio por ingresso ou faturamento.
- Orientar estratégias de marketing e alocação de ingressos.

## Fluxo do Projeto

1. **Ingestão de dados** — carregar as bases e transferi-las para o Google Sheets para armazenamento e validação.
2. **Inspeção dos dados** — verificar estrutura, tipos de dados, valores ausentes, duplicatas e relacionamentos entre tabelas.
3. **Análise exploratória** — calcular estatísticas descritivas e comparar vendas por tipo de ingresso e gênero musical.
4. **Análise de distribuição** — avaliar assimetria, percentis, faixas de valores e possíveis outliers.
5. **Visualização e interpretação** — utilizar gráficos para comunicar os resultados.
6. **Recomendações de negócio** — transformar os resultados analíticos em recomendações práticas e documentar limitações.

## Estrutura do Repositório

```text
festival-musica/
├── data/
│   ├── raw/                  # Dados originais
│   └── processed/             # Dados tratados / prontos para análise
├── ingestion/
│   └── data_ingestion.ipynb  # Fluxo de geração, envio e validação de dados
├── notebooks/
│   └── 01_analise_exploratoria_vendas.ipynb
│                               # Análise exploratória de vendas de ingressos
└── README.md
```

## Notebooks

| Notebook | Descrição |
|---|---|
| [`ingestion/data_ingestion.ipynb`](ingestion/data_ingestion.ipynb) | Conecta ao Google Sheets, prepara registros fictícios de atrações, envia bases CSV em lotes e valida quantidade de linhas e cabeçalhos. |
| [`notebooks/01_analise_exploratoria_vendas.ipynb`](notebooks/01_analise_exploratoria_vendas.ipynb) | Inspeciona as bases, verifica qualidade e relacionamentos, explora valores de venda e compara tipos de ingresso e gêneros musicais com estatísticas descritivas e gráficos. |

## Tópicos de Análise

- Tipos de dados, valores ausentes, registros duplicados e consistência de chaves estrangeiras.
- Estatística descritiva: contagem, média, mediana, desvio padrão, mínimo, máximo e quantis.
- Volume de vendas e faturamento por tipo de ingresso e gênero musical.
- Distribuição dos valores de ingresso, assimetria e avaliação de outliers pela regra do IQR.
- Exploração visual com histogramas, boxplots e gráficos de barras categóricos.
- Interpretação orientada ao negócio e recomendações.

## Tecnologias

- **Python** — análise e preparação de dados
- **Pandas** — manipulação e agregação de dados
- **NumPy** — operações numéricas
- **Matplotlib & Seaborn** — visualização de dados
- **Jupyter Notebook / Google Colab** — análise interativa
- **gspread** — integração com Google Sheets
- **Faker** — geração de dados fictícios

## Como Executar

### 1. Clone o repositório

```bash
git clone https://github.com/sugarfreecat/festival-musica.git
cd festival-musica
```

### 2. Configure um ambiente Python

```bash
python -m venv .venv
```

Ative o ambiente:

```bash
# Windows
.venv\Scripts\activate

# macOS / Linux
source .venv/bin/activate
```

### 3. Instale as dependências

Instale as bibliotecas utilizadas nos notebooks:

```bash
pip install pandas numpy matplotlib seaborn jupyter gspread faker
```

### 4. Execute os notebooks

Inicie o Jupyter:

```bash
jupyter notebook
```

Também é possível abrir os notebooks no Google Colab pelos links **Open in Colab** incluídos em cada notebook.

> Algumas etapas de ingestão utilizam Secrets do Google Colab e credenciais do Google Sheets. Configure suas próprias credenciais e o ID da planilha antes de executar essas células. Não envie credenciais de service account, tokens ou arquivos secretos para o repositório.

## Dados

A pasta `data/` foi organizada para separar os dados por etapa do ciclo de vida:

- `raw/` — arquivos de origem, recebidos ou gerados, mantidos o mais próximo possível do formato original.
- `processed/` — dados preparados para análise, após eventuais transformações.

Os notebooks utilizam arquivos CSV para as bases de atrações e vendas de ingressos. Os arquivos de dados e credenciais não estão incluídos no repositório.

## Status do Projeto

🚧 **Em desenvolvimento**

O projeto está sendo construído de forma iterativa. Os notebooks, perguntas analíticas, visualizações e recomendações podem mudar à medida que a análise evolui.

## Limitações

- Os dados são fictícios e não representam transações reais nem o comportamento real de públicos de festivais.
- O desempenho das vendas é analisado sem considerar a frequência dos eventos ou a disponibilidade de cada categoria de ingresso, a menos que esses fatores sejam incorporados em uma etapa futura.
- Outliers são tratados como sinais para investigação, não como erros automáticos; sua exclusão depende de avaliação contextual.

## Autora

**Giovanna Simões**  
[GitHub — sugarfreecat](https://github.com/sugarfreecat)

</details>

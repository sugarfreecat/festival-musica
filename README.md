## 🇧🇷 Português

### Sobre o Projeto
Este projeto implementa e automatiza um pipeline de ingestão, transformação e validação de dados para o banco de dados de eventos do **Festival Gatitos** (contendo as tabelas de `atrações` e `ingressos vendidos`). Utilizando a linguagem **Python**, a biblioteca **Pandas** para manipulação de dados e a biblioteca **gspread** integrada à API do Google Sheets/Drive, o sistema ingere com segurança mais de 65.000 registros na nuvem.

### 🚀 Principais Destaques

* **Ingestão Baseada em Lotes (Batch Uploading & API Resilience):** Como o volume total supera 65.000 registros, um upload direto causaria interrupções devido aos limites de taxa da API da Google (*rate limiting*). Desenvolvi um algoritmo de fracionamento em lotes (*chunking*) estruturado que gerencia dinamicamente o tráfego de rede e insere pausas inteligentes (`time.sleep`) para garantir a estabilidade do processo de ingestão.
* **Autenticação Segura e SecOps (IAM):** A integração com serviços do Google Cloud Platform (GCP) é estabelecida usando Contas de Serviço (*Service Accounts*). As chaves de acesso são manipuladas de forma restrita através do gerenciador de segredos nativo do ambiente (`google.colab.userdata`), evitando a prática insegura de expor credenciais diretamente no código-fonte.
* **Processamento e Tratamento de Dados (Pandas ETL):** Processamento eficiente de tipos de dados heterogêneos. Datas e horas nativas são padronizadas para strings compatíveis com as especificações da API Sheets, e valores ausentes (`NaN`) são devidamente preenchidos para manter a fidelidade e consistência analítica.
* **Garantia de Qualidade de Dados (Data Quality & Automation):** O fluxo é finalizado com rotinas de testes automatizados (`assert`) que comparam de forma rigorosa as assinaturas dos cabeçalhos das tabelas enviadas com o que foi fisicamente gravado no Google Sheets, assegurando que o volume de registros esteja 100% íntegro.

---

## 🇺🇸 English

### About the Project
This project implements and automates a professional data ingestion, transformation, and validation pipeline for the **Festival Gatitos** database (housing the `attractions` and `ticket sales` tables). Powered by **Python**, **Pandas** for data wrangling, and the **gspread** library connected to the Google Sheets/Drive APIs, this system safely synchronizes and validates over 65,000 live cloud records.

### 🚀 Key Highlights

* **Batch Data Ingestion & API Resilience:** Ingesting over 65k rows directly risks throttling by Google's strict API rate limits. To overcome this infrastructure barrier, the pipeline features a custom batching algorithm that partitions data into manageable chunks, applying regulated pauses (`time.sleep`) to keep the ingestion flow reliable and error-free.
* **Secure Authentication & Cloud SecOps (IAM):** Connection to Google Cloud services is established using a private Service Account. Access keys are safely fetched through the environment's native secrets manager (`google.colab.userdata`), eliminating hardcoded credentials risk and showing robust cloud security alignment.
* **Data Wrangling & Transformation (Pandas ETL):** Advanced transformation layer built to parse heterogeneous data formats. Native date and time columns are cast to unified ISO strings, and missing data points (`NaN`) are resolved before synchronization to ensure downstream compatibility.
* **Automated Data Quality & Schema Validation:** Programmatic schema checks (`assert`) run automatically post-upload. The pipeline compares local schema signatures and row counts directly against cloud metadata, guaranteeing 100% end-to-end data integrity.

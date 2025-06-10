# Projeto Consolidado de Análise e Agrupamento de Dados Contratuais

Este projeto integra três frentes principais de análise de dados:

- Previsão de campos ausentes utilizando Machine Learning
- Ajuste e normalização de índices em dados contratuais
- Agrupamento de fórmulas sintéticas com base em vetorização textual

---

## 📌 Parte 1: Previsão com Machine Learning

# CSFR - Análise e Previsão com Machine Learning

Este projeto tem como objetivo realizar a análise e previsão de valores ausentes em colunas específicas de um conjunto de dados CSFR utilizando técnicas de aprendizado de máquina, com foco especial em Random Forest.

## 📌 Objetivos

- Analisar a relação entre variáveis categóricas e numéricas.
- Preencher dados ausentes nas colunas de Índice, Peso e FatorK com base em features relevantes.
- Avaliar o desempenho do modelo com métricas apropriadas.
- Exportar o resultado em um arquivo Excel com destaques visuais nas células preenchidas.

## 📁 Estrutura

O notebook executa as seguintes etapas:

1. **Carregamento dos dados**: Leitura de arquivos `.xlsx` usando o `pandas`.
2. **Pré-processamento**:
   - Conversão de colunas categóricas para `category`.
   - Criação de pipelines com `ColumnTransformer` e `Pipeline`.
3. **Modelagem**:
   - Treinamento de modelos `RandomForestClassifier` e `RandomForestRegressor`.
   - Previsão apenas de células originalmente nulas.
4. **Pós-processamento**:
   - Coloração de células preenchidas por grupo de colunas (Índice, Peso, FatorK).
   - Exportação final do DataFrame com formatação.

## ▶️ Como executar

1. Clone este repositório:
   ```bash
   git clone https://github.com/seuusuario/csfr-ml-previsao.git
   cd csfr-ml-previsao
   ```

2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```

3. Execute o notebook:
   ```bash
   jupyter notebook CSFR_analise_ML_previsão.ipynb
   ```

## 📊 Resultados

Os dados preenchidos são exportados para um arquivo Excel com destaque por cor, indicando quais valores foram imputados pelo modelo.

## 🛠️ Tecnologias

- Python 3.10+
- pandas
- scikit-learn
- openpyxl
- matplotlib

## 📄 Licença

Este projeto é confidencial e destinado ao uso interno da organização.


---

## ⚙️ Parte 2: Ajuste de Índices Contratuais

# CSFR - Ajuste de Índices em Dados Contratuais

Este projeto tem como foco o ajuste e análise dos índices aplicados em dados contratuais. O objetivo é tratar e harmonizar os dados utilizando agrupamento de índices e normalização, garantindo consistência para análises futuras.

## 📌 Objetivos

- Carregar dados contratuais em formato Excel.
- Agrupar e normalizar valores de colunas específicas.
- Aplicar ajustes e consistência nos índices relacionados.
- Exportar os dados tratados com formatação visual.

## 📁 Etapas do Notebook

1. **Leitura de Dados**:
   - Utilização do `pandas` para importar os dados de um arquivo `.xlsx`.

2. **Pré-processamento**:
   - Conversão de colunas para tipos adequados.
   - Agrupamento e ajuste de valores conforme regras específicas.

3. **Ajustes e Normalizações**:
   - Normalização de pesos por grupo de índice.
   - Garantia de que somatórios respeitam as regras de 100%.

4. **Exportação**:
   - Salvamento dos dados ajustados em um novo arquivo Excel.
   - Aplicação de cores para destacar as colunas modificadas.

## ▶️ Como Executar

1. Clone este repositório:
   ```bash
   git clone https://github.com/seuusuario/csfr-ajuste-indices.git
   cd csfr-ajuste-indices
   ```

2. Instale os pacotes necessários:
   ```bash
   pip install -r requirements.txt
   ```

3. Execute o notebook:
   ```bash
   jupyter notebook CSFR_ajuste_indices.ipynb
   ```

## 🛠️ Tecnologias

- Python 3.10+
- pandas
- openpyxl
- numpy

## 📄 Licença

Projeto restrito ao uso interno e confidencial.


---

## 🧠 Parte 3: Agrupamento de Fórmulas Sintéticas

# Agrupamento de Fórmulas Sintéticas com Machine Learning

Este projeto aplica técnicas de agrupamento não supervisionado para classificar e agrupar fórmulas sintéticas com base em similaridade semântica. O objetivo é identificar padrões em fórmulas contratuais e agrupá-las de forma automatizada usando aprendizado de máquina.

## 📌 Objetivos

- Vetorizar fórmulas utilizando TF-IDF.
- Aplicar algoritmos de clustering como KMeans para agrupar fórmulas similares.
- Determinar o número ideal de clusters com base em análise de inércia.
- Visualizar e exportar os resultados com agrupamentos destacados.

## 📁 Etapas do Notebook

1. **Leitura dos Dados**:
   - Importação de planilha com fórmulas sintéticas.

2. **Vetorizações e Pré-processamento**:
   - Limpeza textual.
   - Aplicação de TF-IDF para transformar texto em vetores.

3. **Clusterização**:
   - Uso de `KMeans` com diferentes valores de `k`.
   - Análise de inércia para escolha de `k` ideal.
   - Atribuição de rótulo de cluster a cada fórmula.

4. **Exportação**:
   - Geração de um novo arquivo Excel com a coluna `cluster` e coloração por grupo.

## ▶️ Como Executar

1. Clone este repositório:
   ```bash
   git clone https://github.com/seuusuario/agrupamento-formulas.git
   cd agrupamento-formulas
   ```

2. Instale os pacotes necessários:
   ```bash
   pip install -r requirements.txt
   ```

3. Execute o notebook:
   ```bash
   jupyter notebook Agrupamento_Formula_Sintetica.ipynb
   ```

## 📊 Tecnologias

- Python 3.10+
- pandas
- scikit-learn
- matplotlib
- seaborn
- openpyxl

## 📄 Licença

Este projeto é confidencial e de uso restrito para análise contratual.


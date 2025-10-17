# Portfólio Analise de dados (Python)

# Life Style Analysis

**Descrição**

Análise exploratória e preparação de dados de um dataset "Life Style" com objetivo de extrair insights, preparar features e demonstrar um fluxo completo de análise.

---

## 1. Objetivo do projeto

* Demonstrar habilidades em ingestão, limpeza, exploração e visualização de dados.
* Realizar análise descritiva e identificar padrões relevantes no comportamento de vida/estilo.
* Preparar dados e, opcionalmente, conduzir modelagem preditiva simples (classificação/regressão) para responder perguntas de negócio.

---

## 2. Conteúdo entregue

* Notebook `Life Style Analysis.ipynb` contendo o fluxo completo da análise.
* (Opcional) diretório `data/` com datasets usados (raw e processed).
* `README.md` — este arquivo, com instruções para reproduzir e pontos-chave do projeto.

---

## 3. Resumo do dataset

* Número de linhas: 20000.
* Número de colunas: 53.
* Tipos principais: numéricos (e.g. idade, peso), categóricos (e.g. gênero), binários (e.g. pratica_exercicio)).
* Colunas de destaque (exemplos): `Age`, `Gender`, `Height`, `Weight`, `Activity_Level`, `Calories_Burned_30min`, `Sleep_Hours`, `Diet_Type`.

---

## 4. Perguntas de negócio (exemplos que o projeto responde)

* Quais variáveis estão mais correlacionadas com queima de calorias em 30 minutos?
* Existe diferença significativa de atividade física por faixa etária e gênero?
* Quais perfis de usuário apresentam maior risco de sedentarismo?
* Como agrupar usuários por estilo de vida (clustering) para segmentação?

---

## 5. Metodologia / Estrutura do notebook

1. **Carregamento e inspeção inicial**

   * Leitura de arquivos (CSV / Excel).
   * Visualização de shape, tipos, primeiras linhas e estatísticas descritivas.

2. **Limpeza e pré-processamento**

   * Tratamento de valores faltantes (remoção, imputação por média/mediana/moda ou modelos).
   * Conversão de tipos (datas, categóricos), normalização/transformação de unidades (cm/kg → m/ kg se necessário).
   * Criação de colunas derivadas (IMC, faixa etária, bins para calorias, etc.).
   * Detecção e tratamento de outliers (IQR, z-score ou inspeção manual).

3. **Análise exploratória (EDA)**

   * Distribuições univariadas (histogramas, boxplots).
   * Análises bivariadas (heatmap de correlação, scatterplots por pares relevantes).
   * Análise de variáveis categóricas (contagens, proporções, gráficos de barras).
   * Análise temporal (se houver timestamps).

4. **Feature engineering**

   * Encoding de variáveis categóricas (one-hot, label encoding).
   * Escalonamento de features numéricas quando necessário.
   * Seleção de features (correlação, importância, LASSO, permutação).

5. **Modelagem (opcional)**

   * Problema proposto (classificação: ex. sedentário vs ativo; regressão: calorias queimadas).
   * Pipeline de treino/validação (train/test split, cross-validation).
   * Modelos de baseline (Logistic Regression, Decision Tree, Random Forest, XGBoost).
   * Métricas (AUC, accuracy, precision/recall, RMSE) e interpretação de resultados.

6. **Interpretação e conclusões**

   * Principais insights.
   * Recomendações (ações de negócio, limitações dos dados).

---

## 6. Principais insights esperados (exemplos)

* Variáveis com maior influência sobre gastos calóricos.
* Perfis etários com menor atividade física média.
* Segmentos de usuários que podem se beneficiar de intervenções (programas de atividade, dieta).

---

## 7. Como rodar o projeto localmente

1. Clone este repositório.
2. Crie e ative um ambiente virtual (ex.: `venv` ou `conda`).

```bash
python -m venv .venv
source .venv/bin/activate     # macOS / Linux
.\.venv\Scripts\activate    # Windows
```

3. Instale dependências sugeridas:

```bash
pip install -r requirements.txt
```

**Sugestão de `requirements.txt`**

```
pandas
numpy
matplotlib
seaborn
scikit-learn
jupyterlab
openpyxl
plotly
xgboost
```

4. Abra o notebook:

```bash
jupyter lab
# ou
jupyter notebook
```

---

## 8. Boas práticas aplicadas

* Reprodutibilidade: seeds fixas para splits e modelos, `requirements.txt`.
* Versionamento: sugerir uso de Git e commits atômicos.
* Organização: separar raw/processed data, scripts e notebooks.
* Documentação: comentários e células Markdown explicativas no notebook.

---

## 9. Extensões recomendadas / próximos passos

* Implementar um dashboard interativo com Power BI ou Plotly Dash para visualização dinâmica.
* Construir modelo preditivo robusto e criar monitoramento de performance.
* Enriquecer dados com fontes externas (ex.: dados demográficos por região, clima) para análises causais.

---

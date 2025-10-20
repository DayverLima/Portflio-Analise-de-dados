# Análise de Fatores de Risco de Câncer

**Descrição**

Análise Exploratória de Dados (EDA) e processamento de um *dataset* de fatores de risco de câncer. O objetivo é identificar as correlações mais significativas entre hábitos, histórico e ambiente, e o Nível de Risco Geral (`Risk_Level`) de um paciente, extraindo *insights* cruciais para a prevenção e conscientização.

-----

## 1\. Objetivo do projeto

  * **Identificação de Fatores:** Determinar quais variáveis (estilo de vida, demográficas, genéticas) possuem o maior impacto no `Overall_Risk_Score`.
  * **Demonstração Técnica:** Apresentar um fluxo completo de análise de dados (limpeza, exploração, visualização e interpretação) usando Python.
  * **Saúde Pública:** Gerar *insights* baseados em dados que podem informar programas de prevenção ou alertas de saúde.

-----

## 2\. Conteúdo entregue

  * Notebook `Cancer Risk Factors.ipynb` contendo o fluxo completo da análise e todas as visualizações.
  * (Opcional) diretório `data/` com o *dataset* original (e.g., `cancer-risk-factors.csv`).
  * `README.md` — este arquivo, com o resumo da análise e instruções.

-----

## 3\. Resumo do dataset

  * Número de linhas: 2000.
  * Colunas de Risco: 17 fatores de risco e 3 variáveis de saída.
  * Tipos principais: Numéricos (`Age`, `Overall_Risk_Score`) e Categóricos/Binários (`Smoking`, `Family_History`, `Risk_Level`).
  * **Colunas de destaque:**
      * **Saída:** `Overall_Risk_Score`, `Risk_Level`
      * **Estilo de Vida:** `Smoking`, `Alcohol_Use`, `Obesity`, `Physical_Activity`
      * **Genético/Histórico:** `Family_History`, `BRCA_Mutation`
      * **Dieta/Outros:** `Diet_Red_Meat`, `Diet_Salted_Processed`, `Fruit_Veg_Intake`, `Air_Pollution`

-----

## 4\. Perguntas de Análise (Foco em Risco)

  * Quais fatores de risco (e.g., Fumo, Obesidade) possuem a maior correlação com o `Overall_Risk_Score`?
  * Qual é o perfil de paciente mais comum classificado no `Risk_Level` "High"?
  * Qual a diferença no `Overall_Risk_Score` entre pacientes com e sem `Family_History` (Histórico Familiar)?
  * A combinação de múltiplos fatores (ex: `Smoking` + `Alcohol_Use`) tem um efeito cumulativo e sinérgico no risco?

-----

## 5\. Metodologia / Estrutura do notebook

1.  **Carregamento e Inspeção Inicial**
      * Leitura do arquivo de dados.
      * Inspeção do *shape*, tipos de dados e estatísticas descritivas básicas.
2.  **Limpeza e Pré-processamento**
      * Tratamento de valores faltantes (se aplicável).
      * Conversão e codificação (e.g., *Label Encoding* ou *One-Hot Encoding*) de variáveis categóricas para análise de correlação.
3.  **Análise Exploratória (EDA) e Visualizações**
      * Distribuição da variável de saída (`Risk_Level`).
      * Análise da relação entre idade e risco.
      * **Matriz de Correlação:** Geração de *heatmap* para identificar as variáveis mais correlacionadas ao `Overall_Risk_Score`.
      * Análise da distribuição de risco por fatores individuais (ex: `Smoking` vs. `Risk_Level`).
4.  **Interpretação e Conclusões**
      * Discussão dos principais *insights* e suas implicações.
      * Recomendações finais baseadas nos dados.

-----

## 6\. Principais Insights e Conclusões

A análise revelou fortes correlações entre múltiplos fatores de estilo de vida e o risco de câncer.

  * **Risco Primário:** O **tabagismo e o uso de álcool** foram identificados como os principais fatores de risco, com um impacto que pode elevar a probabilidade de diagnóstico em até 70%.
  * **Fatores Dietéticos:** Dietas ricas em sal e alimentos processados demonstraram uma relação direta, aumentando o risco de câncer de cólon em aproximadamente 37%.
  * **Sedentarismo:** A falta de atividade física (`Physical_Activity`) mostrou um impacto transversal, elevando o risco em diversos tipos de câncer em índices próximos a 50%.
  * **Efeito Cumulativo:** Observou-se que a combinação de múltiplos fatores de risco (como obesidade, dieta inadequada e baixa atividade física) apresenta efeitos ainda mais expressivos, sugerindo um impacto cumulativo sobre o risco.
  * **Recomendação:** As correlações identificadas ressaltam a importância da promoção de hábitos saudáveis, como alimentação equilibrada e prática regular de exercícios, para a prevenção do câncer.

-----

-----

## 7\. Boas práticas aplicadas

  * **Reprodutibilidade:** Uso de *seeds* fixas para garantir a reprodutibilidade de qualquer processo aleatório (se houver).
  * **Organização:** O fluxo analítico segue uma estrutura lógica no notebook, com comentários e células *Markdown* explicativas.
  * **Visualização:** Uso de bibliotecas padrão (`matplotlib`, `seaborn`) para visualizações claras e informativas.

-----

## 8\. Extensões recomendadas / próximos passos

  * **Modelagem Preditiva:** Construir um modelo de Classificação para prever o `Risk_Level` (Low/Medium/High) com base nos fatores de risco, usando algoritmos como *Logistic Regression* ou *Random Forest*.
  * **Web App/Dashboard:** Implementar um *dashboard* interativo com Plotly/Dash ou Streamlit para permitir a simulação de perfis de risco.
  * **Análise Causal:** Utilizar técnicas para tentar inferir relações causais (e não apenas correlacionais) entre os fatores e o risco.

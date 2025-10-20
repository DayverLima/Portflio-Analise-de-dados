

### Fatores de Risco de Câncer - Análise de Dados

Este projeto consiste em uma Análise de Dados Exploratória (EDA) focada na identificação e quantificação da influência de diversos fatores de risco na propensão geral ao câncer. O objetivo principal é entender as correlações entre variáveis demográficas, de estilo de vida, ambientais e genéticas com o **Nível de Risco Geral** do paciente (`Risk_Level`).

### Dados

O projeto utiliza o conjunto de dados `cancer-risk-factors.csv`, que contém 2000 registros de pacientes.

**Variáveis Chave Analisadas:**

| Categoria | Variáveis |
| :--- | :--- |
| **Demográficas** | `Age`, `Gender` |
| **Estilo de Vida** | `Smoking`, `Alcohol_Use`, `Obesity`, `Diet_Red_Meat`, `Diet_Salted_Processed`, `Fruit_Veg_Intake`, `Physical_Activity` |
| **Ambientais/Outras** | `Air_Pollution`, `Occupational_Hazards`, `H_Pylori_Infection` |
| **Genéticas** | `Family_History`, `BRCA_Mutation` |
| **Saída** | `Overall_Risk_Score`, `Risk_Level` (`Low`, `Medium`, `High`) |

### Análise e Resultados Chave

A análise exploratória identificou diversos fatores de risco com impacto significativo no aumento da pontuação de risco geral e no nível de vulnerabilidade ao câncer.

* **Fumo e Álcool como Fatores de Risco Principais:** O tabagismo e o uso de álcool foram identificados como os principais fatores de risco, com um impacto que pode elevar a probabilidade de diagnóstico em até 70%.
* **Fatores Dietéticos:** Dietas ricas em sal e alimentos processados demonstraram uma relação direta, aumentando o risco de câncer de cólon em aproximadamente 37%.
* **Sedentarismo:** A falta de atividade física (`Physical_Activity`) mostrou um impacto transversal, elevando o risco em diversos tipos de câncer em índices próximos a 50%.
* **Efeito Cumulativo:** Observou-se que a combinação de múltiplos fatores de risco (como obesidade, dieta inadequada e baixa atividade física) apresenta efeitos ainda mais expressivos, sugerindo um impacto cumulativo sobre o risco.
* **Perfil de Vulnerabilidade:** O estudo evidencia que os fatores de risco interagem entre si, formando perfis de vulnerabilidade específicos que podem servir de base para análises preditivas futuras.

### Tecnologias

O projeto foi desenvolvido em Python utilizando as seguintes bibliotecas:

* **`pandas`** e **`numpy`**: Para manipulação e processamento de dados.
* **`matplotlib`** e **`seaborn`**: Para visualização e criação de gráficos de distribuição e correlação.
* **Jupyter Notebook**: Para o desenvolvimento interativo da análise.
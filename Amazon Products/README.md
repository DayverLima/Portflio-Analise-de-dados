### Amazon Products – Análise de Dados

Este projeto consiste em uma **Análise de Dados Exploratória (EDA)** aplicada a um conjunto de produtos da **Amazon**, com o objetivo de compreender padrões relacionados a **preço, desconto, avaliações e comportamento de usuários**.
A análise busca identificar os produtos mais bem avaliados, os mais comentados e como o percentual de desconto influencia na avaliação média.

---

### Dados

O projeto utiliza o dataset `amazon.csv`, contendo informações de produtos listados na Amazon.

**Principais variáveis analisadas:**

| Categoria                    | Variáveis                                                             |
| :--------------------------- | :-------------------------------------------------------------------- |
| **Identificação do Produto** | `product_id`, `product_name`, `category`                              |
| **Preço e Desconto**         | `discounted_price`, `actual_price`, `discount_percentage`             |
| **Avaliações**               | `rating`, `rating_count`                                              |
| **Usuários e Reviews**       | `user_id`, `user_name`, `review_id`, `review_title`, `review_content` |

---

### Etapas da Análise

1. **Leitura e Entendimento dos Dados:**
   Importação do arquivo CSV, verificação de colunas, tipos de dados, valores ausentes e duplicados.

2. **Limpeza e Preparação dos Dados:**

   * Remoção de símbolos (`₹`, `%`) e conversão de colunas numéricas.
   * Separação de colunas categóricas e textuais em listas (`category`, `review_content`, etc.).
   * Tratamento de valores inválidos em `rating` e substituição de erros por `0`.

3. **Análise Exploratória de Dados (EDA):**

   * **Top 10 produtos por avaliação**: identificação dos itens com maior nota média.
   * **Top 10 produtos por número de avaliações**: destaque para os produtos mais comentados.
   * **Correlação entre desconto e avaliação**: exploração visual da relação entre o percentual de desconto e a nota recebida.
   * **Distribuição de descontos e avaliações**: histograma da distribuição geral de ambas as variáveis.

---

### Principais Insights

* **Descontos e Avaliações:** Observa-se uma leve tendência de que produtos com maiores descontos apresentam variação significativa nas notas, sugerindo impacto indireto no interesse dos consumidores.
* **Popularidade:** Os produtos com maior número de avaliações não são necessariamente os com melhores notas — indicando possível correlação entre volume de vendas e visibilidade.
* **Distribuição de Descontos:** A maioria dos produtos concentra descontos entre **10% e 50%**, com poucos ultrapassando 70%.
* **Qualidade dos Dados:** Foram identificados valores inválidos e inconsistências textuais, corrigidas durante o tratamento inicial.

---

### Tecnologias Utilizadas

O projeto foi desenvolvido em **Python**, utilizando as seguintes bibliotecas:

* **`pandas`** e **`numpy`** – Manipulação, limpeza e transformação de dados.
* **`matplotlib`** e **`seaborn`** – Visualização e análise gráfica.
* **`warnings`** – Supressão de alertas durante execução.
* **Jupyter Notebook** – Ambiente de desenvolvimento interativo para execução das análises.

---

### Conclusão

A análise revelou **tendências valiosas** sobre os padrões de desconto, avaliação e popularidade dos produtos na Amazon.
Os resultados podem servir como base para **modelos preditivos** (por exemplo, previsão de avaliações ou impacto de descontos nas vendas) ou para **análises de mercado** voltadas à otimização de campanhas promocionais.

---

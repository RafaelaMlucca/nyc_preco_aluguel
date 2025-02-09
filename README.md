# 📊 Previsão de Preços de Imóveis - Nova York

Este projeto tem como objetivo realizar uma análise exploratória de dados (EDA), modelagem estatística e machine learning para prever preços de imóveis em Nova York. O trabalho foi desenvolvido no **Google Colab** e utiliza modelos de regressão linear, regressão logística e Random Forest.

---

## 🚀 Como Executar

### **1️⃣ Acesse o Google Colab**
O projeto foi desenvolvido no Google Colab. Para abrir o notebook, basta clicar no link abaixo:

📎 **[Abrir Notebook no Colab](https://colab.research.google.com/)**

Caso esteja rodando localmente, siga os passos abaixo.

---

## 📥 Instalação das Dependências

Para executar o projeto, instale todas as bibliotecas necessárias:

```bash
pip install -r requirements.txt
```

**Bibliotecas utilizadas**:
- `pandas`
- `numpy`
- `seaborn`
- `matplotlib`
- `scikit-learn`
- `statsmodels`
- `folium`

Se estiver no Google Colab, basta rodar a célula de instalação no início do notebook.

---

## 📂 Estrutura do Projeto

```
📁 PrevisaoPrecosNY/
│── 📜 README.md                 # Documentação do projeto
│── 📜 requirements.txt           # Dependências do projeto
│── 📜 PrevisaoAlugueisNY.ipynb   # Notebook com análise e modelagem
│── 📜 modelo_linear_simples.pkl  # Modelo de Regressão Linear treinado
│── 📜 modelo_logistic_regression.pkl  # Modelo de Regressão Logística treinado
│── 📜 modelo_random_forest.pkl   # Modelo Random Forest treinado
```

---

## 🔎 Análise Exploratória (EDA)

No notebook, realizamos:
- **Análise descritiva das variáveis**: distribuição, estatísticas e relação com o preço.
- **Transformação de variáveis**: ajuste para normalidade e remoção de outliers.
- **Mapeamento de imóveis**: visualização geográfica dos imóveis mais caros e mais baratos.

---

## 🤖 Modelos Treinados

Utilizamos três modelos de Machine Learning para prever os preços dos imóveis:

| Modelo                 | Objetivo  | Arquivo |
|------------------------|-----------|--------------------------|
| **Regressão Linear**   | Previsão de preços contínuos | `modelo_linear_simples.pkl` |
| **Regressão Logística** | Classificação (preço alto/baixo) | `modelo_logistic_regression.pkl` |
| **Random Forest**      | Previsão não linear | `modelo_random_forest.pkl` |

---

## 🔮 Como Fazer Previsões

Para carregar um modelo treinado e fazer previsões:

```python
import pickle
import pandas as pd

# Carregar o modelo treinado
with open("modelo_random_forest.pkl", "rb") as f:
    modelo = pickle.load(f)

# Criar um exemplo de entrada
novo_imovel = pd.DataFrame({
    "minimo_noites": [3],
    "disponibilidade_365": [200],
    "numero_de_reviews": [15],
    "calculado_host_listings_count": [5]
})

# Fazer a previsão
previsao = modelo.predict(novo_imovel)
print(f"📌 Preço previsto: ${previsao[0]:.2f}")
```

---

## 📌 Conclusões

- **Os bairros de Manhattan e Brooklyn apresentam os preços mais elevados**.
- **A disponibilidade anual e o número mínimo de noites impactam no valor do aluguel**.
- **Palavras como "luxury", "loft" e "apartment" são comuns em imóveis de alto valor**.
- **Random Forest apresentou o melhor desempenho na previsão dos preços**.

---

## 📩 Contato
Caso tenha dúvidas ou sugestões, entre em contato:  
📧 **seu-email@example.com**  
📌 [Seu LinkedIn](https://www.linkedin.com/)

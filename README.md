# 🏠 Previsão de Valores de Imóveis — Boston Housing

> Solução completa de Machine Learning para predição de preços de imóveis, com análise exploratória, modelagem por Random Forest e deploy de aplicação interativa via Streamlit.

---

## 📋 Sobre o Projeto

Um executivo do ramo imobiliário em Boston (EUA) solicitou à sua equipe de Ciência de Dados um modelo capaz de prever o valor mediano de imóveis com base em características como localização, infraestrutura e perfil socioeconômico do entorno.

Este repositório contém o pipeline completo: da análise exploratória dos dados (EDA) até o deploy de uma aplicação interativa para uso não técnico.

---

## 🗂️ Estrutura do Projeto

```
previsao-imoveis/
├── PrevisaoValores_Regressao.ipynb   # Análise exploratória + treinamento do modelo
├── app.py                            # Aplicação web com Streamlit
├── model/
│   └── data.csv                      # Dataset processado (gerado pelo notebook)
├── requirements.txt
└── README.md
```

---

## ✨ Funcionalidades

- **Análise Exploratória (EDA)** — estatísticas descritivas, correlações e visualizações
- **Baseline por categoria** — modelo simples de referência por porte do imóvel (Pequeno/Médio/Grande)
- **Modelo Random Forest Regressor** — ensemble de 200 árvores com 8 features selecionadas
- **Métricas de avaliação** — MAE, MSE e R² comparados contra a baseline
- **Aplicação Streamlit** — interface web com histograma interativo e predição em tempo real

---

## 📊 Dataset

O projeto utiliza o **Boston Housing Dataset** (Harrison & Rubinfeld, 1978), um clássico de ML com 506 amostras e 13 variáveis preditoras.

| Variável | Descrição |
|---|---|
| CRIM | Taxa de criminalidade per capita |
| INDUS | Proporção de hectares de negócios não varejistas |
| CHAS | Faz limite com o Rio Charles? (1=Sim, 0=Não) |
| NOX | Concentração de óxido nítrico |
| RM | Número médio de quartos |
| PTRATIO | Razão alunos/professor por bairro |
| B | Proporção de pessoas com descendência afro-americana |
| LSTAT | % da população de baixa renda |
| **MEDV** | **Valor mediano dos imóveis em US$ milhares (alvo)** |

---

## 🤖 Modelo

**Algoritmo:** `RandomForestRegressor` (scikit-learn)

```python
RandomForestRegressor(n_estimators=200, max_depth=7, max_features=3)
```

| Parâmetro | Valor | Significado |
|---|---|---|
| `n_estimators` | 200 | Número de árvores no ensemble |
| `max_depth` | 7 | Profundidade máxima de cada árvore |
| `max_features` | 3 | Máximo de features por divisão de nó |

---

## 🚀 Como Executar

### Pré-requisitos

- Python 3.8+
- pip

### 1. Clone o repositório

```bash
git clone https://github.com/seu-usuario/previsao-imoveis.git
cd previsao-imoveis
```

### 2. Instale as dependências

```bash
pip install -r requirements.txt
```

### 3. Gere o `data.csv` (se necessário)

Abra e execute o notebook `PrevisaoValores_Regressao.ipynb` até a célula que salva o CSV:
```python
X.to_csv('model/data.csv', index=False)
```

### 4. Execute a aplicação

```bash
streamlit run app.py
```

Acesse em: **http://localhost:8501**

---

## 🖥️ Usando a Aplicação

1. **Histograma** — ajuste o slider para filtrar imóveis por faixa de preço e visualizar a distribuição
2. **Painel lateral** — preencha os atributos do imóvel (criminalidade, quartos, poluição etc.)
3. **Predição** — clique em *"Realizar Predição de Valor do Imóvel"* para ver o valor estimado

---

## 🛠️ Tecnologias

| Tecnologia | Uso |
|---|---|
| Python 3.x | Linguagem principal |
| Pandas / NumPy | Manipulação de dados |
| Seaborn / Matplotlib | Visualizações na EDA |
| Scikit-learn | Modelagem — RandomForestRegressor |
| Streamlit | Interface web interativa |
| Plotly Express | Gráficos interativos |

---

## 📄 Referências

- Harrison, D. & Rubinfeld, D.L. (1978). *Hedonic prices and the demand for clean air*
- [UCI ML Housing Dataset](https://archive.ics.uci.edu/ml/machine-learning-databases/housing/)
- Material baseado na **Semana de Data Science do Canal Minerando Dados**

---

<p align="center">Desenvolvido como estudo de caso em Ciência de Dados 🧠</p>

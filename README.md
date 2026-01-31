 Projeto Sousa Imóveis - Previsão de Preços
Este projeto utiliza Machine Learning para prever o valor de imóveis em Boston com base em características como número de quartos, taxa de criminalidade e localização.

 Objetivo
Desenvolver uma ferramenta prática para executivos do ramo imobiliário estimarem preços de mercado de forma automatizada.

 O que foi feito:
Análise de Dados: Exploração do dataset de Boston.

Modelo de IA: Treinamento de um algoritmo de Random Forest (Floresta Aleatória).

Interface Web: Criação de um aplicativo interativo com Streamlit.

 Como rodar o projeto:
Instale as dependências:

Bash
pip install pandas streamlit plotly scikit-learn
Inicie o aplicativo:

Bash
cd Deploy
python -m streamlit run app.py
 Estrutura de Pastas
/Deploy: Arquivos do aplicativo.

/Deploy/app.py: Código da interface e modelo.

/Deploy/model: Pasta contendo o arquivo data.csv.
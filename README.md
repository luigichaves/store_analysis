# store_analysis

Repositório de análise de dados com objetivo de analisar os dados fornecidos de uma loja e identificar insights e padrões, para, em seguida, criar um modelo de previsão para prever a probabilidade de um cliente dar uma resposta positiva à uma oferta.

# Início
Dataset utilizado:
* https://www.kaggle.com/datasets/ahsan81/superstore-marketing-campaign-dataset

Ferramentas utilizadas:
* Python;
* Jupyter Notebook;
* Git;
* GitHub.

Bibliotecas utilizadas:
* Numpy;
* Pandas;
* Matplotlib;
* Seaborn;
* Plotly.

# Apresentação do dataset
|Nome da Coluna|Descrição|Tipo de dado|
|--------------|---------|------------|
|ID|número único de cada cliente|int64|
|Year_Birth|ano de nascimento do cliente|int64|
|Education|nível de educação do cliente|object|
|Maritial_Status|estado civil|object|
|Income|renda familiar anual|float64|
|Kidhome|número de crianças em casa|int64|
|Teenhome|número de adolescentes em casa|int64|
|Dt_Customer|data de inscrição do cliente na empresa|datetime64[ns]|
|Recency|número de dias desde a última compra|int64|
|MntWines|o valor gasto em produtos vitivinícolas nos últimos 2 anos|int64|
|MntFruits|o valor gasto em frutas nos últimos 2 anos|int64|
|MntMeatProducts|o valor gasto em produtos de carne nos últimos dois anos|int64|
|MntFishProducts|o valor gasto em produtos de peixe nos últimos dois anos|int64|
|MntSweetProducts|o valor gasto em produtos doces nos últimos dois anos|int64|
|MntGoldProds|o valor gasto em produtos de ouro nos últimos dois anos|int64|
|NumDealsPurchases|números de compras feitas com desconto|int64|
|NumWebPurchases|número de compras feitas através do site da empresa|int64|
|NumCatalogPurchases|número de compras feitas por catálogo (compra de mercadorias para envio pelo correio)|int64|
|NumStorePurchases|número de compras feitas diretamente nas lojas|int64|
|NumWebVisitsMonth|número de visitas ao site da empresa no último mês|int64|
|Response|1 se o cliente aceitou a oferta na última campanha, 0 caso contrário|int64|
|Complain|1 se o cliente reclamou nos últimos 2 anos|int64|




*Contexto*- Uma loja está planejando a liquidação de fim de ano. Eles querem lançar uma nova oferta - assinatura ouro, que dá 20% de desconto em todas as compras, por apenas $ 499, que é $ 999 nos outros dias. Ele será válido apenas para clientes existentes e a campanha por meio de ligações está sendo planejada para eles. A direção entende que a melhor forma de reduzir o custo da campanha é fazer um modelo preditivo que classifique os clientes que podem comprar a oferta.

*Objetivo* - A superloja quer prever a probabilidade de o cliente dar uma resposta positiva e quer identificar os diferentes fatores que afetam a resposta do cliente. Você precisa analisar os dados fornecidos para identificar esses fatores e, em seguida, criar um modelo de previsão para prever a probabilidade de um cliente dar uma resposta positiva.

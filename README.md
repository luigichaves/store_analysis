# store_analysis

Neste projeto, irei criar um repositório de análise de dados com o objetivo de analisar as informações fornecidas por uma loja e identificar padrões e insights valiosos. Utilizando técnicas de análise de dados, irei criar um modelo de previsão para prever a probabilidade de um cliente responder positivamente à uma oferta.

Os desafios deste projeto incluem a visualização de dados, a exploração do conjunto de dados, o tratamento de dados incompletos ou inconsistentes, o questionamento crítico dos resultados obtidos, a solução de problemas relacionados à análise de dados e a realização de cálculos e agregação de dados.

# Início
Dataset utilizado (Superstore Marketing Campaign Dataset):
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

*Objetivo* - A loja quer prever a probabilidade de o cliente dar uma resposta positiva e quer identificar os diferentes fatores que afetam a resposta do cliente. Precisa analisar os dados fornecidos para identificar esses fatores e, em seguida, criar um modelo de previsão para prever a probabilidade de um cliente dar uma resposta positiva.

---

## Sobre os dados:

![perc_10](https://user-images.githubusercontent.com/105527623/213175396-bec73389-8ae5-4db2-b76e-c2110101fa42.png)

Representados por 0 ou na cor azul, a maioria dos clientes em nosso conjunto de dados não aderiu a nenhuma oferta. Em laranja, temos aqueles que aceitaram alguma oferta (15%). Confira abaixo os percentuais de clientes de acordo com algumas características:


|Education|Percentual|  
|---------|----------| 
|Graduation|50%| 
|Phd|21%|
|Master|25%|
|Basic|2%|

|Marital_Status|Percentual|
|--------------|----------|
|Married|65%|
|Single|22%|
|Divorced|10%|
|Widow|3%|

|Kidhome|Percentual|
|-------|----------|
|0|58%|
|1|40%|
|2|2%|

|Teenhome|Percentual|
|--------|----------|
|0|52%|
|1|46%|
|2|2%|

![cat_perc](https://user-images.githubusercontent.com/105527623/213194747-f203abae-aa18-45a7-9739-8404c80e1988.png)

---

# Insights

* Maior parte do nosso público é graduado, ou casado, ou não tem filhos, como visto no gráfico acima.
* Aqueles que possuem maior probabilidade de adquirir alguma oferta são: solteiros ou viúvos, PhDs, ou sem filhos.

![prob_eciv](https://user-images.githubusercontent.com/105527623/213689708-8805549a-83c2-4b1e-ae4a-5fb265f7f934.png)
> Solteiros e viúvos tem mais probabilidade de aceitar uma oferta. Divorciados não ficam muito atrás. Casados possuem a menor probabilidade.

![prob_ed](https://user-images.githubusercontent.com/105527623/213689778-a0ae10ba-e8b5-4aa8-92b8-cd69f192773b.png)
> PhDs tem a maior chance disparada de aceitar uma oferta. Graduados e Mestres estão bem semelhantes.

![prob_cri](https://user-images.githubusercontent.com/105527623/213689800-7f49808b-4bb7-4df5-9e49-d536d4518f49.png)
> Clientes sem filhos crianças tem mais chances de adquirir uma oferta. O gráfico mostra claramente que esta probabilidade diminui com o aumento de crianças em casa.

![prob_jv](https://user-images.githubusercontent.com/105527623/213689837-7049b73b-6767-420c-9980-f5e8f9500c8a.png)
> Da mesma forma, clientes sem filhos jovens são mais propensos a aceitar uma oferta.

* A renda anual tem certa relação com o total gasto, como o esperado.

![ttl](https://user-images.githubusercontent.com/105527623/213687086-33c578c6-60b7-4d95-80d2-cdfa1ab7df9a.png)

* Clientes que gastam mais, tem uma chance maior de aceitar positivamente uma oferta.

![stplot](https://user-images.githubusercontent.com/105527623/213687627-6d8114d7-4865-48b5-9a03-575b0c57985b.png)

* Clientes sem filhos tendem a gastar mais. Casados e solteiros também.

![cat_box](https://user-images.githubusercontent.com/105527623/213688276-02d89acf-a4cd-48f5-b203-363876c62c24.png)

* A análise de cada tipo de produto mostrou que grandes consumidores de vinho, joias e carne com uma renda anual mais alta são mais propensos a adquirir à oferta.

![mntwines](https://user-images.githubusercontent.com/105527623/213688637-f8d202a4-2d76-484b-bc3f-41db5a15a145.png)
![mntgold](https://user-images.githubusercontent.com/105527623/213688678-92e9e5f7-4bb5-4678-801b-d6d953dac715.png)
![mntmeat](https://user-images.githubusercontent.com/105527623/213688709-7c13f031-8663-446b-ad3c-a25306b38ed2.png)

* Dito isso vejamos aqueles que mais consomem vinho, produtos de ouro e carne:

  * PhD's, divorciados e sem filhos tendem a gastar mais com vinho.
  ![1](https://user-images.githubusercontent.com/105527623/213689016-ff793fba-f9fb-4ea6-bbb6-7a13877800d2.png)
  * Graduados, viúvos e divorciados, e sem crianças em casa tendem a gastar mais em produtos de ouro.
  ![2](https://user-images.githubusercontent.com/105527623/213689053-cd24b03b-351c-4718-81b1-bf817ae4a4c7.png)
  * Graduados gastam mais em carne. Solteiros também, mas ainda próximos dos demais. Pessoas sem filhos tendem a consumir mais.
  ![3](https://user-images.githubusercontent.com/105527623/213689141-5f0b6d3e-67be-42f0-a47c-504ea0e4748f.png)

* 2012 e 2014 venderam muito menos em relação a 2014. Consequentemente, 2014 teve mais clientes que aderiram à oferta.

![vol_vd_ano](https://user-images.githubusercontent.com/105527623/213689196-46f6f08e-cefa-4c96-8ce6-d0c1fc3662ad.png)

# Conclusões

* A campanha de marketing para a oferta premium deve buscar grandes consumidores em geral, podendo então, direcionar a campanha para clientes sem filhos, casados ou solteiros, cuja tendem a gastar mais.
* Deve-se também, aplicar estratégias de marketing para os produtos de vinho, ouro e carne. Visando aqueles que tem preferência por estes produtos comprarem mais, visto que estes são mais propensos a obter a assinatura premium.
* Aos produtos citados acima, podemos direcionar o marketing da seguinte forma:
  * Aos grandes consumidores de vinho, direcionaremos a estratégia de marketing à PhD's, divorciados e sem filhos.
  * Aos grandes consumidore de produtos de ouro, direcionaremos a estratégia de marketing à Graduados, viúvos e divorciados, e sem crianças em casa.
  * Aos grandes cosumidores de carne, direcionaremos a estratégia de marketing à graduados e sem filhos.
* Isto para que possamos indicar a oferta premium com eficiência à aqueles que possuem uma chance maior de aceitar positivamente a assinatura.

# Análise venda bruta e lucro xNstore 2021-2023

# Link para o dashboard
https://app.powerbi.com/view?r=eyJrIjoiNWRmYjg3MGEtYzMyNy00ODk1LTg1YmEtMjA4ZjZhMWNkN2Y2IiwidCI6IjM1ZmZkMDk1LTM4MWQtNDA3MC1hOGM1LTIwOGJhYzgzNTMwOSJ9

* Case - Nos foi solicitado uma análise sobre venda bruta e lucro desde o momento em que a empresa passou a registrar as vendas em sistemas atualizados. 

* 1º Temporal - Observar a tendência dos valores e identificar focos ou desfocos.

* 2º Vendedores - Analisar o desempenho desde supervisores, gerentes e vendedores.

* 3º Região     - Analisar a granularidade, regiões de destaque, cidades com mais vendas.


# Importação de arquivos, power query e relacionamento entre tabelas

* Como foram utilizados arquivos de diferentes fontes como csv, xlsx e txt foram necessários vários passos até chegar uma tabela fVendas final, também mesclar consultas, transformar linhas em colunas e otimizar ao máximo as dimensões para tornar o relatório mais leve.




* PowerQuery - fVendas, dVendedor e dCliente


![PowerQuery - fVendas](https://github.com/nicolaskra/analise_vendas/assets/144272226/7fb0f627-7053-40f6-85b2-9fcf349f5517)![Captura de tela 2024-02-21 122648](https://github.com/nicolaskra/analise_vendas/assets/144272226/82ea86b9-ab97-4098-990d-7e0f3f535576)![Captura de tela 2024-02-21 122915](https://github.com/nicolaskra/analise_vendas/assets/144272226/89d43a04-ddb8-4382-90e1-a84caf66b716)

* Modelo StarSchema a onde existe apenas uma tabela fato conectada as dimensões.

![Captura de tela 2024-02-21 111315](https://github.com/nicolaskra/analise_vendas/assets/144272226/97690790-17fd-496a-b8d0-7049266243c3)

# Medidas DAX -  foram utilizadas diversas medidas desde as mais básicas, percentuais, temporais, formatação, rank. Todas foram agrupadas por subpastas para ficar fácil de localizar.

![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/d2c82f0e-0bf6-487a-a3e2-8affe8043580)


* Básicas

![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/3497b3ba-9497-4882-875a-6277ad8f6497)

* Formatação, algumas para retirar o total da matriz, outras para demonstrar a diferença no tooltip.

![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/52e25096-cf17-4c8b-825e-213e05c1bb7a)

* Percentuais, calculando share de categoria, cidade, estado, vendedor, anexando dax de formatação para retirar o total das matrizes.

![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/8b776da6-4d28-4d42-b63d-0245dd4f5342)

* Rank, calculando ranks para utilizar em matrizes facilitando a identificação dos dados.

![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/ba372bde-5031-4ae9-b454-0fb6d02631ed)

* Temporais, utilizado principalmente na primeira página para fazer os comparativos vs LY, acumulando YTD vs LY.

![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/709d93a0-cd5e-49d6-b502-13f8831d8574)







# Layout no figma

* Elaborei os gráficos primeiro mas defini um layout e usei nas 3 páginas de analise, foram vários testes com cores, layouts até chegar nesse resultado, eu gosto de cor escura mas optei em utilizar tons mais claros dessa vez.
* Pág1 ![Captura de tela 2024-02-21 124037](https://github.com/nicolaskra/analise_vendas/assets/144272226/caf77e47-e52a-42fb-9b0d-c5e3e338954a)

![Captura de tela 2024-02-21 123920](https://github.com/nicolaskra/analise_vendas/assets/144272226/2271400f-59dd-43de-a3ff-952586e80e96)

* Pág2 - Somente alterando o retangulo em cima da aba selecionada


![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/09e43437-46ac-4bb5-8c6a-a8a986d3559b)

* Pág3 - Somente alterando o retangulo em cima da aba selecionada

![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/5f4d65b8-9fff-4db7-a4ad-3ff621ba2cb8)

# Pág1 - Análise Temporal

![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/389a689c-7a12-4c0f-ae15-7378562792bf)

* Gráfico 1 Comparativo VENDA BRUTA X VENDA BRUTA LY sem acumular, com tooltip demonstrando a  variação.
 ![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/df2ae3a3-3f32-4575-9ee5-ad1dc017c30c)

* Gráfico 2 Comparativo VENDA BRUTA X VENDA BRUTA LY acumulando, com tooltip demonstrando a variação.
 ![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/40729022-3e97-4baa-a34d-178843166a7e)

* Gráfico 3 Comparativo LUCRO X LUCRO LY sem acumular com tooltip demonstrando a variação

  ![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/a43de379-c095-4cd5-a3b8-ac1f9139793c)

* Gráfico 4 Comparativo LUCRO X LUCRO LY acumulando com tooltipo demonstrando a variação

  ![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/ebd3adf4-4115-4894-93d1-f0de6ccf094d)

# Insights - Pág1 Temporal
* Nosso melhor ano desde que os registros passaram a ser controlados foi com certeza 2021, entretando faltam metade do mês de outubro, novembro e dezembro para fechar o ano de 2023. Em outubro/23 já superamos em 48.94% em relação a venda bruta LY(2022), para se ter ideia no lucro outubro/23 está 62.58% a cima do mesmo período LY.
* Mesmo faltando dois meses e meio para fechar o ano de 2023 faltam menos de R$50.000 para ultrapassar o valor da venda bruta de 2022, já em questão de lucro foi superado em torno de R$30.000. Um sinal muito bom, que as vendas estão no caminho certo.
* O melhor mês de 2023 foram Abril com os respectivos valores Abril/23 Venda Bruta R$341.565 aumento de 92.62% em relação ao LY, já com o lucro foi de R$83.552 um aumento percentual de 104.13%. 
* Já em 2022 o melhor mês foi agosto/22 com a venda bruta de R$291.363 porém com uma variação de -4.74% em relação a 2021 e lucro R$68.734 com a variação de -8.97%.
* Em 2021 o melhor mês foi novembro/21 com a venda bruta de R$407.620, aqui vale uma campanha para ultrapassar esse valor em 2023, novembro/21 rendeu R$100.605 de lucro. Observar se houve alguma promoção o que aconteceu para as vendas dispararem nesse ano.
* Em 2023 apenas dois meses venderam menos que 2022, janeiro e agosto, aqui vale uma investigação pois janeiro em ambos os anos a venda foi extremamente baixa em relação aos outros meses.
* Podemos observar que a perfomance do time de vendas melhorou muito em relação a 2022, porém podemos trabalhar com certas campanhas em alguns períodos para melhorar as vendas em pontos mais "fracos".

# Pág2 - Análise vendedores
![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/2fdcd40e-ee3a-4517-8327-77ca35aadc1f)

* Gráfico 1 - Gráfico de barras com venda bruta e lucro por supervisor
* Gráfico 2 - Gráfico de barras com venda bruta e lucro por gerente
* Matriz 1 - Análise de vendedor, com possibilidade de hierarquia com categoria, rank de acordo com a venda bruta, percentual representativo do total, parcial e a quantidade de venda. Tooltip com a foto do vendendor, com a venda bruta total acumulada (Year To Date) vs LY a foto e a variação com formatação condicional, caso seja positiva o valor fica verde, caso contrário vermelho.

![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/26ff4f58-9e07-4ac9-ba6f-a747fa0bb06b)![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/5d741a9a-b8c7-40c0-a6b5-f13192635c70)

* Matriz 2 - Análise de vendedor, com possibilidade de hierarquia com categoria, rank de acordo com lucro, percentual representativo do total, parcial e ticket médio. Tooltip com a foto do vendendor, com o lucro acumulado (Year To Date) vs LY a foto e a variação com formatação condicional, caso seja positiva o valor fica verde, caso contrário vermelho.

![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/5cd81dce-00cd-4170-8279-d4fca3a0e47b)![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/d6c5e432-5ff8-4da1-96ec-ca1702fa01c3)

# Insights - Pág2 Vendedores
* Temos 12 vendedores, os três mais bem colocados em venda bruta e lucro total, somam 30.3% da venda bruta total ou seja representam praticamente 1/3 de todas as vendas. Já com lucro eles tem uma representativdade de 30,12%. 
* No total geral Gustavo Gomes obteve 4.206 vendas o maior número, em relação a segunda colocada Julieta gomes com 3.792 é uma diferença de 234 vendas a mais, já comparando com o último Felipe Gonçalves que teve 2851 o saldo é de 1.355 a mais. Vale uma análise mais aprofundada para entender o motivo dessa diferença de valores.
* Porém se filtrarmos o ano de 2023 apenas Felipe Gonçalves subiu para 3º em venda bruta com R$ 242.808 e 9.54% de representatividade, para efeito de comparação Gustavo Gomes caiu para 6º com R$230.315 e 9.05% de representatividade.
* Em 2023 a equipe que mais vendeu foi da gerente Sofia Ribeiro com a venda total de R$706.110, R$171.810 de lucro, 3.400 vendas e 143 clientes. Composta por Felipe Gonçalves, Mateus Costa e Julia Silva.
* Os gerentes Diego Araujo e Fernando Silva contam com uma equipe de dois e um vendedor, e obtiveram resultados razoaveis vale apena analisar e ver a possibilidade de aumentar a equipe deles para maximizar as vendas.

# Pág3 - Análise Região 
![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/7f3825d3-8bc6-40ff-8c81-8bee1edc3ea8)

* Gráfico 1 - Gráfico de barras com venda bruta e lucro por região
* Gráfico 2 - Gráfico de barras com venda bruta e lucro por cidade
* Matriz 1 - Análise por estado com possibilidade de hierarquia por categoria, rank de acordo com a venda bruta, percentual de representatividade e a quantidade de vendas.

![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/a9e40dc7-ab6e-45ce-81b2-78c85dfa7321)

* Matriz 2 - Análise por cidade com possibilidade de hierarquia por categoria, rank de acordo com o lucro, percentual de representatividade e a quantidade de vendas.

![image](https://github.com/nicolaskra/analise_vendas/assets/144272226/962efb27-afce-43b5-8fc7-8ac41066e5d4)

# Insights - Pág3 Região
* Região 1 conta com 6 estados e atende 12 cidades, comparando com a região 2 que atende 11 estados e apenas 11 cidades, vale uma análise de uma possível expansão nessa região, atendendo mais cidades.
* Paraná foi o estado com a pior perfomance de venda bruta com o valor de R$270.693 e 3.22% de representatividade do total. Vale análise, curitiba é uma cidade grande e com comércio grande.
* Porto alegre é a cidade que em relação ao total representou o maior valor de lucro com R$115.996, 5.73% do total e 2.323 vendas.
* A cidade que tem a pior perfomance em relação a lucro é Belo horizonte com apenas R$55.847 e 2.76% de lucro do total. Vale uma análise pois é uma metropole, deveria estar próximo a São Paulo e Porto Alegre.













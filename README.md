# Case_logistica_databricks
Case mostra dados relacionados a logistica de entregas:
Dashboard feito no Databricks com programação em SQL


1 - Saúde da logística:

R.: Ao desenvolver o estudo nos deparamos com os seguintes eventos:
Temos um total de 153604 pedidos distintos no período analisado;
Maior modelo de entrega: “Own delivery” (140435 pedidos);
Tipo de rota mais utilizado: “Single pick single drop” 94,9% pedidos;
Maior modo de entrega: “Motorcicle” 92,4% pedidos;
Tipo de loja com maior alcance: “Restaurant” 98,7% pedidos.

2 - De acordo com os dados recebidos, você diria que houve algum evento especial ou situação anormal durante o período? Por quê?

R.: Ocorreram alguns eventos especiais como:
Conversão de pedidos com atraso pelos sem atraso chegou a 63,45% durante o período para pedidos feitos em restaurantes;
Ocorreram mais pedidos no sábado (11/04/2020), chegando a um crescimento de pedidos de 18,39% comparados ao dia anterior;
Apesar de sábado ser o dia com maior número de pedidos, ao analisar as conversações de pedidos atrasados e sem atrasos, notamos que os dias que mais geram atrasos acontecem durante a semana chegando a um pico de 70% na sexta-feira (10/04/2020).

3 - Observando os dados como cliente, você diria que prefere fazer pedidos em qual dia da semana e em qual restaurante? Por quê?

R.: Observando os dashs “Qtd de pedido por dia da semana”, “Conversões entres pedidos atrasados x sem atrasos” e “TOP 10 - Melhores restaurantes”, podemos dizer que:
Apesar de segunda ser o dia com menor índice de pedidos, o melhor dia para se fazer pedidos seria no sábado, pois ao observar a métrica de conversão de pedido atrasado pelos pedidos sem atraso vimos que durante o fim de semana são os dias que apresentam a menor conversão de pedidos atrasados;
Sobre qual restaurante faria o pedido, considerei duas métricas:
Pediria no restaurante 1019471 levando em consideração o volume de pedidos (721 pedidos);
Pediria no restaurante 141097 levando em consideração a menor média de tempo estimado de entrega (42 min), ou seja, o restaurante que tem entrega mais rápida.
Obs.: Senti falta de alguns dados como: Frete (Valor) e avaliação no app!

4 - Analisando os dados, como você identificaria que um restaurante pode estar tendo problemas na sua operação de delivery?

R.: Através de alguns dados presentes nos dashs “Taxa de atraso - pedido restaurante” podemos notar que alguns restaurantes podem estar com problemas na sua operação pois observamos uma tendência crescente de atrasos durante os dias da semana chegando a um pico na sexta-feira com 41,14% de restaurantes com pedido em atraso em relação aos pedidos gerais, o que deixa claro que existe problemas na pontualidade das entregas no período analisado, no fim de semana a taxa reduziu consideravelmente.
 Outra maneira foi observando o dash “Tempo médio de entregas min”, onde também verificamos um aumento significativo no tempo médio de entrega durante os dias da semana chegando a um pico na sexta-feira com média de 67,99 minutos, o que deixa claro que existe problemas na eficiência das entregas. Fiquei com alguns questionamentos, tais como: 
O que pode estar gerando o atraso no preparo dos pedidos?  
Existiu congestionamentos ou obstruções na via?
Teve algum fator climático que pode ter influenciado e gerado inadequação na logística da entrega?
Obs.: Senti falta de alguns dados como: Dados dos entregadores (id, número de entregadores durante os dias da semana), Taxa cancelamento do pedido.

5 - Se você fosse dono(a) de um restaurante, o que você sugeriria para o iFood melhorar a operação logística tendo em vista os dados fornecidos? Por quê?

R.: 
Pelos dashs “Pedidos atrasados-entregador por dia” e “Pedidos atrasados-entregador por dia %” verificamos que nos dias 07/04/2020 (1687 pedidos; 8,83% de pedidos atrasados pelos entregadores pela quantidade de pedidos total no período) e 12/04/2020 (1969 pedidos; 8,14% de pedidos atrasados pelos entregadores pela quantidade de pedidos total no período) foram os dias que mais tiveram atrasos pelos entregadores, neste caso, como dono de um restaurante, sugeriria ao Ifood deixar claro no app quando foi o entregador que gerou atraso para evitar que avaliações ruins atrapalhem pedidos no restaurante.
Já no dash “Tipo de rota mais eficaz” notamos que na modalidade “Single Pick Multi Drop” as métricas “media_distancia_km” e “media_tempo_entrega_real_min” estavam maiores do que na modalidade “Single Pick Single Drop” em compensação as quantidades de atraso na modalidade multi foram bem menores, neste caso, sendo dono de um restaurante, sugeriria ao Ifood que determine rotas mais rápidas e eficientes junto aos entregadores, que contemplem a integração de entregas ou coletas na mesma viagem/entrega complementar (multi drop). 

Obs.: Para o tipo de rota “Single Pick Multi Drop” senti falta do dado da quantidade de entregas feita dentro de cada entrega “multi drop” para dividir o tempo e distância e confirmar efetividade nessa modalidade de entrega.

Link: https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/6605712877054562/1351783805753811/6665719610652/latest.html

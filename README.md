# FraudShield
## Machine Learning Model for Credit Card Fraud Detection
Este projeto tem como objetivo desenvolver um modelo de aprendizado de máquina capaz de prever fraudes em cartões de crédito utilizando dados históricos de transações que incluem informações como data, hora, valor, localização, tipo de transação, informações do titular do cartão, entre outros.

Para isso, um algoritmo de classificação como Random Forest ou KNN será aplicado para treinar o modelo com os dados históricos. Durante o treinamento, serão utilizadas técnicas de validação cruzada e ajuste de hiperparâmetros para garantir que o modelo seja robusto e tenha bom desempenho.

Finalmente, o modelo será avaliado utilizando um conjunto de dados de transações de cartão de crédito não vistos anteriormente, e suas previsões serão comparadas com as transações reais. Métricas de avaliação como precisão, recall e pontuação F1 serão usadas para avaliar o desempenho do modelo.

O projeto será implementado em Python, utilizando bibliotecas populares de aprendizado de máquina como Scikit-learn e Pandas para facilitar a análise de dados e implementação do modelo.

Vários modelos de aprendizado de máquina foram desenvolvidos para detecção de fraudes em cartões de crédito e, neste cenário bancário, o recall é a principal métrica a ser analisada porque os bancos querem identificar todos os casos de fraude, evitando compensação ao cliente.

Entre os modelos, há um modelo Random Forest desequilibrado, que obteve uma precisão de 0,79 e recall de 0,66. Também há um modelo desenvolvido com a técnica de subamostragem (Near miss), que obteve uma precisão de 0,11 e recall de 0,84. Por fim, o modelo desenvolvido com sobreamostragem obteve uma precisão de 0,71 e recall de 0,73.

Cada modelo apresenta resultados diferentes, e o gerente do banco deve analisá-los cuidadosamente antes de decidir qual modelo é mais apropriado para suas necessidades. Se o banco quiser identificar o maior número possível de fraudes, mesmo que isso resulte em identificar transações legítimas como fraudulentas, então o modelo com maior recall (Near miss) pode ser a melhor escolha.

Por outro lado, se o banco quiser minimizar o número de falsos positivos e garantir que a maioria das transações fraudulentas identificadas sejam de fato fraudulentas, então o modelo mais adequado seria o modelo de sobreamostragem.

Independentemente do modelo escolhido, é importante observar que nenhum modelo é 100% preciso. Portanto, a melhor abordagem pode ser usar o modelo como uma ferramenta para aplicar uma segunda camada de identificação às transações que são julgadas como fraudulentas pelo modelo. Assim, o banco pode garantir que a maioria das transações suspeitas seja identificada e avaliada antes de serem concluídas.

Simulação com o modelo Near Miss (recall 0,84)

Sabendo que o valor total de perda do banco é de 5121413,29, identificar e prevenir 84% dessas transações seria equivalente a economizar 4301987,16.
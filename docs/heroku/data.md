# Dados no Heroku

[Heroku - Data](https://data.heroku.com/)

Podemos pensar em um aplicativo Heroku como um conjunto de microsserviços. Ou seja,
haverá os Dynos para a aplicação web, o add-on PostgreSQl para
gerenciar o banco de dados e também há a possibilidade de adicionar algo a mais
(por exemplo, um microsserviço de pesquisa de dados).

Em resumo, para todos os dados do deploy, deve-se usar a parte de dados do Heroku.

## Dashboard

Aqui haverá informações sobre o aplicativo e as suas definições. 

<b>Atenção:</b> é muito importante ver
as variáveis de ambiente e sempre mantê-las em segredo! Pois elas possuem papel importantíssimo no funcionamento do aplicativo.

## Datastores

Aqui, haverá uma lista dos bancos de dados para adicionar ao seu aplicativo, com seus tipos e outras muitas opções.

Você também terá a opção de alterar o tamanho do banco de dados, ver a quantidade de tabelas disponíveis, etc.

## Dataclips

Dataclips são linhas de comando SQL. Na verdade, seu objetivo é criar, modificar ou excluir linhas do banco de dados.

Para obter mais informações, vá para a parte <a href="../../database/queries">SQL</a> da documentação.

## Documentação
[Documentação do Heroku](https://devcenter.heroku.com/)

<hr>
Para mais informações:

[Heroku - Dados](https://data.heroku.com/)

[Heroku - Suporte](https://help.heroku.com/)
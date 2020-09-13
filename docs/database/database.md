
# Base de dados

O objectivo deste arquivo é explicar as principais relações da base de dados; a base de dados principal, as suas tabelas, a forma como os dados são armazenados e dar uma imagem global da nossa base de dados.

A aplicação do website da Hollow contém diferentes modelos, que são implementadas em arquivos do tipo `models.py`.

Se quiser criar um novo modelo, terá de o fazer neste arquivo.

Para mais informações sobre bases de dados Django, consulte por favor a [`documentação`](https://docs.djangoproject.com/en/3.0/topics/db/models/) 

## Especificações

Serviço: heroku-postgresql

- PLANO : [standard-0](https://devcenter.heroku.com/articles/heroku-postgres-plans)
- Aplicação de facturação: 

- Região: 
- Primário: 
- Versão : 
- Criação : 
- Cópias de segurança: 
- Tabelas: 
- Usando : 

## Comandos com Heroku ##

Utilize o [Heroku CLI](https://devcenter.heroku.com/articles/heroku-command-line) para aceder aos registos a partir da linha de comando.
```bash 
heroku logs --tail --ps postgres --app {app_name}
```

Para se ligar à base de dados (OBS: É melhor utilizar o DataGrip)
```bash 
heroku psql --app {app_name}
```

Para recuperar as referências do banco
```bash
heroku pg:credentials:url --app {app_name}
```

Ajuda para exibir informação de base de dados
```bash
heroku pg --app {app_name} --help
```

Para mais informações
```bash
heroku help
```

## Ficha técnica

Os `dataclips` são essencialmente consultas SQL que podem ser partilhadas com os colegas através de Heroku.
Se tiver uma query em SQL que gostaria de partilhar com a equipa, sinta-se à vontade para a acrescentar [aqui](https://data.heroku.com/dataclips).


- Para mais informações, por favor visite [documentação](https://devcenter.heroku.com/articles/dataclips)

## Tabelas
Para visualizar as tabelas e as suas relações, podemos utilizar o DataGrip e exportá-las em formato pdf. 

Para encontrar o diagrama de relações, basta ir à pasta "tabelas", clicar com o botão direito do mouse e seleccionar "Diagramas" e "Ver Vista", ou usar o atalho "Ctrl+Alt+Shift+U".


## Relacionamentos
Na teoria das bases de dados relacionais, existem 3 tipos principais de relações:

1. Um-para-um (um-para-um):
Uma linha num campo da tabela está relacionada apenas com um outro elemento da tabela.
Por exemplo, temos as relações "membro" e "utilizador". O membro e o utilizador devem ser a mesma pessoa. Representam então um único elemento.

2. "Um a muitos (1 - n)": um elemento de um campo numa tabela pode ser ligado a vários outros elementos de outra tabela.
Por exemplo, temos relações de "cidade" e "país". Uma cidade pode ter apenas um país, mas um país pode ter várias cidades.

3. "Muitos para muitos (n - n)": a relação de pluralidade é para trás e para a frente. Por exemplo, "utilizador" e "evento". 
Um utilizador pode ter vários eventos e um evento pode ter vários utilizadores.

## Como armazenar dados

O armazenamento de dados é muito importante. Temos de considerar os seguintes aspectos 
acrescentando dados à base de dados BRASA:

1) ``Dados actuais``: processar sempre dados actuais.
2) `Integridade dos dados`: os dados devem ser completos, não corrompidos ou incompletos.
3) `Limpeza de dados`: os dados devem estar limpos, nenhuma informação deve ser acrescentada a nada.
4) ``Padronização dos dados``: Os dados devem ser padronizados. A mesma coluna da base de dados não deve ser utilizada.
para dados que pertencem a dois tipos diferentes de formatação.
5) `Consistência dos dados`: os dados devem ser coerentes. Do ponto de vista da homogeneidade, consistência e firmeza. 
Não se deve trabalhar com dados que estejam ou venham a estar quebrados no futuro.

Use o comando :
```
Command:     INSERT
Description: create new rows in a table
Syntax:
[ WITH [ RECURSIVE ] with_query [, ...] ]
INSERT INTO table_name [ AS alias ] [ ( column_name [, ...] ) ]
```

Para mais informações :

- Vídeo SQL : [CS50 SQL](https://www.youtube.com/watch?v=u5pDdEKnbKA)

- Folha de dados SQL e outras informações : [w3schools SQL](https://www.w3schools.com/sql/sql_ref_keywords.asp) 



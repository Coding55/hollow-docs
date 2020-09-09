# O Aplicativo Hollow
[Dashboard - Heroku](https://dashboard.heroku.com)

O link para um aplicativo no Heroku é ``https://dashboard.heroku.com/apps/{app-name}``, onde o nome do aplicativo
deve ser substituído pelo ``{app-name}``.

<b>Atenção:</b> A URL real não possui as chaves ``{}``!

## Overview
Nesta parte, você terá as informações gerais do aplicativo. Dynos, add-ons (com postgres), atividade dos colaboradores (desenvolvedores responsáveis pela manutenção do app) e
o histórico de deploys, onde poderemos as mudanças no aplicativo.

## Resources
Nos recursos, você verá um resumo de todos os microsserviços que estão sendo executados. Assim, você verá o preço que deve ser pago a cada mês.

## Deploy
Na implantação, você terá todas as informações para realizar implantações (deploys). Na verdade, você tem opções para realizar essas implantações. Utilizando ``git push`` ou implantações automáticas com a integração ``GitHub``. Ainda assim, você pode usar a [`Heroku CLI`: Heroku command line interface](https://devcenter.heroku.com/articles/heroku-command-line) para ajudar em suas implantações.

## Metrics
Se você deseja adicionar métricas para o aplicativo, é aqui onde você deve mexer. É uma boa maneira de ver como os usuários estão utilizando a plataforma.

## Activity
É um histórico de todas as atividades e implementações.

## Access
Aqui, você verá as pessoas que têm direitos para alterar o aplicativo e realizar outras implantações.

## Settings
Esta é a parte para alterar e adicionar configurações no aplicativo.

Não hesite em vir aqui e mudar o que quiser.

Na verdade, as partes importantes são:

- <b>App Informations</b>: para alterar o nome do aplicativo.
- <b>Config Vars</b>: para gerenciar variáveis de ambiente.
- <b>Buildpacks</b>: scripts que serão executados.
- <b>Certificados SSL</b>: certificado para utilizar HTTPS.
- <b>Domains</b>: adicionar domínio (não <em>herokuapp.com</em>).
- <b>Maintenance Mode</b>: usado quando você deseja alterar algo no site (o aplicativo será desligado).


<hr>

Para mais informações:
[Dashboard - Heroku](https://dashboard.heroku.com)
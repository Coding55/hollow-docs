# Implantação
A implantação do site da **Hollow** e todas as atividades que tornam o serviço web disponível para uso.

As fases da atividade de implantação são:

1. ``Liberação``: Às vezes, isso envolve determinar os recursos necessários para que o sistema opere com desempenho e planejamento toleráveis ​​e / ou documentar atividades subsequentes no processo de implantação. Então, você tem que saber o tamanho dos aplicativos que serão definidos com o Heroku.

2. ``Instalação e ativação``: É feito com o Heroku. Fazemos o 'push' do branch `local/production` (que deve ser testado) como` heroku/master`.

3. ``Desativação``: A prática de remover do serviço sistemas usados ​​com pouca frequência ou obsoletos é frequentemente referida como aposentadoria ou solicitação de downgrade. Não há necessidade em nosso caso.

4. ``Desinstalação``: É a remoção de um sistema que não é mais necessário. Não precisamos disso em nosso caso.

5. ``Atualizar``: Normalmente consiste na desativação seguida pela instalação. É preciso um desenvolvedor para manter novas versões do Django e Python.

6. ``Atualização integrada``: atualização do Windows ou equivalente. Isso não se aplica ao nosso caso.

7. ``Monitoramento de versão``: Realizado em ``requirements.txt``.

## Lista de verificação de implantação do Django

Antes de implantar o aplicativo, você precisa saber se ele é adequado para uso na vida real com pessoas da **Hollow**.

Para fazer isso, você deve executar o comando:

```` shell
python manage.py check --deploy
````

Este comando verificará a estabilidade do aplicativo. Corrigimos alguns problemas, mas se você adicionar outro recurso, terá que executar dita verificação.

Para obter mais informações sobre a lista de verificação do Django (recomendamos a leitura):

[Link para a lista de verificação para a implantação do Django ](https://docs.djangoproject.com/en/3.0/howto/deployment/checklist/)

## Verificação de produção

A ``verificação de produção`` (_Production check_) é um recurso do Heroku para saber se sua aplicação está bem implementada.

Os pontos a verificar são:

1. Heroku-18 Stack
2. Contêineres[^1] típicos (recomendamos Contêineres pagos, dado seu uso)
3. Falhas na Redundância dos contêineres
4. Falhas no Banco de dados de Postgres de produção
5. Alta disponibilidade de Postgres
6. Monitoramento do aplicativo em caso de falha
7. Monitorar o registro de falhas
8. Páginas de manutenção personalizadas
9. Heroku SSL

[^1]: No Heroku os contêineres são chamados de "Dynos" em inglês.

Para o servidor de produção, é recomendável ter configurações bem gerenciadas.

## Implantação com heroku

Para obter mais informações sobre a implantação com Heroku, o link para a documentação é:

[Deployment - Heroku](https://devcenter.heroku.com/categories/deployment)

## Preparando uma base de código para a implantação do Heroku

[Preparando uma base de código[^2] para implantação Heroku](https://devcenter.heroku.com/articles/preparing-a-codebase-for-heroku-deployment)

[^2]: Base de código: _codebase_ em inglês.
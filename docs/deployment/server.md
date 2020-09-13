# Servidor

Para gerenciar o servidor, é recomendado que o responsável assista ao [tutorial de uso do python com heroku](https://devcenter.heroku.com/articles/getting-started-with-python), ele contem muitos conceitos importantes para gerenciar o aplicativo.

## Ver os arquivos de log

O Heroku trata os logs (arquivos de log) como fluxos de eventos ordenados por tempo agregados a partir dos fluxos de saída de todos os aplicativos e os componentes do Heroku, fornecendo um único canal para todos os eventos.

Veja informações sobre o seu aplicativo em execução usando um dos comandos `heroku logs --tail`

## Escala de aplicação

Você pode verificar quantos contêineres[^1] estão em execução usando o comando `ps`:
[^1]: No Heroku os contêineres são chamados de "Dynos" em inglês.

```` shell
$ heroku ps
Free dyno hours quota remaining this month: 999h 6m (99%)
Free dyno usage for this app: 0h 0m (0%)
For more information on dyno sleeping and how to upgrade, see:
https://devcenter.heroku.com/articles/dyno-sleeping

=== web (Free): gunicorn gettingstarted.wsgi (1)
web.1: up 2018/10/12 14:26:45 -0500 (~ 33s ago)
````

Por padrão, seu aplicativo é implantado em um contêiner gratuito. Os mesmos serão desativados após meia hora de inatividade (se não estiverem recebendo tráfego). Isso causa um atraso de alguns segundos para a primeira solicitação de ativação. As solicitações subsequentes funcionarão normalmente. Os contêineres grátis também consomem de uma cota mensal gratuita do contêiner - desde que a cota não seja usada, todos os aplicativos gratuitos podem continuar a funcionar.

Para evitar a desativação do contêiner, você pode mudar para um profissional ou tipo de contêiner conforme descrito no artigo [Tipos de contêiner](https://devcenter.heroku.com/articles/dyno-types). Por exemplo, se você está migrando seu aplicativo para um contêiner profissional, pode escalá-lo facilmente executando um comando que diz ao Heroku para executar um número específico de contêineres, cada um executando seu tipo de processo da web.

O dimensionamento de um aplicativo no Heroku é equivalente a alterar o número de contêineres em execução.

Escala do número de contêineres da web até zero:

```` shell
heroku ps:scale web=0
````

Escale novamente:
```` shell
heroku ps:scale web=1

````

## Inicie um console

Você pode executar qualquer comando, geralmente scripts e aplicativos que fazem parte do seu aplicativo, em um único contêiner usando o comando `heroku run`. Ele também pode ser usado para iniciar um processo REPL anexado ao seu terminal local para experimentar em seu ambiente de aplicativo:

````shell
$ heroku run python manage.py shell
Python 3.7.6 (default, Dec 23 2019, 04:25:22)
[GCC 7.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
(InteractiveConsole)
>>>
````

Se você receber um erro de ``Erro ao conectar ao processo``, pode ser necessário configurar seu firewall.

O shell Python está sendo executado no contexto de seu aplicativo e todas as suas dependências. De lá, você pode importar alguns dos arquivos do seu aplicativo.

Para ter uma ideia real de como o contêiner funciona, você pode criar outro contêiner exclusivo e executar o comando, que abre um shell naquele contêiner. Você pode então executar comandos lá. Cada contêiner tem seu próprio espaço de arquivo efêmero, preenchido por seu aplicativo e suas dependências. Nesse caso, assim que o comando for concluído, o contêiner será excluído.

````shell
$ heroku run bash
Running `bash` attached to terminal... up, run.3052
~ $ ls 
gettingstarted  hello  manage.py  Procfile  README.md  requirements.txt  runtime.txt  staticfiles
~ $ exit
exit
````

Não se esqueça de digitar 'exit' para sair do shell e encerrar o contêiner.
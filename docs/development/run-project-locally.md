Fazer o clone do repositório na sua maquina local : 
```bash
$ git clone https://coding55@dev.azure.com/coding55/hollow-website/_git/hollow-website
```

Migrar o banco de dados : 

```bash
$ python manage.py makemigrations 

$ python manage.py migrate --noinput
```

Iniciar um servidor Django : 

```bash
$ python manage.py runserver
```

Agora você deve ter a sua aplicação em [localhost](http://127.0.0.1:8000) no seu navegador. 


Quando quiser sair, não se esqueça de fechar o servidor : 

```bash
Quit the server with CTRL-BREAK
(In Windows) Ctrl + C
```

# Arquivos Estáticos

O Heroku não permite o armazenamento de arquivos estáticos no sistema, tais quais CSS ou imagens, por exemplo. 
 
<b>Info:</b> ``Ubuntu 18.04 LTS`` é o sistema.

É por esse motivo que usaremos o serviço S3 do Amazon AWS. Na verdade, só é necessário criar um ``bucket``
para armazenar arquivos. Um ``bucket`` é como uma pasta online para armazenar arquivos. O aplicativo possui todo o código necessário para integrar um bucket com os serviços compatíveis com o Django.

<hr>

Para mais informações:

[Amazon S3](https://aws.amazon.com/s3/)

[Prix - Amazon S3](https://aws.amazon.com/s3/pricing/)

[Amazon AWS](https://aws.amazon.com/)
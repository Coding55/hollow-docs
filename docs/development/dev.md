# Branch `develop`

No projeto Azure DevOps da aplicação, o branch em que o desenvolvimento será feito é a branch __dev__.

Quando você quiser modificar o código da aplicação, você precisa :

* Criar uma branch __nova__ (com um nome explícito, se possível, relacionado com as mudanças que serão feitas ali).

* Uma vez feitas as mudanças neste novo branch, o `commit` deve ser formado com um título explícito e uma breve descrição do trabalho realizado na branch.

* Depois é feito um pedido de __pull request__

* Uma vez que todos os desenvolvedores tenham assegurado que não haja conflito entre o novo código e o código existente, podemos __fundir__ a nova branch na branch __dev__.


***É fortemente recomendado não modificar diretamente a branch dev, caso contrário podem ser introduzidos erros no código, cuja origem não pode ser conhecida a priori.

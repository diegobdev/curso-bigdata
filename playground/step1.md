Primeiro, vamos baixar a versão mais recente da imagem do Jenkins em seu repositório oficial no Docker Hub.

Iremos executar o seguinte comando para 'puxar' a imagem do repositório Jenkins no Docker Hub, para nossa máquina local:

`docker pull jenkins`{{execute}}

Após executar o comando acima, conseguiremos ver que o Docker trabalha com o conceito de 'layers', com isso, veremos que ele fará o download localmente de cada parte da imagem e depois se encarregará de juntar todas essas camadas.

O resultado esperado do comando acima é:

`$ Status: Downloaded newer image for jenkins:latest`

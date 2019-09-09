Agora que o container foi criado, vamos acessá-lo.

Primeiro, vamos verificar se o container está em execução, executando o seguinte comando:

`docker ps`{{execute}}

Este comando lista todos os contêineres que estão atualmente ativos. É possível vermos que no passo anterior o hash exibido para nós será exibido em nossa listagem atual, de forma abreviada. (ex.: de acordo com o hash exibido no passo anterior, em nossa listagem do docker ps o campo 'CONTAINER ID' mostrará '926e5a17c703'.

Agora, é hora de fazer login executando:

`docker exec -it $(docker ps -q) bash`{{execute}}

Sobre o comando executado, vamos ver o que cada parte se refere:

*docker exec*: Executar um comando em um contêiner em execução.

*-it*: permite acessarmos o container no modo interativo e com possibilidade de uso do terminal

*$(docker ps -q)*: comando para retornar o ID do container que está rodando - como neste momento só temos 1, ele será retornado. No lugar deste comando podemos colocar manualmente o ID do container.

*bash*: Executa um shell bash no container.

Agora, estamos logados em nosso container como um usuário root.

O resultado esperado é que estejamos logado no container, sua linha de digitação de comando deve ter mudado para algo como:
`root@90b6acd7681c:/#`
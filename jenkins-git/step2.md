Na etapa anterior, baixamos a imagem do Jenkins do Docker Hub. Então agora é hora de executar um contêiner com base nessa imagem.

Para fazer isso, usaremos o run, através do seguinte comando:

`docker run -d -u root -p 80:8080 jenkins`{{execute}}

No comando que executamos, colocamos alguns parâmetros:

*-d: detached* - Executar contêiner em modo separado.

Esse parâmetro faz com que o Docker inicie o contêiner no modo "desanexado".

Uma maneira simples de pensar nisso é pensar em executar o contêiner em "segundo plano", como qualquer outro processo Unix. Em vez de 'sequestrar' o terminal e mostrar a saída do aplicativo, o Docker iniciará o contêiner no modo desanexado.

*-u: user* - É o usuário padrão dentro de um contêiner. O desenvolvedor da imagem pode criar usuários adicionais, que são acessíveis por nome. Neste caso, usaremos 'root'.

*-p: publish* - Publique as portas de um contêiner no host.

Usamos o parâmetro -p para publicar a porta 8080 do host para o contêiner na porta 80 no contêiner.

Isso significa que qualquer pessoa que se conecte a esse host pela porta 8080 será roteada para o contêiner pela porta 80.

*jenkins*: Nome da imagem base para executar este contêiner.

Por padrão, quando uma tag/versão não é passada o próprio docker se encarregará de buscar a imagem pela tag 'latest'.

Depois de executar este comando, um novo contêiner será criado e seu ID do contêiner será impresso no terminal. O resultado esperado após o comando é o ID do container (sha hash) que está sendo executado, como por exemplo:
`$ 926e5a17c7034472af9d8945121ca807799bb5d135490c2a5c28531a68b7f0a3 (ID de exemplo)`
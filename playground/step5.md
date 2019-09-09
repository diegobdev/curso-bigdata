Primeiro, iremos `desbloquear` Jenkins. Para isso, precisamos a senha de admin gerada por ele.

Como mostra na tela, ele é escrito por padrão em `/var/jenkins_home/secrets/initialAdminPassword` neste local em seu contêiner.

Para obter a senha, vamos exibi-la no terminal, com o seguinte comando:

`cat /var/jenkins_home/secrets/initialAdminPassword`{{execute}}

Copie a senha exibida e cole-a na caixa de texto na página do Jenkins que abrimos no passo anterior, depois pressione 'Continue'.
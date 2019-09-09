Como este cenário é sobre como podemos usar o Git com o Jenkins para construir continuamente o 'alvo' com base nos *commits* feitos no repositório no GitHub, você deve ter uma conta no GitHub (é gratuito). **Se você jã possui, pode acessá-la em uma nova aba, e se você ainda não tem, crie uma conta em [github.com](https://github.com/).**

Depois de fazer login na sua conta do GitHub, **crie um novo repositório**, clicando em + no canto superior direto e quando a página carregar, dê um nome para ele no campo "Repository name".

Voltando ao Terminal, se não estiver logado no container, faça o login com: `docker exec $(docker ps -q) bash`

Para este cenário, já configuramos o Git nesta máquina.

Você pode verificar se eles estão instalados por:

`git --version`{{execute}}

Deverá aparecer a versão do Git instalada.

---
#### Configurando o Git

Primeiro, iremos definir a configuração inicial do Git em nosso container. Para fazer isso, digite no terminal:

- `git config --global user.email "nome@exemplo.com"` (seu e-mail de login no github)
- `git config --global user.name "usuário"` (um nome de usuario para identificação de commits e pushes)
*Substitua a string 'nome@exemplo.com' pelo seu e-mail e a string 'usuário' pelo seu nome de usuário.*

Agora, iremos clonar um repositório de exemplo deste laboratório onde contém um script simples escrito em python que usaremos em nossa demonstração. Para isso, execute o seguinte comando:

- `git clone https://github.com/diegobdev/treinamento-bigdatasystems-cicd.git`{{execute}}

Para que possamos trabalhar no nosso ambiente de desenvolvimento (na aplicação), vamos navegar até o diretório que 'clonamos' com o seguinte comando:

`cd treinamento-bigdatasystems-cicd`{{execute}}

Neste momento, temos que trocar a URL remota do repositório clonado para a URL do repositório que foi criado na sua conta (no começo deste passo), faça isso com o seguinte comando:

`git remote set-url origin URL`

(substitua `URL` para a url seu repositório - ela termina com final *.git*)

Agora, envie este repositório local para o seu repositório remoto:

`git push`{{execute}}

Agora você tem seu repositório pronto para ser integrado ao Jenkins, se você abrir seu repositório no GitHub e atualizar a página, verá que seu repositório já possui os arquivos clonados.

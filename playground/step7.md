Após a configuração, você será levado para o Jenkins Dashboard.

Antes de instalarmos o(s) plugin(s) necessários, como Git, vamos atualizar a versão do Jenkins e reiniciá-lo para evitar conflitos.

**No menu a esquerda, clique em *Gerenciar Jenkins*** e depois que a página carregar, clique no botão **'Atualizar automaticamente'**.
Neste momento, abrirá uma tela de confirmação onde **selecionaremos a opção 'reiniciar assim que finalizar'**.

Você será desconectado e em alguns segundos pode atualizar a página para recarregar o Jenkins.

Quando a página recarregar, será solicitado o login de acesso.
- Em *username*, digite `admin`;
- Em password, digite a senha que havíamos copiado no Step 5 (comando *cat*).

Agora, para nosso cenário, temos que configurar e instalar o plugin Git.

---
Agora, vamos instalar o Plugin Git para Jenkins.

- **Clique em Gerenciar Jenkins** no menu esquerdo.
- **Clique em Gerenciar Plugins** na próxima página.
- **Selecione a guia Disponível** na página Gerenciador de plugins.
- No campo superior a direita, **digite `Git`** e pressione 'Enter' para pesquisar.

(Diversos plugins serão exibidos, para facilitar a localização do plugin que precisamos nesta página, **busque (ctrl+f no browser)** pelo texto **'This plugin integrates Git with Jenkins.'**

- **Marque a caixa antes do plugin do Git (o nome do plugin é 'Git')**.

- **Clique em 'Instalar sem reiniciar'**.

O Jenkins baixará e instalará o plugin selecionado, assim como suas dependências.

Quando o download estiver concluído e aparecer 'Sucesso' após cada plugin - as instalações e configurações terão sido finalizadas.


É isso aí! Você terminou com as configurações.

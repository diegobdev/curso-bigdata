Se você se lembra, nós selecionamos uma expressão cron para checar qualquer mudança no repositório Git a cada minuto.

Agora, faça qualqer alteração na mensagem do arquivo `example.py` em nossa cópia local do repositório, depois, envie-a para o repositório remoto (commit + push) e observaremos nosso Job Jenkins para ver que está sendo acionado após uma alteração feita no repositório remoto.

**Para fazer isso:**

- Faça o login no seu container
- Vá para o seu repositório local (treinamento-bigdatasystems-cicd)
- Faça alguma alteração no arquivo example.py
- Agora, envie as alterações para o repositório remoto (git add, commit e push).

Caso não esteja seguro de realizar essa alteração localmente para enviar, você pode alterar o arquivo diretamente na console do GitHub em seu repositório.

Depois que as alterações forem enviadas ao repositório remoto, poderemos observar a seção Histórico de construção do painel do nosso projeto.

Depois de esperar por alguns segundos, você observará um novo trabalho iniciado em execução na seção 'Build History'.

Isto acontece porque Jenkins verifica continuamente as mudanças no repositório dado. A expressão Cron especificada que informamos, verifica as alterações a cada minuto no repositório remoto, e neste momento, ele acionará automaticamente uma nova compilação.

Pronto! Você integrou com sucesso Jenkins com o Git neste tutorial.

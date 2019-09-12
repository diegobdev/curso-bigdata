Se você se lembra, nós selecionamos uma expressão cron para checar qualquer mudança no repositório Git a cada minuto.

Agora, faremos uma alteração da mensagem 'printada' no arquivo `example.py` em nossa cópia local do repositório. Depois, envie-a para o repositório remoto (commit + push) e observaremos nosso Job Jenkins para ver que está sendo acionado após uma alteração feita no repositório remoto.

**Para fazer isso:**

- Faça o login no seu container (se não estiver mais logado);
- Vá para o seu repositório local (pasta treinamento-bigdatasystems-cicd)
- Trocaremos o conteúdo do arquivo example.py com o seguinte comando:
  - `echo "print('BigData Systems')" > example.py`
- Agora, envie as alterações para o repositório remoto (`git add .`, `git commit -m "change echo message"` e `git push origin master`).

Depois que as alterações forem enviadas ao repositório remoto, conseguiremos observar a seção 'Histórico de construção' no painel do nosso projeto, dentro do Jenkins.

Depois de alguns segundos, veremos um novo trabalho iniciado em execução na seção 'Build History'.

Isto acontece porque Jenkins verifica continuamente as mudanças no repositório dado.
A expressão Cron especificada que informamos, verifica as alterações a cada minuto no repositório remoto, e neste momento, ele acionará automaticamente uma nova compilação.

Pronto! Você integrou com sucesso Jenkins com o Git neste tutorial.

Agora, vamos criar um novo trabalho (job) no Jenkins.

**Vá para o painel do Jenkins:**

- Clique em Novo job
- Digite um nome para o novo job na caixa de texto.
- Clique na primeira opção de projeto (Construir um projeto de software free-style)
- Clique OK

Um novo projeto será criado e você será redirecionado para a página de configuração do projeto.

**Aqui, vamos definir o Git como nosso gerenciamento de código-fonte. Para fazer isso:**

- Selecione Git na seção Gerenciamento de código-fonte.
- Digite o URL do seu repositório na caixa de texto
- Mantenha todas as outras opções como estão.

**Na seção Trigger de Construção (ou Trigger de Build):**
- Marque a opção de Poll SCM (ou Consultar periodicamente o SCM)
- Digite a expressão cron no campo de texto:
```* * * * *```


***(Expressão cron, pode ser resumido em "agendador de tarefas baseado em tempo em sistemas operacionais", neste caso: verificar o repositório para uma possível mudança a cada minuto)***


**Agora vamos adicionar o passo de construção. Para fazer isso:**
- Clique no dropdown Add Build Step na seção Build.
- Selecione a opção Executar Shell.
- Digite seguinte no campo de texto:
```
cd /treinamento-bigdatasystems-cicd
python example.py
```

- Clique em Apply
- Clique em Salvar

**Você pode ver a primeira construção na seção Histórico de construções. Para ver a saída:**

- Clique no #1
- Clique na saída do console (menu da esquerda)

Pronto! Você pode ver a saída do programa `example.py` na saída do console.


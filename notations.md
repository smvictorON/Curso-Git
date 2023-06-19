*** Controle de versão ***
é uma tecnica para gerenciar código fonte em que cada desenvolvedor
pode trabalhar em uma versão do mesmo projeto, isso é chamado
controle de versão, que ajuda a organização de um projeto!

*** Git ***
é o sistema mais utilizando para controle de versão, baseado em
repositórios, com operações otimizdas e criptografadas, o git tbm é
um projeto open source.

*** Github ***
é um serviço para gerenciar repos, gratuito e amplamente usado nas
empresas.

*** Repo ***
é onde nosso código fonte fica, e por ser enviados para plataformas
que gerenciam repos como Github e Bitbucket

para criar um repo basta executar:
`git init`

após a execução uma pasta oculta chamada .git vai ser criada na
pasta e o git vai reconhecer a pasta com o um repositório


### COMANDOS

`git init`
Inicializa um repositório Git em um diretório.

`git clone <URL>`
Clona um repositório Git existente para o seu ambiente local.

`git add <arquivo>`
Adiciona um arquivo específico ao índice (staging area) para ser commitado.

`git add .`
Adiciona todos os arquivos modificados e novos ao índice.

`git commit -m "<mensagem>"`
Realiza um commit dos arquivos adicionados no índice com uma mensagem descritiva,
podemos commit um arquivo de cada ver deixando explicito no comando
`git commit <arquivo.extensao> -m "<mensagem>"`
ou commitar varios arquivos de uma vez só utilizando o -a(all)
`git commit -a -m "<mensagem>"`

`git status`
Mostra o status atual do repositório, incluindo os arquivos modificados, adicionados e commitados.

`git push`
Envia os commits locais para um repositório remoto.

`git pull`
Atualiza o repositório local com as alterações mais recentes do repositório remoto.

`git branch`
Lista todas as branches disponíveis no repositório.

`git branch <nome_branch>`
Cria uma nova branch.

`git checkout <nome_branch>`
Altera para a branch especificada.

`git merge <nome_branch>`
Incorpora as alterações da branch especificada na branch atual.

`git remote add <nome_remoto> <URL>`
Adiciona um repositório remoto ao seu ambiente local.

`git log`
Mostra um histórico de commits.

`git diff`
Mostra as diferenças entre o código atual e o último commit.

`git rm <arquivo.extensao>`
Deleta um arquivo do repositório.

`git mv <arquivo.extensao> <local><arquivo.extensao>`
Move/Renomeia um arquivo do repositório, o monitoramento do arquivo antigo é
perdido e ele começa um para o novo arquivo.

### OBSERVAÇÕES

- antes o padrão de nome para a branch princial era 'master', mas o
github mudou esse paradrão para 'main'.

- um arquivo novo é tratado com "untracked" e fica com a letra U na
frente do nome do arquivo, `git add` para adiciona-lo ao controle de
versão.

- um arquivo modificado é tratado como "not staged" e fica com a letra
M na frente do nome do arquivo, `git add` para adiciona-lo ao controle de
versão.
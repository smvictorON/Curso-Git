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
que gerenciam repos como Github e Bitbucket.

para criar um repo basta executar:
`git init`

após a execução uma pasta oculta chamada .git vai ser criada na
pasta e o git vai reconhecer a pasta com o um repositório.

*** Tags ***
tags são usadas como um checkpoint, servem para demarcar um estágio do
desenvolvimento.

*** Submodulos ***
é uma maneira de possuir dois ou mais projetos em um só repo.

*** Markdown ***
é uma maneira de inserir estilos para textos na web.

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

`git branch -d <nome_branch>`
Deleta uma branch.

`git checkout <nome_branch>`
Altera para a branch especificada, adicionando o `-b` antes do nome da branch
se ela nao existir ele cria e depois muda para ela, o checkout de outra branch
não leva os commits feitos, mas leva os arquivos modificados.

`git checkout <local>/<arquivo.extensao>`
Altera o arquivo para o estado inicial, igual ao do remote.

`git merge <nome_branch>`
Incorpora as alterações da branch especificada na branch atual.

`git remote add <nome_remoto> <URL>`
Adiciona um repositório remoto ao seu ambiente local.

`git log`
Mostra um histórico de commits.

`git shortlog`
Mostra um histórico resumido de commits.

`git diff`
Mostra as diferenças entre o código atual e o último commit, mas tambem
pode ser especificado o arquivo e tambem branchs diferentes.

`git rm <arquivo.extensao>`
Deleta um arquivo do repositório.

`git mv <local>/<arquivo.extensao> <local>/<arquivo.extensao>`
Move/Renomeia um arquivo do repositório, o monitoramento do arquivo antigo é
perdido e ele começa um para o novo arquivo.

`git reset --hard`
Limpa todos os commits feitos e arquivos modificados deixando a branch local
igual a branch remote.

`git stash`
Volta ela para o estado sem modificações e salva as modificações no stash da branch
para poder ser usado depois.

`git stash list`
Lista as stashs.

`git stash apply <nome_stash>`
Recupera os mudanças da stash para a branch.

`git stash show -p <nome_stash>`
Mostra o código modificado que tem na stash.

`git stash clear`
Apaga todas as stashs do branch atual.

`git stash drop <nome_stash>`
Apaga uma stash especifica.

`git tag -a <nome_tag> -m "<mensagem>"`
Cria uma tag.

`git tag`
Mostra as tags da branch.

`git show <nome_tag>`
Mostra detalhes das mudanças, é possível tambem fazer o checkout por uma tag.

`git push origin <nome_tag>`
Manda uma tag para o repositório.

`git push origin --tags`
Manda todas nossas tags para o repositório.

`git fetch -a`
Atualiza todas as branchs e tags ainda não conhecidos.

`git submodule add <repo>`
Adiciona um submodulo(outro repo) a um repo.

`git submodule`
Visualiza os submodulos presentes no repo.

`git push --recurse-submodules=on-demand`
Atualiza o submodule.

`git show`
Mostra detalhes da branch.

`git clean -f`
Limpa/Remove todos os arquivos nao trackeados, pode ser usado para limpar
logs ou imagens que são geradas na pasta do projeto.

`git gc`
Significa Garbage Collector ele identifica e exclui arquivos que nao são mais
necessario no projeto, otimizando o repo.

`git fsck`
Significa File System Check verifica a integridade de arquivos,
otimizando o repo.

`git reflog`
Mapeia todos os passos do dev no repo, diferente do `git log` que mostra somente
informações dos commits, o reflog tem tempo de expiração de 30 dias.

`git archive --format zip --output <file_name>.zip <repo>`
Transforma o repo em um arquivo compactado.

`git rebase <branch_atual> <branch_incoming> -i`
Faz o rebase das branchs, o `-i` é para o log ficar iterativo, mostando commits e
ações, para editar basta apertar o i, o pick na frente do nome do commit significa
para o usar o commit do jeito que está com a msg igual, temos a opção de usar o
squash que é para nao levar esse commit ele vai ser colocado em outro commit
e tambem é o reword que serve para mudar a mensagem do commit, após feito as edições
apertar esc e :x! para sair do arquivo e continuar o rebase, vão ser mostradas
algumas opções sobre o que está sendo feito e novos nomes para commits, é possivel
pegar muitos commits de uma branch e unir só em um commit.
### OBSERVAÇÕES

- antes o padrão de nome para a branch princial era 'master', mas o
github mudou esse paradrão para 'main'.

- um arquivo novo é tratado com "untracked" e fica com a letra U na
frente do nome do arquivo, `git add` para adiciona-lo ao controle de
versão.

- um arquivo modificado é tratado como "not staged" e fica com a letra
M na frente do nome do arquivo, `git add` para adiciona-lo ao controle de
versão.
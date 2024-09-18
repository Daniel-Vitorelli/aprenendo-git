# PRIMEIROS PASSOS
> &nbsp;
> #### 1. VERIFICANDO A INSTALAÇÃO
> > Você pode verificar  versão instalada do seu git digitando o seguinte comando no prompt de comando:
> > ```GIT
> > git --version
>
> #### 2. INICIAR UM REPOSITÓRIO
> > Com seu projeto aberto no Visual Studio Code você devera abrir o terminal, para isso pressione **Ctrl + '**
> >
> > No seu terminal dígite o seguinte comando:
> > ```GIT
> > git init
> >```
> > Fazendo isso você tera inicializado um repositório vazio.
> >
> > Para verificar o status do seu repositório, você pode digitar o seguinte comando no terminal:
> > ```GIT
> > git status
> > ```
> > Assim tera informações de qual branch você esta, os seus commits e os seus arquivos.
> 
> #### 3. ADICIONANDO ARQUIVOS NO SEU REPOSITÓRIO
> > Com o status do seu repositório, você pode ver qual arquivo esta incluído. Para incluir um arquivo você pode escrever "git add" e depois o nome do arquivo.
> > Por exemplo, tenho um index.html mas ele não esta incluído, o código para inclui-lo seria:
> > ```GIT
> > git add index.html
> > ```
> > Se quiser adicionar tudo que pode de uma vez, pode-se usar o comando:
> > ```GIT
> > git add .
> > ```
>
> #### 4. CRIANDO UMA VERSÃO DO CÓDIGO
> > Com os arquivos preparados podemos dar o comando principal do git, que é para criar uma versão do código, o comando é "git commit -m" e depois uma descrição entre aspas. Continuando o exemplo anterior, o código ficaria assim:
> > ```GIT
> > git commit -m "Título e formulário feitos."
> > ```
> > Muito provavelmente, se for sua primeira vez fazendo isso, tera ocorrido um erro, esse erro acontece porque o git não esta vinculado a um email e a um usuário dentro de sua maquina. Para resolver isso você pode escrever o seguinte código colocando seu email no lugar de you@example.com :
> > ```GIT
> > git config --global user.email "you@example.com"
> > ```
> > E para o usuário, substitua o "Your Name" pelo seu nome de usuário:
> > ```GIT
> >   git config --global user.name "Your Name"
> > ```
> > Lembrando que este email e este nome de usuário não precisa ser o mesmo que esta no github.
> > Agora se tentar criar uma versão do código provavelmente funcionara.
> >
> > Para verificar as versões do seu projeto, ou as commits, usa-se o comando:
> > ```GIT
> >   git log
> > ```
>&nbsp;

&nbsp;

# GERENCIAMENTO DE VERSÕES
> &nbsp;
> ### 1. NAVEGANDO ENTRE VERSÕES
> > Primeiro use o git log para ver seus commits. Um deles tera (HEAD -> master) , oque tiver será oque esta selecionado.
> > Para selecionar outro commit, você pode escrever "git checkout" e depois a versão que quer.
> > Para ver todas as commits, até as que foram feitas depois da que esta selecionada, pode-se usar o comando:
> > ```GIT
> > git log --all
> > ```
> > Por fim, para voltar direto para a commit mais atualizada, se usa o comando:
> > ```GIT
> > git checkout master
> > ```
>
> ### 2. RAMIFICAÇÃO (BRANCH)
> > Se o seu código é como se fosse uma linha do tempo, e cada commit é um ponto nesta linha do tempo em que se pode visitar, o branch seria uma ramificação da linha do tempo, partindo sempre de algum ponto (commit) podendo-se assim criar novos pontos (commits) ou alterações no código sem alterar o código em produção, que é comparado a linha do tempo principal (master). A ramificação (branch) pode ter sua terminação em outro ponto (commit) da linha do tempo principal, fazendo assim, ou não, a fusão (merge) da linha do tempo ramificada (branch) com o ponto (commit) de seu termino.
>
> ### 3. CRIANDO UMA BRANCH
> > Para fazer uma branch e ja navegar para ela, deve-se estar selecionado o commit de partida da branch e digitar o seguinte comando: "git checkout -b " e depois o nome para esta branch.
> > Continuando o exemplo anteriormente citado, poderíamos criar uma branch da seguinte forma:
> > ```GIT
> > git checkout -b inscrição
> > ```
> > Para ver suas branch's pode-se usar o comando:
> > ```GIT
> > git branch
> > ```
>
> ### 4. FUNDINDO BRANCH'S (MERGE)
> >  Com o commit que você quer que seja fundido com um branch selecionado, escreva o seguinte comando: "git merge " e depois o nome da branch que quer fundir.
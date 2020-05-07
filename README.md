# Git e Github Ninja 

## Seção 1 Aula-1. Introdução  

* **Comandos**  

mkdir <nome do diretório> --> Criar diretório

touch --> criar arquivo.

git init --> Inicia o repositóiro do git  

git status --> Verifica o estado atual da árvore do git  (Mostra o controle de versão dos arquivos);
****  

## Seção 1 Aula-2. Adicionando arquivos e fazendo as configurações iniciais do git  

--> Passando do Working directory para o Staging Area --> git add  < file >

Staging Area --> Ainda não está no Diretório do Git

**CONFIGURAÇÕES PARA A REALIZAÇÃO DE COMMIT NO GIT --> PERMISSÕES PARA COMMIT**


--> git config --global user.name "nome de usuário"

--> git config --global user.email "nome@email.com"

--> config -l = Listar as configurações.

* Passando do Staging Area para a git Directory = git commit -m "Commit message"
****  

## Seção 1 Aula-3. Ver log de arquivos  
A partir daqui veremos a vizualização de pontos no histórico do Git.  

### Comando para vizualização:

--> git log = Apresenta um histórico dos commits e alterações realizadas.  

--> git diff = mostra as alterações realizadas nos arquivos, depois do git add, esse comando não apresenta as alterações realizadas.  
****  

## Seção 1 Aula-4.  Trabalhando com mais arquivos  
  
--> git add . = Adiciona todos os arquivos do working diretory para stage area de uma só vez.

--> git diff --staged = vizualiza as modificações da stage area.  
****  

## Seção 1 Aula-5. Voltando no tempo - Diff de commits  
  
--> git log --name-status = Mostra nomes dos arquivos modificados na staged area.

--> git diff <hash commit 1 hash commit 2> = Mostra a diferença entre dois commits pré determinados...
****  

## Seção 1 Aula-6. Remover arquivos

--> git rm arquivo = remove o arquivo da árvore do git.  
****  

# Seção 2  
  

## Seção 2 Aula-7. Adicionar arquivos

--> git add --all = adiciona arquivos da árvore do git de uma só vez.  

ou  

--> git add -A  
  
Faz sentido usar se quero mandar as alterações com um só commit.
****  

## Seção 2 Aula-8. gitignore  
  
.gitgnore --> Ignora arquivos a serem subidos.  
  
Trata-se de um arquivo oculto.  
  
--> .gitignore = **DEVE SER ADICIONADO A RAIZ DO PROJETO**
****  

## Seção 2 Aula-9. gitignore - parte 2  
  
git rm -rf node_modules/ --cached --> remove arquivos adicionados a staging area.   
****  

## Seção 2 Aula-10. gitignore - parte 3  
  
--> git commit -a -m ==> Ignora a staging area, passando as alterações diretamente para o git directory.  

**Cuidado** é perigoso, pois pode adicionar informações que não deveriam ser adicionadas  

**No Linux**  
git commit -am  

--> git config core.excludesfile ~/.gitignore ==> trabalha o .gitignore na raiz do projeto, ignorando um módulo específico em todos os projetos existentes na máquina.
****  

## Seção 2 Aula-11. commit sem parâmetros  

--> git commit ==> Encaminha para o nano ou VIM para edição do commit.  

--> git config --global core.editor < nome do editor > ==> Modifica o editor padrão do git.  

--> git config --global -e ==> muda as configurações globais manualmente, por exemplo editor ou user.
****  

## Seção 2 Aula-12. git log  
  
--> git log --pretty=oneline ==> Mostra cada log em apenas uma linha;  
  
--> git log --abbrev-commit ==> Abrevia o hash dos commits realizados;  
  
--> git log --stat ==> Mostra estáticas do log;  
  
--> git log -p ==> Mostra a alteração realizada nos arquivos;  
  

#### Posso unir dois comandos:  
  
--> git log --pretty=oneline --abbrev-commit  

****  
  
# Seção 3  
  

## Seção 3 Aula-13. git branch  
  
Não se faz alterações na **branch master** a branch master é criada por padrão no git. O correto é criar uma ramificação (branch) para o desenvolvimento do projeto.  
  
--> git branch < nome da branch > ==> cria uma nova branch;  
  
--> git checkout < nome da branch > ==> muda de branch;  

**Obs:** O git não faz commit de diretórios vazios.  
  
****  

## Seção 3 Aula-14. git branch - parte2  
  
--> git merge < nome da branch > ==> une branches!  
  
--> branch master ==> branch final de desenvolvimento;  

--> branch dev ==> onde serão realizadas as modificações. Será a versão beta do programa. Onde estará tudo o que foi e será desenvolvido.  

****  

## Seção 3 Aula-15. git branch - parte3  
  
--> git checkout -b < nome da branch > ==> cria uma nova branch e automáticamente seleciona a nova branch.  

--> git branch -m < novo nome da branch > ==> modifica o nome da branch;  

--> git branch -D < nome da branch > ==> apaga a branch  

No checkout -b = a branch terá o mesmo conteúdo da branch em que o comando foi executado  

--> git checkout --orphan < nome da branch> ==> cria uma branch vazia, sem relação com qualque outra  


****  

## Seção 3 Aula-16. Criando repositórios  
  
--> git init --bare ==> Cria um repositório  (ainda não será criado no Github)  
Será feito localmente o que o github faz na nuvem!  

--> git remote add < origin > < repository > ==> "linca" o diretório origem com o diretório remoto  

****  

## Seção 3 Aula-17. Sincronizando ambiente local com o repositório
  
--> git push < origin > < branch > == mandar para o origin o que está na nossa branch...  
****

## Seção 3 Aula-18. Clonando Repositórios
  
--> git clone < caminho > == Clonando repositório...  
****
  
# Seção 4  
  

## Seção 4 Aula-19. Como trabalhar em equipe - melhorar histórico de commits
  
--> Controle de versão centralizado == O repositório principal fica bloqueado sempre que alguém faz uma alteração no arquivo  
  
--> git commit -m < "Comentário" >  --amend == aproveita o commit anterior sobrescrevendo-o  
  
**OBS:** Utilizar o --amend após a realização de um push pode causar conflitos com outros commits já realizados pela equipe.
  
**OBS2:** Realizado o push --> **faça um novo commit**
  

****

## Seção 4 Aula-20. Automerge - Resolver conflitos  
  
--> git merge --abort == aborta o merge a ser realizado  
****  

## Seção 4 Aula-21. Merge Tool  

--> Ferramentas utilizadas para fazer Merge == meld  -> Utilizada no linux  
  
--> git config --global merge.tool meld
****  

## Seção 4 Aula-22. Alterações sem espaço e git checkout 

--> git diff -w == não mostra alterações de espaçamento no diff  
  
--> git checkout < file > == desfaz alterações **não commitadas**  
  
--> git checkout < num hash do commit > == volta em um commit para correções! Será necessário saber o número do commit  
  
--> git checkout -b < name of new branch > == Cria uma branch baseada na anterior.  
  
--> git checkout < name of branch based > -b < name of new branch > == Cria uma branch baseada na anterior, a partir de uma branch do repositório.  
  
--> git checkout < hash number for correction > -b < name of new branch > == Retorna no commit ao qual se quer corrigir e cria uma nova branch de correção  
  

****  

## Seção 4 Aula-23. git stash 

--> git stash == coloca as alterações de uma branch em uma "lista" para ser alterada depois!  
  
--> git stash list == mostra a lista de stashes salvas  
  
--> git stash apply == retorna a stash para o trabalho corrente  

--> git stash drop < nome do stash > == apaga a stash salva em memória  
  
--> stash@{0} == **SEMPRE** será o stash **MAIS RECENTE**

--> git stash apply == **SEMPRE** aplica o stash **MAIS RECENTE**, ou seja, **stash@{0}**  
  
--> git stash pop == Aplica o último stash e apaga o registro dele do stash list  
  
****  

## Seção 4 Aula-24 - Logs Personalizados  

--> git log -p -2 == Visualização do log com as duas últimas alterações realizadas nos arquivos  
  
--> o parâmetro numérico pode ser alterado conforme a necessidade do usuário. Exemplo:  
  
        git log -p -3  

--> git log --pretty=format:"%h - %an, %ar : %s"  
  
### Significado dos Parâmetro  

* %h = hash do commit abreviado  
* %an = Autor Name  
* %ar = Tempo em que foi realizado o commit  
* %s = Título do Commit  
  
### Outros Parâmetros  
  
* %H - Commit hash  
* %h - Commit Abreviado  
* %T - Tree Hash  
* %t - Abbreviated tree hash  
* %P - Parent hashes  
* %p - Abbreviated parent hashes  
* %s - Assunto do Commit  
* %an - Nome do autor  
* %ae - E-mail do autor  
* %ad - Autor date ou git log --date=option (exemplo date=short)  
* %ar - Autor date, relative  
* %cn - Committer name  
* %ce - Committer email  
* %cd - Committer date  
* %cr - Committer date, relative  

****  
  
# Seção 5  
  

## Seção 5 Aula-25 - Conhecendo o Github  
   
--> Aula de introdução e conhecimento sobre a plataforma Github

****  

## Seção 5 Aula-26 - Usando repositórios no GitHub
   
--> Utilização da url para subir no github (Alteração no origin):  

        git remote set-url origin https://github.com/henemesis/ecommerce.git  
       

****  

## Seção 5 Aula-27 - Conhecendo a página do repositório  
   
--> Na página do Github:  

+ Botão Watch == Fazer observações e receber atualizações do diretório ("assistir alterações")  

![config](/../master/ImgGit/img1.png?raw=true)  
  
+ Botão Star == Botão para marcar o repositório como "favorito", são separados em outro local  
  
![config](/../master/ImgGit/img2.png?raw=true)  
  
+ Botão Fork == Copia o repositório do Github para a minha conta Github, usado para colaboração entre projetos  
  
![config](/../master/ImgGit/img3.png?raw=true)  
  
  
+ Botão Change default Branch == Modifica a branch padrão.  
  
![config](/../master/ImgGit/img4.png?raw=true)  
  
****  

## Seção 5 Aula-28 - Conhecendo a página do repositório parte-2  
  
--> git commit -m "< commit > -fix #1" == Fecha a Issue aberta pelo por um usuário   

****  

## Seção 5 Aula-29 -  Trabalhando com branches no GitHub
     
--> Visualização de branches no site Github  
  
### Criando um pull request:  
  
* Pull request == solicitação de merge!  
  
****  


## Seção 5 Aula-30 -  Deletando branches no GitHub
     
--> git push origin < branch > --delete ou   

--> git push origin :< branch >
  
****  

# Seção 6  
  

## Seção 6 Aula-31 - Cache de Senha 
   
--> git config --global credential.helper cache == Evita o uso de senhas do git.  
  
Trata-se de uma configuração global!  Ao digitar a senha em uma operação ela será ficará em cache, sendo desnecessário digitar a senha novamente!  
  
--> git config --global --unset credential.helper == desfaz o comando acima. Dessa forma, volta-se a digitar senha e credencial.  

--> git config --global credential.helper 'cache --timeout=3600' == Comando para que a senha fique temporariamente no cache do git.
  

****  

## Seção 6 Aula-32 - Overview do repositório  
   
--> Overview de todos os links e tag do repositório no github.

****  

## Seção 6 Aula-33 - Configurações do repositório 
   
--> Configurações simples criadas no repositório do github na web para questões de segurança, modificação de branches entre outros.  

****  

## Seção 6 Aula-34 - Perfil do usuário e configurações
   
--> Overview do perfil do usuário e configurações do perfil do repositório no github 

****  

## Seção 6 Aula-35 - Configurações do usuário - parte 2
   
--> Overview do perfil do usuário e configurações do perfil do repositório no github 

****  

# Seção 7  
  

## Seção 7 Aula-38 - Markdown parte 2   
   
\_palavra\_  == coloca a palavra em itálico  (o underline deve ficar próximo a palavra)  
  
\[Link\](https:meusite.com.br) == Cria link no markdown  

****  

## Seção 7 Aula-39 - Markdown parte 3   
   
--> listas:  
  
usar travessão == -  
  
 Para sublistas, basta aumetar o espaço.  


****  

## Seção 7 Aula-40- Markdown parte 4  
  
### Tabelas  
  
* Como é escrita:  

![Tabela](/../master/ImgGit/img5.png?raw=true)  
  
* Visualização:  
  
Linguagem | Num de Usuários
----------|-----------------
Java      |   10K
Kotlin    |   8k
C         |   9k
Ruby      |   6k
  
#### Alinhando elementos da tabela:  
  
##### Alinhamento de valores a direita
* Codigo:  
  
![Tabela](/../master/ImgGit/img6.png?raw=true) 

* Visualização:(alinhamento dos valores a direita)  
  
Linguagem | Num de Usuários
----------|-----------------:
Java      |   10K
Kotlin    |   8k
C         |   9k
Ruby      |   6k
  
##### Alinhamento das palavras no centro
* Codigo:  
  
![Tabela](/../master/ImgGit/img7.png?raw=true) 

* Visualização:(alinhamento das palavras no centro)  
  
Linguagem   | Num de Usuários
:----------:|-----------------:
Java        |   10K
Kotlin      |   8k
C           |   9k
Ruby        |   6k
  
**** 

## Seção 7 Aula-41 - Markdown parte 5   
   
Review de tópicos de inserção de imagens entre outros. 

****

## Seção 7 Aula-42 - Upload - README - gists
   
Review de README e upload de arquivos e imagens.
Criação de gists --> pequenos trechos de código.

****

# Seção 8 
  

## Seção 8 Aula-43 - Trabalhando em equipe no GitHub  
   
Criando um forked no Github. --> Utilizando a estrutura do site do github.  
  

****  

## Seção 8 Aula-44 - Trabalhando em equipe no GitHub  parte 2
   
--> git fetch < nome do repositório > == busca atualizações do Github para a máquina local  
  

--> git merge upstream/master (upstream == repositório criado para exemplo) == compara os ambientes de trabalho para atualização  

--> git pull upstream/master (upstream == repositório criado para exemplo) == união de git merge e fetch em um só comando.  
  
--> git remote set-url < nome da url do git> --> Configura o remote através de uma url git  
  
--> git remote add upstream < nome da url do git>: upstream == nome padrão para o repositório principal  
  

****  

## Seção 8 Aula-45 - Trabalhando em equipe no GitHub  parte 3
   

****  


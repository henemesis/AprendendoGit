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
  

## Seção 3 Aula-12. git branch  
  
Não se faz alterações na **branch master** a branch master é criada por padrão no git. O correto é criar uma ramificação (branch) para o desenvolvimento do projeto.  
  
--> git branch < nome da branch > ==> cria uma nova branch;  
  
--> git checkout < nome da branch > ==> muda de branch;  

**Obs:** O git não faz commit de diretórios vazios.  
  
****  

## Seção 3 Aula-12. git branch - parte2  
  
--> git merge < nome da branch > ==> une branches!  
  
--> branch master ==> branch final de desenvolvimento;  

--> branch dev ==> onde serão realizadas as modificações. Será a versão beta do programa. Onde estará tudo o que foi e será desenvolvido.  

****  

## Seção 3 Aula-12. git branch - parte3  
  
--> git checkout -b < nome da branch > ==> cria uma nova branch e automáticamente seleciona a nova branch.  

--> git branch -m < novo nome da branch > ==> modifica o nome da branch;  

--> git branc -D < nome da branch > ==> apaga a branch  

No checkout -b = a branch terá o mesmo conteúdo da branch em que o comando foi executado  

--> git checkout --orphan < nome da branch> ==> cria uma branch vazia, sem relação com qualque outra  


****  

## Seção 3 Aula-12. Criando repositórios  
  
--> git init --bare ==> Cria um repositório  (ainda não será criado no Github)  
Será feito localmente o que o github faz na nuvem!  

--> git remote add < origin > < repository > ==> "linca" o diretório origem com o diretório remoto  

****  

## Seção 3 Aula-13. Sincronizando ambiente local com o repositório
  

****
# Git e Github Ninja 

## Seção 1 Aula-1. Introdução  

* **Comandos**  

mkdir <nome do diretório> --> Criar diretório

touch --> criar arquivo.

git init --> Inicia o repositóiro do git  

git status --> Verifica o estado atual da árvore do git  (Mostra o controle de versão dos arquivos);
****  

## Seção 1 Aula-2. Adicionando arquivos e fazendo as configurações iniciais do git  

--> Passando do Working directory para o Staging Area --> git add  <file>

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

## Seção 2 Aula-9. gitignore - parte 2.  
  
git rm -rf node_modules/ --cached --> remove arquivos adicionados a staging area.   
****  

## Seção 2 Aula-10. gitignore - parte 3.  
  
--> git commit -a -m ==> Ignora a staging area, passando as alterações diretamente para o git directory.  

**Cuidado** é perigoso, pois pode adicionar informações que não deveriam ser adicionadas  

**No Linux**  
git commit -am  

--> git config core.excludesfile ~/.gitignore ==> trabalha o .gitignore na raiz do projeto, ignorando um módulo específico em todos os projetos existentes na máquina.
****  

## Seção 2 Aula-11. commit sem parâmetros  

--> git commit ==> Encaminha para o nano ou VIM para edição do commit.  

--> git config --global core.editor <nome do editor> ==> Modifica o editor padrão do git.  

--> git config --global -e ==> muda as configurações globais manualmente, por exemplo editor ou user.
****  

## Seção 2 Aula-12. git log  
  
--> git log --pretty=oneline ==> Mostra cada log em apenas uma linha;  
  
--> git log --abbrev-commit ==> Abrevia o hash dos commits realizados;  
  
--> git log --stat ==> Mostra estáticas do log.  
  
  
#### Posso unir dois comandos:  
  
git log --pretty=oneline --abbrev-commit  

****
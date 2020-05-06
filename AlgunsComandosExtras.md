# Alguns Comandos Extras

## 1. Comando de fetch  

--> git fetch origin --prune --> Atualiza as listas de branch
****
  
## 2. Comandos de Stash  

--> git stash list --> Lugar da memória para não perder partes do trabalho.  

--> git stash save "<mensagem>" --> Salva o estágio de trabalho na stash com comentário!  

--> git stash apply stash@{1} -> Aplica a stash que estava em memória ao trabalho corrente!  
  
--> git stash drop stash@{0} -> Apaga... Perigoso!  

--> git stash pop -> tira da stash e aplica a stage.  

--> git stash show -p stash@{0} > patch.txt --> Salva a stash em um patch.txt caso seja necessário utilizar a stash em outra máquina (backup da stash)  
    
--> git apply patch.txt --> Aplica o patch salvo
****  

## 3. Comando de history  

### O Comando Abaixo será executado somente uma vez no terminal (GitBash ou Terminal Linux)
--> echo 'export HISTTIMEFORMAT="%d/%m/%y %T "' >> ~/.bash_profile  
--> source ~/.bash_profile

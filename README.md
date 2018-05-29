# Estudos_Git_e_Github
Estudando os comandos GIT, criando o chave(para comunicação entre o PC e o github remoto) e criando um repositório no github.



Conceitos, comando e praticas com GIT.

    Git é um sistema distribuído de repositório, 
    o que significa que estará todo o código em todas as máquinas.

    Após instalar o git, temos que configurar o git na máquina.
    Para configurar segue o passo a passo a baixo.

1 - git config --global user.name 'leonardo campos'
2 - git config --global user.email 'ljcjleonardo@gmail.com'
3 - git init (c:/projeto/angular) = criar um repositorio local no caminho específico
4 - clear = para limpar o console(tela).
5 - git status = verifica se tem algo para ser comitar ou confirmado.


PAREI na aula Curso de Git para iniciantes - Aula 2

1 - git add  . - adiciona todos os arquivos
    git add *.txt - adiciona todos os arquivos com a extensão .txt
    git add *.cs - adiciona todos os arquivos com a extensão .cs

2 - git commit -m 'mensagem'' => faz um comiti local(para o servidor utilizar o push)

2.1 - git commit -a -m 'comentário' - Esse comando faz o get add(-a) e depois o git commit mais a mensagem(-m)

2.2 - criar arquivo .gitignore e colocar os nomes dos pasta ou arquivos, imagens, e outras coisas que
      vc não quer que o git controle/versone/ingnorar.

7 - git diff -  ver tudo que foi modificado/alterado(antes do git add) nos arquivos.

8 - git diff --staged - ver tudo que foi modificado/alterado(depois do git add) nos arquivos.

9 - git log - mostra todos os commit do inicio ao fim

10 - gitk - Ferramenta visual para ver o relatório/log de alterações.

11 - git commit --amend - m 'mensagem' - comando para editar o ultimo commit.

12 - git log --pretty=oneline - comando par visualizar algumas linhas de log

13 - git reset HEAD nomeDoArquivo.extensão - comando para resetar/remover da stage area, 
     quando você fizer um commit de um arquivo que não podia comitar.

14 - git checkout -- nomeDoArquivo.extensao - Reverte(undo) o que foi feito no arquivo  

15 - git tag a- v0.0 -m 'Versão 1.0' (melhor usar as branch)
15.1 - git show => mostra as informações da tag criada
15.2 - git checkout v0.0 => pega a tag criada 
15.3 - git tag -d  v0.0 => deleta uma tag    

16 - git branch teste ou master
16.1 - git checkout teste ou git checkout -b teste (cria a branch e faz o checkout)
16.2 - por padrão o git cria uma branch MASTER.

17 - git marge teste(se vc estiver no master e vice e versa)
17.1 - o comando acima faz o seguinte: master faz um merge com o teste(o master será o código mais atualizado)
17.2 - git branch -d teste

Criando ambiente de DESENVOLVIMENTO / HOMOLOGAÇÃO / PRODUÇÃO
    Simulando uma ambiente de TRABALHO REAL do dia a dia de um programador na empresa.
    Assista essa aula para fazer o testes => https://www.youtube.com/watch?v=fRQrnWqDLn0&index=5&list=PLInBAd9OZCzzHBJjLFZzRl6DgUmOeG3H0

18 - git init --bare (no servidor) - git init é para criar um repositório local, apenas.
     Utilizando o GIT INIT --BARE no servidor, permite que o código seja acessivel para todo o time de desenvolvimento.
     Fazendo GIT INIT não será acessível para o time de desenvolvimento, pois é para criar um repositório local, quem está fora "não vê o código" ou não consegui fazer um push ou uma branch.
        
        O que é: Ao incializar um repositório como bare não será permitido editar arquivos (git add) e commitar mudanças (git commit), já que o mesmo não possui uma working tree. Você deve atualizar um repositório bare utilizando git push.

        Quando é usado: Você inicializa um repositório como bare quando deseja que ele seja o respositório central(no caso a master).

19 - git clone file:////nomeDoServidor/pastaDoCódgioFonte/ProjetoComCodigoFonte => obtém uma cópia do código fonte 

20 - git push (origin master) => envia o comite (local) para o servidor(remoto)
20.1 - git remote para  imptime na tela o nome do servidor, que no caso é origin, remote. 
       Por padrão o git cria o nome do servidor como origin.

21 - git pull (origin master) => Busca/pucha os arquivos/projeto do servidor para sua máquina.
    Caso ocorra conflito, ele faz um merge entre os arquivos locais e remotos(puchados).

22 - git fetch (origin master) => Faz o mesmo que o git pull, mas sua diferência é que ele não 
     faz merge automatico.

6 - git rebase



====================================================================

Trabalhando com o git hub

1 - primeiro faça um cadastro no git hub

2 - Abra o git bash(terminal de comandos git).
    Digite a chave ssh-keygen e aberte o entre
        Antes de terminar o processo, você pode digitar uma senha para a segurança da chave.
        Mas a cada push será solicitado a senha.

3 - Após isso acesse o github em settings => SSH keys => New SSH keys e copie e cole a chave gerada no campo. 
   A chave gerada vai estar geralmente no caminho C:\Users\ljcam\.ssh\id_rsa.pub

4 - Depois digite no git bash o comando git clone e o endereço do github repositorio remoto.
    Exemplo: $ git clone https://github.com/leleomaster/Estudos_Git_e_Github.git githubClone1(esse é o nome da pasta local)       


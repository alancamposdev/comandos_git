
<img src="https://seeklogo.com/images/G/git-logo-A1D01DDA30-seeklogo.com.png" alt="logo git" style="width:50px;"/>


Sumário
[TOC]


## O que é Git !?


É um sistema distribuído de controle de versão open-source, criado por Linus Torvalds.
Esse sistema registra alterações de um arquivo ou conjunto de arquivos ao longo do tempo, os __pontos na história__ através dos commits.


## Repositório Local 
Com o software instalado em sua máquina local, ele cria um repositório em sua máquina através de comandos.


---

###  Instalação


Para usar o git você precisa fazer a instalação em sua máquina.

Site oficial: <https://git-scm.com/downloads> 

Baixe conforme seu sistema operacional . "Windows,Mac,Linux"

Para confirmar se tem o git instalado no seu pc e qual a versão use o comando

`git --version`


---

### Opções para trabalhar com o git;

- Use o **terminal** para digitar os comandos git. 

- Use o **git bash** que é o terminal do git para digitar os principais comandos.

* Use um **editor de texto** de sua preferencia que tenha um terminal embutido.

* Use uma GUI - Graphical User Interface - escolha qual interface vc quer usar e instale.

---

### Configurações iniciais

Todos os comandos são iniciados com a instrução  _**git**_ seguido da instrução e complementos.

- Configurar seu nome:

  `git config --global user.name "SeuNome"`

* Configurar seu e-mail:

  `git config --global user.email "seu@email.com"`


* configurar seu editor principal:

  ` git config --global core.editor "" ` 

Usando --global você só precisa fazer uma vez que já estará configurado em todos os projetos.

* Ver a lista de suas configurações.

  `git config --list`

  

  Para mostrar uma lista de *comandos mais usados* pelo git.

  `git --help` ou `git --help --all` mostra todos os comandos.

---


### Estágios do git


São três:
| Diretório de trabalho  | área de preparo/espera | repositório |



1. Working directory (untracked)- **diretório de trabalho**, arquivos ainda não estão sendo monitorados
2. Stagind area (staged) - área temporária, onde você determina quais mudanças serão adicionadas ao seu repositório.  
3. Committed - área com os arquivos commitados, salvos no repositório local.

Para saber em qual status está seu arquivo.

Use o comando: `git status`

<img src="https://res.cloudinary.com/practicaldev/image/fetch/s--D7nJOADN--/c_imagga_scale,f_auto,fl_progressive,h_900,q_auto,w_1600/https://cl.ly/569e7f0bbfaf/download/Image%25202018-08-29%2520at%25208.26.35%2520PM.png" style="zoom:25%;" />

---


### Iniciar um novo repositório local

Comando para iniciar o repositório, onde cria uma pasta **.git** *oculta* com o repositório local.

Vá até diretório que você quer criar o repositório. E digite o comando:

`git init`



> Estagio 1. Diretório de trabalho - Working directory (untracked)

os arquivos ainda não estão sendo rastreados e se encontra no "Working Directory".

---

#### Adicionando arquivo na Stage Area

Usado para adicionar arquivos para a

`git add`

```git
git add nomeDir           // um arquivo espécifico
git add arq.txt
git add arq1 arq2 arq3  //adicionando multiplos arquivos
 
git add .           // todos os arquivos que estão no diretório de trabalho
git add -A         //se comporta da mesma forma que o comando anterior
```



> Estágio 2. Área de espera - Stagind area (staged)

Esse comando é usado para adicionar os arquivos não-rastreados para a staging area . Os arquivos passam a ser rastreados passando para a "staging area"





#### Alterações feitas

Gostaria de ver as alterações feitas antes de comitar!?

Use o comando `git diff` 

mostrando as linhas que foram adicionadas ou removidas (compara com o que está no estágio-1 com o estágio-2)

`git diff --staged` compara as alterações que estão no estágio-2 com o seu ultimo commit. 



---



`git commit`

```git
git commit -m "mensagem do commit" //use uma mensagem significativa

git commit -a -m "adicinando e comitando" //atalho para add e comitar 
```

 O atalho* só funciona  se tiver feito pelo menos um git add antes.



> Estagio 3. Área com os arquivos adicionados no repositório local - *repository*



#### Histórico de commits

Comando para ver a lista de commits.

`git log `

```git
git log                       //lista todos os commits feitos
git log -p                   //log com diff -lista de commits e alterações
git log --graph
git log --pretty=oneline    //mostra o codigo e a msg do commit
git log --oneline  	     	//mostra o codigo de forma reduzida

```



O git oferece a sua própria interface gráfica para mostrar as alterações feitas nos *commits*, para facilitar o entendimento.

`gitk`


> 
> | Comandos básicos | **Resumo com mudanças locais:**                             |
> | :--------------- | ----------------------------------------------------------- |
> | git init         | inicia um repositório local e cria um *working directory* . |
> | git add .        | adiciona todas as mudanças atuais no *stage area.*          |
> | git commit       | confirma alterações preparadas e salva no *repository*.     |
> | git status       | arquivos alterados em seu repositório de trabalho           |
> | git diff         | mudanças em arquivos rastreados                             |
> | git log          | lista com o histórico de  *commits* no repositório local    |

---

### Ignorar arquivos

Criar um arquivo com a extensão `.gitignore`

Os arquivos ou repositório que estiverem declarados dentro desse arquivo serão ignorados.

```git
*.pdf            //ignorar todos os arquivos com extensão pdf
pastaX/       	 //ignora uma pasta específica
```



---


###  Desfazendo as alterações feitas

Adicionou ou commitou e se arrependeu!? Não se desespere !!

`git reset HEAD arquivo`  - remove da *stage area*

`git commit --amend -m ""` - editar o ultimo commit (substituindo-o)

`git checkout --NOMEARQUIVO` reverte ao ultimo commit    *perde as alterações feitas no ultimo commit.



___

### Apelidos no Git 

São usados para tornar os comandos git mais simples e fácil, adicionando apelidos(alias).

Para isso temos que configurar esses "alias" nas configurações.

```git
git config --global alias.st status
git config --global alias.lg log
git config --global alias.cm commit
```



Nesse comando eu adicionei apelidos ao comando git status e git log. Substituindo o comando pelo apelido.

Agora basta digitar `git st` e `git lg`  e `git cm` para que os comandos serão executados



___

## Repositório Remoto

- Crie um repositório remoto no GITHUB. Site do github: <https://github.com/>
- Faça a ligação entre  o repositório local com o remoto.


### Sincronizar repositório local/remoto

Uma das formas é usando gitbash: (é o  terminal que vem no git), crie as chaves de segurança (privada e publica) no seu pc.
  Digite o comando.

  `ssh-keygen -t ed25519-sk -C "seu_email@example.com" `

  Digite uma senha,confirme e uma adicione uma palavra chave - todas opcionais. <br>
  Será criada uma pasta com as duas chaves em seu computador.

 Após criados as chaves. Vá no github é adicione a chave pública.

Como saber se estamos conectamos a um repositorio remoto!?<br>
Através do comando <br>
`git remoto`     <-- retorna o nome do repositorio remoto se houver <br>
`git remote -v`  <-- retorna o nome com a URL - HTTPS do repositório remoto

Se ficar em branco é porque não esta conectado com nenhum.

Adicioando um repositório remoto.

`git remoto add origin git@github.com:USERNAME/REPOSITORY-NAME.git`  <--passando o SSH>

`git remoto add origin https://github.com/USERNAME/REPOSITORY-NAME.git`  <--passando o HTTPS

 <br>

__Origin__ é o alias (apelido) da URL do seu repositório remoto.<br>
Você pode *Renomear* o origin.
`git remote rename origin novonome` 


> Pronto agora está na hora de fazer o push ou pull do repositório remoto.

 `git push -u origin master`


<br>


### Push e Pull ##

**Push** empurrando seus commits para  o repositório remoto.

`git push`

**Pull** atualizando com seu repositório local, com o repositório remoto.

`git pull`

**Fetch** equivale ao git pull, só que não faz o merge (a mesclagem) das versões do projeto

`git fetch`

```git
    git push origin master
    git pull origin master
```

Origin - é o nome do remote;

Para saber qual o nome remoto:
`git remote -v`

Master - é o branch; se tiver usando outro ponteiro(ramificação), troque pelo ponteiro desejado.



---
<br>

### Clonar repositório do GITHUB ##

Copie o link do repositorio do github que deseja clonar. Escolha o local que deseja salvar os arquivos.
Dentro do local desejado digite esse comando pelo terminal  ou pelo terminal do git( gitbash)<br>
ou com o editor de texto que tenha o terminal integrado.

`git clone https://github.com/.....` 



### Colaboração no GitHub



Fazer um fork do repositório que gostaria de colaborar

1. clicar em fork (vai criar um repositório do projeto no seu GitHub)

2. clonar o repositório na sua máquina "git clone"

3. trabalhar no projeto
4. salve suas alterações
5. envie suas alterações "git push"
6. concluiu a colaboração !? Envie para o autor do projeto."pull request"
7. envie "Send pull request" e só aguardar a aprovação do autor ou não das alterações feitas 
8.  O autor pode mesclar com o projeto original ou não. 
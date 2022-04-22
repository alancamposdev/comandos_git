# Comandos git    <img src="https://seeklogo.com/images/G/git-logo-A1D01DDA30-seeklogo.com.png" alt="logo git" style="zoom:8%;" />



### Comandos de configurações iniciais
| comandos globais| função | 
| ---| --- |
| git config --global user.name "seuNome"| configura um nome de usuário|
| git config --global user.email "seuEmail"|configura um email de usuário|
| git config --global core.editor "code --wait" | o editor de texto padrão do git é o VIM, caso queira mudar pro VSCode| 
| git config --list | lista as configurações feitas|
|| |
|🔸 **Comandos importantes** | |
| git --help       | lista os principais comandos do git |
| git --help --all | lista todos os comandos git   |
| git --version    | mostra a versão do git instalado|


<br><br>

### Os três estagios do git

<img src="https://res.cloudinary.com/practicaldev/image/fetch/s--D7nJOADN--/c_imagga_scale,f_auto,fl_progressive,h_900,q_auto,w_1600/https://cl.ly/569e7f0bbfaf/download/Image%25202018-08-29%2520at%25208.26.35%2520PM.png" style="zoom:25%;" />

| Diretório de trabalho  | área de preparo/espera | repositório |

<br><br>

### Comandos básicos
|comandos |  mudanças locais  |status| área
| --- | --- | --- | --|
| git init   | inicializa um repositório local|não rastreado | diretório de trabalho |
| git diff   | mostra as alterações feitas antes de adicionar|não rastreado| diretório de trabalho |
| git add    | adiciona os arquivos na "stagind area"                          |rastreado     | area de espera|
| git diff --staged| compara as alterações na stage com o ultimo commit|rastreado|area de espera|
| git commit | salva as alterações no repositório  |             | repositório local |
| git log    | mostra o histórico de "commits"| |
| gitk       | mostra uma interface gráfica com o histórico dos commits|
| git status | mostra o status das alterações |como não rastreado, modificadas ou testadas||




<br><br>

###  Desfazendo as alterações feitas

Adicionou ou commitou e se arrependeu!? Não se desespere !!

`git reset HEAD arquivo`  - remove da *stage area*

`git commit --amend -m ""` - editar o ultimo commit (substituindo-o)

`git checkout --NOMEARQUIVO` reverte ao ultimo commit    *perde as alterações feitas no ultimo commit.

<br><br>

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


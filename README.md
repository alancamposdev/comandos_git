# Comandos git



### Comandos de configurações iniciais
| comandos globais| função | 
| ---| --- |
| git config --global user.name "seuNome"| configura um nome de usuário|
| git config --global user.email "seuEmail"|configura um email de usuário|
| git config --global core.editor "code" | o editor de texto padrão do git é o VIM, caso queira mudar pro VSCode| 
| git config --list | lista as configurações feitas|

### Comandos básicos
|🎯comandos |  mudanças locais  |status| área
| --- | --- | --- | --|
| git init   | inicializa um repositório local|não rastreado | diretório de trabalho |
| git diff   | mostra as alterações feitas antes de adicionar|não rastreado| diretório de trabalho |
| git add    | adiciona os arquivos na "stagind area"                          |rastreado     | area de espera|
| git diff --staged| compara as alterações na stage com o ultimo commit|rastreado|area de espera|
| git commit | salva as alterações no repositório  |             | repositório local |
| git log    | mostra o histórico de "commits"| |
| gitk       | mostra uma interface gráfica com o histórico dos commits|
| git status | mostra o status das alterações |como não rastreado, modificadas ou testadas||


### Comandos 


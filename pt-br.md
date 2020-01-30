# Comandos Linux

    Uma lista de comandos do terminal Linux que é comumente usada.

## Navegação

|Comando|Descrição|
|------|------|
|```pwd```|Onde estou?|
|```ls```|Exibe arquivos e diretórios.|
|```ls -l```|Exibe arquivos e diretórios de uma forma extendida.|
|```ls -lh```|Exibe arquivos e diretórios de uma forma extendida com unidade de medida.|
|```ls -a```|Exibe arquivos e diretórios inclusive os ocultos.|
|```ls -la```|Exibe arquivos e diretórios inclusive os ocultos de uma forma extendida.|
|```cd <diretório>```|Vai para o diretório de destino.|
|```cd <diretório>/<sub-diretório>```|Vai ara o sub-diretório de destino.|
|```cd ..```|Retorna para o diretório anterior.|
|```cd ../../```|Retorna para o diretório anterior.|
|```cd /```|Vai para o diretório raiz.|
|```cd ~```|Vai para o diretório home.|
|```clear```|Limpa a tela do terminal.|
|```Ctrl + l```|Limpa a tela do terminal.|

## Manipulação de arquivos e diretórios

|Comando|Descrição|
|------|------|
|```mkdir <nome>```|Cria diretório.|
|```mkdir -p <a>/<ab>/<abc>```|Cria diretório aninhado.|
|```touch <arquivo>```|Cria arquivo.|
|```mv <arquivo> <destino>```|Move arquivo para diretório de destino.|
|```mv <origem>/<arquivo> .```|Move arquivo da origem para para o diretório atual.|
|```mv <diretório> <novo nome>```|Renomeia o diretório.|
|```mv <arquivo> <novo nome>```|Renomeia o arquivo.|
|```cp <arquivo> <nova cópia>```|Copia arquivo para novo arquivo.|
|```cp -r <diretório> <novo diretório>```|Copia diretório para novo diretório de forma recursiva.|
|```rm <arquivo>```|Remove arquivo.|
|```rm -r <diretório>```|Remove diretório de forma recursiva.|
|```cat <arquivo>```|Exibe o conteúdo do arquivo.|
|```more <arquivo>```|Exibe o conteúdo do arquivo. Carrega todo o arquivo em memória de uma vez.|
|```less <arquivo>```|Exibe o conteúdo do arquivo. Carrega o arquivo usando streams, isso significa que o comando carrega somente a parte necessária do arquivo.(Suporta os comandos do vim)|
|```chown <usuário> <arquivo>```|Altera o usuário que é dono do arquivo.|
|```chown :<grupo> <arquivo>```|Altera o grupo de usuários que são donos do arquivo. Este comando pode ser usado junto com o comando anterior.|

## Histórico

|Comando|Descrição|
|------|------|
|```history```|Exibe o histórico de comandos.|
|```Ctrl + r```|Inicia a busca interatica no histórico ou encontra a próxima ocorrência quando a busca interativa já foi iniciada.|
|```!n```|Executa o comando número 'n'.|
|```!!```|Repete o comando anterior.|
|```!<string>```|Repete o comando anterior que inicia com 'string'.|
|```dirs -p```|Exibe o histórico de diretórios visitados.|

## Permissions

|comando|Description|
|------|------|
|```chmod xxx <arquivo or diretório>```|chmod changes the permissions of usuário, group or everyone to read, write or run the arquivo.|
|```chmod -R xxx <diretório>```|Changes the permissions of all arquivos and directories that are in the diretório recursively.|

This comando uses a string that represents the permissions.

![ inserir explicação aqui ][permissions]

* __( r )__ read permitted.

* __( w )__ write permitted.

* __( x )__ execution permitted.

### Exemples

|||
|------|------|
|```chmod 111 <arquivo>```|Everyone could execute the arquivo.|
|```chmod 222 <arquivo>```|Everyone could write to the arquivo.|
|```chmod 700 <arquivo>```|Only the owner has all the permissions.|
|```chmod 600 <arquivo>```|The owner could read and write the arquivo.|

## Varieties

|Comando|Description|
|------|------|
|```diff -qr <diretório1> <diretório2>```|Shows the differences between the directories. Argument ```-q``` shows modified or nonexistent arquivos. Argument ```-r``` shows the differences between arquivos content.|
|```man <comando>```|Page of Manual of comandos.|
|```whoami```|Who am i? Shows you usuárionome.|

## Packet manager (apt-get)

|Comando|Description|
|------|------|
|```sudo apt-get install <pacote>```|Installs a pacote.|
|```sudo apt-get install -f```|Finds and fixes broken pacotes.|
|```sudo apt-get remove <pacote>```|Removes a pacote. Leaves usuário configuration arquivos.|
|```sudo apt-get purge <pacote>```|Removes a pacote completely.|
|```sudo apt-get update```|Verifies if exists pacotes repository updates.|
|```sudo apt-get upgrade```|Verifies if exists system updates.|
|```sudo apt-get autoremove```|Removes all obsolete and unnecessary pacotes.|
|```sudo apt-get autoclean```|Cleans the packet manager cache.|
|```apt-cache search <pesquisa>```|Finds pacotes in repository.|
|```apt-cache show <nome_do_pacote>```|Shows a description about the pacote.|

[permissions]: https://github.com/hemilioaraujo/Linux-comandos/blob/master/img/permissionsEN.PNG?raw=true
"String representation"
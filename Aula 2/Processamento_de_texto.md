# Processamento de Texto

## Comandos básicos

- ### nano ou pico
>- Ctrl + W -> Procura;
>- Ctrl + K -> Corta;
>- Ctrl + U -> Cola;

- ### vim
>- **Dois modos de operações**:
>>- Modo de comando -> ESC;
>>- `:w!`  -> Salva;
>>- `:q!`  -> Sai;
>>- `:wq!` -> Salva e sai;
>>- `/procura` -> Procura a palavra `procura`;
>>- `/(procura|varias|palavras)` -> Procura a ocorrência das três palavras ao mesmo tempo;
>- Modo de inserção -> i;
>>- Escreve normal;

- ### sed
>- Não interativo;
>- Funciona em comandos;
>- `sed "s/Tacos/Nachos/" arquivo.txt`;
>>- Lê o arquivo trocando Tacos por Nachos para primeira ocorrência;
>- `sed "s/Tacos/Nachos/g/" arquivo.txt`;
>>- Lê o arquivo trocando Tacos por Nachos para todos ocorrências;
>>- **Obs**: Não salva o arquivo;
>>- `sed -i".bkp" "s/Não/Sim/" Anotacoes.md` -> Salva o arquivo trocando Não por Sim e o que estava antes salva em um arquivo com extensão .bkp;

- ### cut
>- `cut -f1 -d" "`
>>- **Obs**: Delimitador é  o espaço;
>>- Filtra por espaço os arquivos;
>- **Exemplo**: `ls -l Anotacoes.md  | cut -f1 -d " "`
>- Saída do ls -l Anotacoes.md:
>>- `-rw-rw-r-- 1 bezard bezard 919 Ago 16 11:38 Anotacoes.md`
>- Saída do cut:
>>- `-rw-rw-r--`

- ### awk
>- `ls -l Anotacoes.md | awk -F" " '{print $1}'`
>- Saida:
>>- `-rw-rw-r--`;
>- **Obs**: 
>>- Delimitador é o espaço;
>>- O $1 coloca para printar apenas o primeiro campo;
>>- Sem o `-F` o delimitador padrão é espaço e tab;
>- `ls | awk '{print "mv "$1" "$1".txt"}' | sh`
>>- Renomeia todos os arquivos da pasta para .txt;

- ### strings
>- `strings unknown.mp3`
>>- Imprime apenas caracteres que conseguimosler;

- ### cat
>- `cat arquivo1 arquivo2` 
>- Concatenar dois arquivos na tela;

- ### tac
>- `tac arquivo1 arquivo2`
>- Imprime de baixo para cima;
>- Útil para ler logs;

- ### wc
>- Word Count;
>- Imprime número de linhas, palavras e caracteres;
>- `wc /etc/pnm2ppa.conf`
>- Saída = 187 1233 7649 /etc/pnm2ppa.conf
>- Flags
>>- l -> linhas;
>>- c -> caracteres;
>>- w -> palavras;

- ### head
>- `head -n 2 Arquivo.txt`
>>- Mostra as duas primeiras linhas do Arquivo.txt;

- ### tail
>- `tail -n 2 Arquivo.txt`
>>- Mostra as duas últimas linhas do Arquivo.txt;
>- `tail -f Arquivo.txt`
>>- Se aparecer mais linhas atualiza;

- ### tee
>- `ls -l /etc/ | tee arquivo.txt`
>>- Escreve na tela e também salva no arquivo;

- ### grep
>- `grep -i failed /var/log/syslog`
>- Flags:
>>- `-v` -> Procura linhas que não tem a palavra
>>- `-c` -> Conta as linhas;
>>- `-i` -> Ignora diferença de letras maiúsculas

- ### sort
>- `sort Arquivo.txt`
>- Printa o arquivo de maneira ordenada;
>- Flags:
>>- `-n` -> ordenação númerica
>>- `-r` -> ordenação reversa;

- ### uniq
>- printa uma única vez o que estiver em sequência
>>- Arquivo.txt: oi\n oi\n oi\n;
>>- `uniq Arquivo.txt` -> oi;

- ### zcat
>- Lê arquivo compactado;

- ### diff
>- Mostra diferença entre dois arquivos;


  # Introdução

- Terminal (Shell) é um programa que interpreta comandos;
>- Entradas e saída em formato texto;
- Existem mais de um tipo de Shell;
>- É possível criar um programa que atue como Shell;
>>- São padronizados;
>>- bash (GNU);
>>- dash (Debian);
>>- pdksh

## Modo interativo

```bash
- echo "oi
> mundo"
- for((j=0; j<12; j++)) do
> echo $j
> done;
0
1
2
3
4
5
6
7
8
9
10
11
```
## Modo não interativo

- Inicia documento com #!/bin/bash
>- Define o  interpretador do conteúdo do arquivo;
>- Executa ./nome do arquivo;
>>- **OBS:** Pode usar qualquer interpretador #!/bin/python por exemplo

## Observações

- $PATH -> Contém as pastas e diretórios que você tem os programas para executar;
- --help -> comando para comandos utilitátios;
>- Esse comando é útil quando se sabe o comando;
>- `$ cat --help;`
>- **OBS:** `$cat -n arquivo` -> Mostra número da linha;
- `man arquivo`-> para acessar o manual da instrução;
>- Esse comando é útil quando se sabe o comando;
- `python --help | less ou more`
>- '|' é um paginador, executa a opção pedida '--help' junto com outro programa;
- `grep "#" arquivo` -> Procura linhas que tem #;
>- `grep -v "#" arquivo` -> Procura todas as linhas uqe não tem #;


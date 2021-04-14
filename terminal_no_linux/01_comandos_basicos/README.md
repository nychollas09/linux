# Kickstart

## Comandos Básicos

```bash
# Exibe o diretório atual de onde o comando está sendo executado

pwd
```

```bash
# Exibe um manual do comando informado

man COMAND

# EX:

man ls
```

```bash
# Troca para o diretório informado

cd PATH
```

```bash
# Para conteúdos muito grandes, ele possibilida uma visualização mais compassada.

more FILE_NAME ou FILE_CONTENT

# Ex:

more dpkg.log
```

```bash
# Localiza no conteúdo informado a palavra/RegEx informada

grep PALAVRA FILE_NAME ou FILE_CONTENT

# EX:

grep status dpkg.log
```

```bash
# Exibe todas as partições existente

# "-h" = Exibe de uma maneira mais amigável

df -h
```

```bash
# Exibe o tamanho de cada arquivo/pasta no diretório executado

# "-h" = Exibe de uma maneira mais amigável

du -h
```

```bash
# Exibe a quantidade de mémoria que está disponível e ocupada na máquina

free
```

```bash
# Cria um diretório no caminho informado

# "-p" = Possibilita a criação recursa(aninhada) desses diretórios

mkdir -p DIR_PATH

# Ex:

mkdir pasta1

mkdir -p pasta1/pasta2/pasta3
```

```bash
# Renomeia o arquivo/pasta informado

mv TARGET_A_SER_RENOMEADO NOVO_NOME

# Ex:

mv dpkg.log my-dpkg.log
```

```bash
# Remove o arquivo informado

rm FILE

# Ex:

rm dpkg.log

# Remove o diretório informado

rm -rf DIR

# Ex:

rm -rf temp
```

## Cat

Pode pegar exibir o conteúdo do arquivo informado, além de pode subrescrever ou concatenar o conteúdo do arquivo informado para outro arquivo.

```bash
cat FILE_NAME

# Ou

cat FILE_NAME > PATH_DO_SEGUNDO_ARQUIVO

# Ex:

cat dpkg.log > ~/bkp-dpkg.log
```

## Pipe "|"

Envia a saída de um comando para a entrada do próximo comando, assim, dando continuidade no processamento.

```bash
cat dpkg.log | more
```

# Permissões

Permissões que os usuários tem dentro de um escopo.
Seja dentro de uma pasta específica ou dentro de todo SO

| Número da permissão (Octal) | Valor da permissão (Binário) | Read "R"           | Write "W"          | Execute "X"        |
| --------------------------- | ---------------------------- | ------------------ | ------------------ | ------------------ |
| 0                           | 000                          | :x:                | :x:                | :x:                |
| 1                           | 001                          | :x:                | :x:                | :heavy_check_mark: |
| 2                           | 010                          | :x:                | :heavy_check_mark: | :x:                |
| 3                           | 011                          | :x:                | :heavy_check_mark: | :heavy_check_mark: |
| 4                           | 100                          | :heavy_check_mark: | :x:                | :x:                |
| 5                           | 101                          | :heavy_check_mark: | :x:                | :heavy_check_mark: |
| 6                           | 110                          | :heavy_check_mark: | :heavy_check_mark: | :x:                |
| 7                           | 111                          | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |

<br>

# Nomenclatura das permissões

<img src="https://raw.githubusercontent.com/nychollas09/linux/main/terminal_no_linux/.assets/permissoes.png">

Tomando como exemplo: "drwxr-xr-x"

<p>
    O <strong>Primeiro</strong> caractere classifica o resultado em três tipos:

    "-" = Arquivo
    "d" = Diretório
    "l" = Link simbólico (atalho)

</p>

<br>

<p>
    Do <strong>Segundo</strong> ao <strong>Terceiro</strong> caractere é referente a permissão do <strong>usuário</strong>.
</p>

<br>

<p>
    Do <strong>Quarto</strong> ao <strong>Sexto</strong> caractere é referente a permissão do <strong>grupo</strong>.
</p>

<br>

<p>
    Do <strong>Sétimo</strong> ao <strong>Nono</strong> caractere é referente a permissão do <strong>dono do arquivo</strong>.
</p>

# Mudando permissão de arquivo/diretório

```bash
chmod NÚMERO_PERMISSÃO_GRUPO NÚMERO_PERMISSÃO_USUÁRIO NÚMERO_PERMISSÃO_DONO ARQUIVO/DIRETÓRIO

# Ex:

chmod 660 adduser.conf

# Ou

# "u" = Usuário
# "g" = Grupo
# "o" = Outros/Autor

# Permite que os membros do grupo façam o Read e Write no arquivo/diretório (adiciona as permissões já existentes)

chmod g+rw adduser.conf

# Permite que os membros do grupo façam o Read e Write no arquivo/diretório (Sobrescreve as permissões já existentes e deixa somente as informadas)

chmod g=rw adduser.conf
```

# Grupos

## Comandos básicos

```bash
# Cria um usuário com diretório home

# PS: Quando cria-se um usuáro, por padrão ele também ja cria um grupo com o mesmo nome

adduser nichollas

# Ou

# Cria o usuário sem diretório home

useradd nichollas
```

```bash
# Troca de usuário

su - USUARIO

# Ex:

su - nichollas
```

```bash
# Troca senha do usuário atual

passwd
```

```bash
# Remove o usuário
# "--remove-home" = Remove a pasta home do usuário

deluser nichollas
```

```bash
# Cria um grupo

groupadd school_of_net
```

```bash
# Adiciona/Cria um usuário e adiciona ao grupo existente

adduser USUARIO GRUPO

# Ex:

adduser nichollas school_of_net
```

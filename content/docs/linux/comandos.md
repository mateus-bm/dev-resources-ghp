---
title: "Comandos"
description: "Comandos básicos no linux"
weight: 2
icon: "article"
draft: false
toc: true
---
---

## Navegação

Para navegar até um diretório, podemos utilizad o `cd`:

```sh
cd /caminho/do/diretorio
```

Exemplo, para navegar até a `home` do usuario atual podemos utilizar o seguinte comando:

``` sh
cd ~
```

Para visualizar o caminho do diretório atual, podemos utilizar o comando `pwd`:

``` sh
pwd
```

Por fim, para visualizar o conteudo do diretório atual podemos utilizar o comando `ls`:

``` sh
ls
```

O comando `ls` possui `flags` que podem facilitar a visualização de informação, exemplo:

```sh
ls -lah
```

Neste caso usamos 3 `flags`:

- **l**: A flag `l` faz com que os diretórios sejam listados como links e traz dados detalhados dos arquivos listados.

- **a**: A flag `a` faz com que os arquivos ocultos sejam listados.

- **h**: Por fim, a flag `h` faz com que os valores exibidos sejam de facil leitura.
  - Exemplo: um arquivo que tem tamanho "5506048" (Bytes) quando listado com `ls -l`, vai passar a exibir o tamanho "5.3M" (Mega Bytes) com `ls -lh`.

---

## Pacotes

### Informações gerais

Enquanto no ecosistema unix, comumente vamos referir a ferramentas ou serviços como `pacotes`.

Cada distribução linux pode utilizar diferentes gerenciadores de pacotes.

Sistemas baseados em debian costumam utilizar pacotes `.deb` e usam gerenciadores como `apt`.

Sistemas baseados em rhel costumam utilizar pacotes `.rpm` e usam gerenciadores como `yum` e `dnf`.

### Listando pacotes

Para listar os pacotes instalados, execute:

```sh
apt list --installed
```

Como a lista de pacotes pode ser bem extensa, utilize de utilitários como `grep` para filtrar a resposta, exemplo:

```sh
apt list --installed | grep nome_do_pacote
```

O comando acima deve retornar todos os pacotes que possuem o texto `nome_do_pacote`.

### Atualizando pacotes com APT

{{< alert context="info" text="A execução de alguns comandos necessita de permissão de administrador, a gestão de pacotes provavelmente deverá ser feita incluindo `sudo` antes do comando" />}}

Para atualizar a lista de pacotes disponiveis, utilize:

```sh
apt update
```

Para atualizar todos os pacotes exibidos em `apt update`, execute:

```sh
apt upgrade
```

Para atualizar um pacote especifico, execute:

```sh
apt upgrade nome_do_pacote
```

### Removendo pacotes

Para remover um pacote, execute:

```sh
apt remove nome_do_pacote
```

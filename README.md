# dev-resources-ghp

Projeto para armazenar e centralizar recursos para consulta e fixação de conhecimentos.

## Ferramentas utilizadas

- [Go 1.25](https://go.dev/)
- [Hugo](https://gohugo.io/)
  - [Lotus Docs](https://lotusdocs.dev/)

## Executando o projeto

Instale os componentes do [Go](https://go.dev/doc/install) e [Hugo](https://gohugo.io/installation/)

Execute no terminal:

```sh
hugo server -D
```

## Criando novas paginas

Todas as paginas de documentação devem estar em `./content/docs`.

Caso seja conteudo de um novo tópico, este deverá ser isolado em uma nova pasta, após criar a pasta crie seu indice com o comando abaixo:

```sh
hugo new docs/caminho/do/topico/_index.md
```

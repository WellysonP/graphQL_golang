# Meu Projeto GraphQL

Este é um projeto GraphQL desenvolvido em Go, que fornece uma API para gerenciar categorias e cursos.

## Descrição
Este projeto permite a criação, leitura e gerenciamento de categorias e cursos utilizando GraphQL. Ele utiliza o `gqlgen` para gerar o código GraphQL e `sqlite3` como banco de dados.

## Instalação
1. Clone o repositório:
   ```bash
   git clone https://github.com/WellysonP/graphQL_golang.git
   cd graphQL
   ```
2. Instale as dependências:
   ```bash
   go mod tidy
   ```
3. Instale o `sqlite3` se ainda não estiver instalado:
   ```bash
   sudo apt install sqlite3
   ```
4. Crie o banco de dados e as tabelas:
   ```bash
   sqlite3 data.bd
   create table courses (id string, name string, description string, category_id string);
   create table categories (id string, name string, description string);
   .exit
   ```

## Uso
Para rodar o servidor, execute:
```bash
go run ./src/server.go
```

Acesse a API GraphQL em `http://localhost:8080`.

## Estrutura do Código
- `src/database/`: Contém a lógica de acesso ao banco de dados.
- `graph/model/`: Define os modelos de dados utilizados na API.
- `graph/schema.resolvers.go`: Contém os resolvers para as operações GraphQL.
- `gqlgen.yml`: Configuração do gqlgen.
- `README.md`: Este arquivo.

## Contribuição
Contribuições são bem-vindas! Sinta-se à vontade para abrir um pull request.

## Licença
Este projeto está licenciado sob a MIT License.

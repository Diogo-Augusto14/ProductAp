# Product API - ASP.NET Core

API REST desenvolvida em **C# com ASP.NET Core** para gerenciamento de produtos.

Este projeto foi criado para demonstrar conhecimentos em **desenvolvimento backend, arquitetura em camadas e integração com banco de dados utilizando Entity Framework Core**.

---

# Tecnologias Utilizadas

* C#
* ASP.NET Core Web API
* Entity Framework Core
* SQLite
* Swagger

---

# Funcionalidades

A API permite realizar operações CRUD de produtos:

* Criar produto
* Listar produtos
* Buscar produto por ID
* Atualizar produto
* Deletar produto

---

# Arquitetura do Projeto

O projeto foi organizado em camadas seguindo boas práticas de desenvolvimento backend.

```
ProductApi
│
├── Controllers
├── Data
├── Models
├── Repositories
├── Services
└── Program.cs
```

### Controllers

Responsáveis por receber as requisições HTTP da API.

### Services

Camada responsável pela lógica de negócio da aplicação.

### Repositories

Camada responsável pela comunicação com o banco de dados.

### Data

Configuração do banco de dados e DbContext.

### Models

Definição das entidades da aplicação.

---

# Modelo de Produto

A entidade principal da API é o produto.

```csharp
public class Product
{
    public int Id { get; set; }
    public string Name { get; set; }
    public decimal Price { get; set; }
    public int Stock { get; set; }
}
```

---

# Endpoints da API

## Listar produtos

GET

```
/api/products
```

Retorna todos os produtos cadastrados.

---

## Buscar produto por ID

GET

```
/api/products/{id}
```

Retorna um produto específico.

---

## Criar produto

POST

```
/api/products
```

Exemplo de JSON:

```json
{
  "name": "Camiseta",
  "price": 79.90,
  "stock": 10
}
```

---

## Atualizar produto

PUT

```
/api/products/{id}
```

---

## Deletar produto

DELETE

```
/api/products/{id}
```

---

# Banco de Dados

O projeto utiliza **SQLite**, um banco de dados leve baseado em arquivo.

O banco é criado automaticamente com o nome:

```
products.db
```

O Entity Framework Core é responsável por criar as tabelas através de **migrations**.

---

# Como Executar o Projeto

### 1. Clonar o repositório

```
git clone https://github.com/seu-usuario/product-api-dotnet.git
```

---

### 2. Entrar na pasta do projeto

```
cd ProductApi
```

---

### 3. Restaurar dependências

```
dotnet restore
```

---

### 4. Criar o banco de dados

```
dotnet ef migrations add InitialCreate
dotnet ef database update
```

---

### 5. Rodar a aplicação

```
dotnet run
```

---

# Testando a API

Após executar o projeto, acesse o Swagger no navegador:

```
http://localhost:5200/swagger
```

O Swagger permite testar todos os endpoints da API diretamente pelo navegador.

---

# Estrutura do Banco

Tabela principal:

### Products

Campos:

* Id
* Name
* Price
* Stock

---

# Objetivo do Projeto

Este projeto foi desenvolvido com objetivo de praticar e demonstrar conhecimentos em:

* desenvolvimento de APIs REST
* arquitetura backend em camadas
* utilização do Entity Framework Core
* integração com banco de dados SQLite
* organização de código em projetos backend

---

# Autor

Diogo Augusto
Backend Developer
Python | Django | C# | .NET

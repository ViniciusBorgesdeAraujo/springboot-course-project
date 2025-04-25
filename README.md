# Projeto Spring Boot - API de Produtos

Este projeto é uma **API RESTful** desenvolvida com **Java** e **Spring Boot**. A aplicação é focada na gestão de produtos, com funcionalidades de CRUD, autenticação via **JWT** e segurança com **Spring Security**. Utiliza o banco de dados **PostgreSQL** para persistência de dados e **Spring Data JPA** para o gerenciamento da camada de dados.

## Tecnologias Utilizadas

- **Java 17+**
- **Spring Boot**
- **Spring Security** (com **JWT** para autenticação)
- **PostgreSQL** (para persistência de dados)
- **Spring Data JPA** (para interação com o banco de dados)
- **Maven** (para gerenciamento de dependências)
- **JWT** (JSON Web Token para autenticação)

## Funcionalidades

- **CRUD de Produtos**: Criação, leitura, atualização e exclusão de produtos na aplicação.
- **Autenticação com JWT**: Segurança no acesso aos endpoints através de tokens JWT.
- **Spring Security**: Proteção das rotas da API com **Spring Security**, garantindo que apenas usuários autenticados possam acessar os recursos.
- **Persistência com PostgreSQL**: Armazenamento de dados no banco de dados PostgreSQL utilizando **Spring Data JPA**.
- **Tratamento de Exceções**: Exceções personalizadas e globais para um melhor controle de erros e respostas para o cliente.
  
## Estrutura do Projeto

O projeto segue a seguinte estrutura básica:

```
src/main/java/com/example/meu_primeiro_springboot
  ├── controller      # Contém os controladores da API
  ├── model           # Modelos de dados, como Produto e Usuário
  ├── repository      # Repositórios para acessar o banco de dados
  ├── security        # Configurações de segurança (JWT, Spring Security)
  ├── service         # Lógica de negócios
  ├── exception       # Tratamento de exceções globais
```

## Como Rodar o Projeto

### Pré-requisitos

- **Java 17+** instalado
- **Maven** instalado
- **PostgreSQL** configurado localmente ou remotamente

### Passos para rodar

1. Clone o repositório:
   ```bash
   git clone https://github.com/ViniciusBorgesdeAraujo/springboot-course-project.git
   ```

2. Entre na pasta do projeto:
   ```bash
   cd springboot-course-project
   ```

3. Configure o banco de dados PostgreSQL. Adicione as credenciais de conexão no arquivo `src/main/resources/application.properties`:
   ```properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/seu_banco
   spring.datasource.username=seu_usuario
   spring.datasource.password=sua_senha
   spring.jpa.hibernate.ddl-auto=update
   ```

4. Execute o projeto:
   ```bash
   ./mvnw spring-boot:run
   ```

   Ou se preferir rodar com Maven:
   ```bash
   mvn spring-boot:run
   ```

5. A aplicação estará disponível na URL: `http://localhost:8080`

## Endpoints

A API possui os seguintes endpoints:

- **POST** `/api/produtos` - Criar um novo produto
- **GET** `/api/produtos` - Listar todos os produtos
- **GET** `/api/produtos/{id}` - Buscar um produto por ID
- **PUT** `/api/produtos/{id}` - Atualizar um produto
- **DELETE** `/api/produtos/{id}` - Excluir um produto


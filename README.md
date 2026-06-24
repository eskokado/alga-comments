# AlgaComments - Microsserviços de Comentários

Este projeto é uma demonstração de uma arquitetura de microsserviços para gerenciamento e moderação de comentários, desenvolvida com **Spring Boot 3** e **Java 21**.

## 🏗️ Arquitetura

O sistema é composto por dois microsserviços principais organizados via Git Submodules:

1.  **Comment Service** (Porta 8083): Responsável pelo CRUD de comentários e integração com o fluxo de moderação.
2.  **Moderation Service** (Porta 8084): Responsável por analisar o conteúdo dos comentários e decidir se são aprovados ou rejeitados com base em regras de negócio.

## 🚀 Como Executar

### Pré-requisitos

- Java 21+
- Git

### Clonando o Projeto

Como o projeto utiliza submodules, você deve clonar incluindo-os:

```bash
git clone --recursive https://github.com/eskokado/alga-comments.git
```

Ou, se já clonou:

```bash
git submodule update --init --recursive
```

### Executando os Serviços

Navegue até a pasta de cada módulo e execute via terminal:

```bash
# Terminal 1 - Moderation Service
cd microservices/moderation-service
./gradlew bootRun

# Terminal 2 - Comment Service
cd microservices/comment-service
./gradlew bootRun
```

## 🛠️ Tecnologias Utilizadas

- **Java 21**
- **Spring Boot 3**
- **Spring Data JPA**
- **H2 Database** (Persistência em memória/arquivo)
- **Lombok**
- **Spring Interface Clients** (Integração HTTP)

## 📝 Licença

Este projeto está sob a licença MIT.

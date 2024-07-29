# Santander Dev Week 2024
 - API em Java

Esta é a API da Santander em parceria com a DIO, desenvolvida em 2024, utilizando Java 17 com Spring Boot 3, oferecendo uma base robusta para aplicações modernas.

## Tecnologias Utilizadas
- **Java 17**: Utilizamos a versão LTS mais recente do Java para aproveitar as mais novas funcionalidades e melhorias da linguagem.
- **Spring Boot 3**: A mais recente versão do Spring Boot, otimizando o desenvolvimento com sua configuração automática e práticas recomendadas.
- **Spring Data JPA**: Facilita o acesso e manipulação de dados com bancos SQL, simplificando a camada de persistência.
- **OpenAPI (Swagger)**: Para criar uma documentação clara e detalhada da API, promovendo a transparência e facilidade de uso.
- **Railway**: Plataforma de deploy e monitoramento na nuvem, oferecendo serviços de banco de dados e pipelines de CI/CD.

## Design da API

### [Link do Figma](https://www.figma.com/file/0ZsjwjsYlYd3timxqMWlbj/SANTANDER---Projeto-Web%2FMobile?type=design&node-id=1421%3A432&mode=design&t=6dPQuerScEQH0zAn-1)

O Figma foi utilizado para projetar e abstrair o domínio da API, ajudando na visualização e planejamento da solução.

### Diagrama de Classes

```mermaid
classDiagram
  class User {
    -String name
    -Account account
    -Feature[] features
    -Card card
    -News[] news
  }

  class Account {
    -String number
    -String agency
    -Number balance
    -Number limit
  }

  class Feature {
    -String icon
    -String description
  }

  class Card {
    -String number
    -Number limit
  }

  class News {
    -String icon
    -String description
  }

  User "1" *-- "1" Account
  User "1" *-- "N" Feature
  User "1" *-- "1" Card
  User "1" *-- "N" News

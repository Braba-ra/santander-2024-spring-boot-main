# Publicando Sua API REST na Nuvem Usando Spring Boot 3, Java 17 e ~~Railway~~ Render

Ministrado por Venilton Falvo Jr. através da plataforma da DIO no Bootcamp Santander Fullstack Java.

## Principais Tecnologias
 - **Java 17**: Utilizaremos a versão LTS mais recente do Java para tirar vantagem das últimas inovações que essa linguagem robusta e amplamente utilizada oferece;
 - **Spring Boot 3**: Trabalharemos com a mais nova versão do Spring Boot, que maximiza a produtividade do desenvolvedor por meio de sua poderosa premissa de autoconfiguração;
 - **Spring Data JPA**: Exploraremos como essa ferramenta pode simplificar nossa camada de acesso aos dados, facilitando a integração com bancos de dados SQL;
 - **OpenAPI (Swagger)**: Vamos criar uma documentação de API eficaz e fácil de entender usando a OpenAPI (Swagger), perfeitamente alinhada com a alta produtividade que o Spring Boot oferece;

   
O projeto foi criado através do [Spring Initializr][(https://start.spring.io/#!type=gradle-project&language=java&platformVersion=3.1.4&packaging=jar&jvmVersion=17&groupId=dio&artifactId=santander-dev-2023&name=santander-dev-2023&description=Java%20RESTful%20API&packageName=dio.santander&dependencies=web,data-jpa,h2,postgresql)](https://start.spring.io/), importado e descompactado.

O projeto não foi publicado no Railway pois a versão de teste não suporta mais o versionamento do github, em vez disso, foi publicado no [Render][(https://render.com/)](https://dashboard.render.com/static/srv-cqvopiij1k6c73fcq51g) com o banco de dados PostgreSQL gratuito que expira automaticamente em 30 dias. (https://dashboard.render.com/)

## [Link do Figma](https://www.figma.com/file/0ZsjwjsYlYd3timxqMWlbj/SANTANDER---Projeto-Web%2FMobile?type=design&node-id=1421%3A432&mode=design&t=6dPQuerScEQH0zAn-1)

O Figma foi utilizado para a abstração do domínio desta API, sendo útil na análise e projeto da solução.

##Diagrama de Classes

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
        -float balance
        -float limit
    }

    class Feature {
        -String icon
        -String description
    }

    class Card {
        -String number
        -float limit
    }

    class News {
        -String icon
        -String description
    }

    User "1"*-- "1"Account
    User "1"*-- "N"Feature
    User "1"*-- "1"Card
    User"1" *-- "N"News
```

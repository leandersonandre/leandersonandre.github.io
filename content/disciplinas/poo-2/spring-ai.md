---
title: "Spring AI"
slug: "spring-ai"
description: "Spring AI"
tags:
- generative-ai
- spring-ai
---


## Definição

**Spring AI** é um framework de aplicações para engenharia de IA. Seu objetivo é aplicar ao domínio da IA ​​os princípios de design do ecossistema Spring, como portabilidade e design modular, e promover o uso de POJOs como blocos de construção de aplicações para IA.

## Funcionalidades

Spring AI fornece:

* Suporte para fornecedores de modelos de AI como Anthropic, OpenAI, Microsoft, Amazon, Google, and Ollama. Tipos de modelos inclui: Chat
  * Completion
  * Embedding
  * Text to Image
  * Audio Transcription
  * Text to Speech
  * Moderation
 
* Saidas estruturadas em POJOs
* Suporte para banco de dados de vetores
* Entre outros.

## Documentação oficial

Página oficial do [Spring AI](https://spring.io/projects/spring-ai)

Documentação do [Spring AI](https://docs.spring.io/spring-ai/reference/index.html)

## Criando um projeto 

Crie uma aplicação web Spring Boot com a dependência Spring AI OpenAI Boot Starter. Este [link do Spring Initializr](https://start.spring.io/) pode ajudar você a inicializar a aplicação. (Com o start.spring.io, você pode selecionar quaisquer modelos de IA ou armazenamentos de vetores que desejar usar em suas novas aplicações).

Selecione as dependências:

* Spring Web
* Spring Boot DevTools
* Mistral AI

Adicione sua chave [MistralAI](https://mistral.ai/) ao `applications.properties`:

```
spring.ai.mistralai.api-key=<SUA CHAVE MISTRAL-AI>
```

Adicione o seguinte trecho a sua classe `SpringAiDemoApplication`:

```java
@Bean
public CommandLineRunner runner(ChatClient.Builder builder) {
    return args -> {
        ChatClient chatClient = builder.build();
        String response = chatClient.prompt("Vai chover em Joinville?").call().content();							
        System.out.println(response);
    };
}
```

Execute o programa e configura a saída no terminal.

## Saída estruturada

O SpringAI permite solicitar uma saída estruturada do modelo de AI. Isso permite realizara conversão da resposta bruta do modelo para um tipo de dados específico.


O primeiro passo é criar o tipo de dados que deseja que a AI retorne.

```java
public record CidadeDTO(String nome, String estado, String pais) { }
```

Defina o prompt que será enviado para o modelo de AI.
```java
var meuPrompt = """
                Liste as 10 cidades (nome, estado e país) mais turísticas da Europa.
                """;
```

Indique no `chatCliente` o tipo de dados que será retornado.

```java
 var lista = chatClient.prompt()
              .user(meuPrompt)
              .call()
              // O tipo de dados que irá retornar.
              .entity(new ParameterizedTypeReference<List<CidadeDTO>>() {}); 
```

Exemplo completo:
```java
@Bean
public CommandLineRunner runner(ChatClient.Builder builder) {
    return args -> {
        var meuPrompt = """
            Liste as 10 cidades (nome, estado e país) mais turísticas da Europa.
            """;
        ChatClient chatClient = builder.build();
        var lista = chatClient.prompt()
                .user(meuPrompt)
                .call()
                .entity(new ParameterizedTypeReference<List<CidadeDTO>>() {});
        System.out.println(String.format("%-20s", "Cidade")+"\t\t\t\t"+String.format("%-20s", "Estado")+"\t\t\t\tPaís");
        System.out.println("-----------------------------------------------------------------------------------------");
        for(var cidade : lista) {
            System.out.println(String.format("%-20s", cidade.nome())+"\t\t\t\t"+String.format("%-20s", cidade.estado())+"\t\t\t\t"+cidade.pais());
        }
    };
}
```

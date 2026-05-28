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

Adicione sua chave MistralAI ao `applications.properties`:

```
spring.ai.openai.api-key=<SUA CHAVE MISTRAL-AI>
```

Adicione o seguinte trecho a sua classe `SpringAiDemoApplication`:

```java
@Bean
public CommandLineRunner runner(ChatClient.Builder builder) {
    return args -> {
        ChatClient chatClient = builder.build();
        String response = chatClient.prompt("Vai chover hoje em Joinville?").call().content();							
        System.out.println(response);
    };
}
```

Execute o programa e configura a saída no terminal.

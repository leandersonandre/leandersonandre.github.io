---
title : "Spring AI : Saída Estruturada"
slug: "spring-ai"
outputs : ["Reveal"]
reveal_hugo:
  theme: "serif"
  custom_css: "css/univille.css"
---

{{% slide-capa titulo="Spring AI: Saída Estruturada" subtitulo="Programação Orientada a Objetos II" %}}

---

## Saída Estruturada

{{% block titulo="Definição" %}}
O Spring AI permite converter a resposta do modelo de IA em um objeto Java, utilizando uma estrutura de dados previamente definida.
{{% /block %}}

___

#  Crie o DTO


{{% block titulo="Definição" %}}
**DTO (Data Transfer Object)** é um objeto utilizado para transportar dados entre diferentes partes de um sistema, definindo os atributos que compõem essas informações.
{{% /block %}}

```java
public record CidadeDTO(String nome, String estado, String pais) { }
```

___

#  Define o prompt

{{% block titulo="Instrução" %}}
Descreva no prompt as informações que deseja obter do modelo de IA e o formato esperado para a resposta.
{{% /block %}}

```java
var meuPrompt = """
   Liste as 10 cidades mais turísticas da Europa,
   informando o nome, estado (ou região) e país.
                """;
```
___

#  Ajuste a chamada da GenAI

Utilize o método `entity()` para converter a resposta do modelo em objetos Java do tipo desejado.


```java
var lista = chatClient.prompt()
  .user(meuPrompt)
  .call()
  // O tipo de dados que irá retornar.
  .entity(new ParameterizedTypeReference<List<CidadeDTO>>() {}); 
```

___

{{% slide-contracapa %}}

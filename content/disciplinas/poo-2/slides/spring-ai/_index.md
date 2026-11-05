---
title : "Spring AI"
slug: "spring-ai"
outputs : ["Reveal"]
reveal_hugo:
  theme: "serif"
  custom_css: "css/univille.css"
---

{{% slide-capa titulo="Spring AI" subtitulo="Programação Orientada a Objetos II" %}}

---

## Spring AI

{{% block titulo="Definição" %}}
Framework de aplicações para engenharia de IA. Seu objetivo é aplicar ao domínio da IA os princípios de design do ecossistema Spring, como portabilidade e modularidade, promovendo o uso de POJOs como blocos de construção de aplicações para IA.
{{% /block %}}

---

## Spring AI

<img src="https://images.ctfassets.net/mnrwi97vnhts/4mda205vy509Dx3vGkMwFr/af520e66dc79fb80cd1bc129a11d6d23/spring-ai-integration-diagram-3.svg" height="300">

Em sua essência, o Spring AI aborda o desafio fundamental da integração de IA: conectar os **Dados** e as **APIs** da sua empresa aos **Modelos de IA**.

---

## Modelos e recursos do Spring AI

Spring AI fornece suporte para fornecedores de modelos de AI. Tipos de modelos inclui: 

<table>
  <thead>
    <tr>
      <th>Modelos e tarefas</th>
      <th>Recursos</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><small>Chat Completion</small></td>
      <td><small>Saídas estruturadas em POJOs</small></td>
    </tr>
    <tr>
      <td><small>Embedding</small></td>
      <td><small>Tool Calling</small></td>
    </tr>
    <tr>
      <td><small>Text to Image</small></td>
      <td><small>Moderação de conteúdo</small></td>
    </tr>
    <tr>
      <td><small>Audio Transcription</small></td>
      <td><small>RAG (Retrieval-Augmented Generation)</small></td>
    </tr>
    <tr>
      <td><small>Text to Speech</small></td>
      <td><small>Integração com bancos de dados vetoriais</small></td>
    </tr>
    <tr>
      <td><small>Geração de áudio e vídeo</small></td>
      <td><small>Entre outros recursos</small></td>
    </tr>
  </tbody>
</table>

___

# Inteligência Artificial Generativa

{{% block titulo="Definição" %}}
IA Generativa ( do inglês, *Generative AI*) é um ramo da Inteligência Artificial capaz de criar novos conteúdos, como textos, imagens, áudios, vídeos e códigos, a partir de instruções ou exemplos fornecidos pelo usuário.

Ela utiliza modelos treinados com grandes volumes de dados para aprender padrões e relações permitindo gerar conteúdos com base nesses aprendizados.
{{% /block %}}

___ 

# Relação entre a grande área da IA e IA Generativa


<div style="display:flex; justify-content:center; width:100%;">
<svg viewBox="0 0 700 570" style="width:100%; max-width:700px; height:auto;">
  <circle cx="350" cy="285" r="275" fill="#dbeafe" stroke="#2563eb" stroke-width="2"/>
  <text x="350" y="60" text-anchor="middle" font-size="18" font-weight="bold" fill="#1e3a8a">Inteligência Artificial (IA)</text>

  <circle cx="350" cy="305" r="225" fill="#bfdbfe" stroke="#2563eb" stroke-width="2"/>
  <text x="350" y="130" text-anchor="middle" font-size="17" font-weight="bold" fill="#1e40af">Machine Learning (ML)</text>

  <circle cx="350" cy="325" r="175" fill="#bbf7d0" stroke="#16a34a" stroke-width="2"/>
  <text x="350" y="190" text-anchor="middle" font-size="16" font-weight="bold" fill="#166534">Deep Learning (DL)</text>

  <circle cx="350" cy="365" r="125" fill="#fef3c7" stroke="#d97706" stroke-width="2"/>
  <text x="350" y="265" text-anchor="middle" font-size="17" font-weight="bold" fill="#92400e">GenAI</text>

  <g font-size="14" text-anchor="middle" fill="#92400e">
    <rect x="285" y="278" width="130" height="29" rx="7" fill="white" stroke="#d97706"/>
    <text x="350" y="298">LLMs (Texto)</text>
    <rect x="285" y="313" width="130" height="29" rx="7" fill="white" stroke="#d97706"/>
    <text x="350" y="333">Imagens</text>
    <rect x="285" y="348" width="130" height="29" rx="7" fill="white" stroke="#d97706"/>
    <text x="350" y="368">Áudio</text>
    <rect x="285" y="383" width="130" height="29" rx="7" fill="white" stroke="#d97706"/>
    <text x="350" y="403">Vídeo</text>
    <rect x="285" y="418" width="130" height="29" rx="7" fill="white" stroke="#d97706"/>
    <text x="350" y="438">Música</text>
  </g>
</svg>
</div>

----

# A magia das Inteligências Artificiais Generativas

IA Generativa combina conceitos de geometria, álgebra linear, estatística e probabilidade com redes neurais para aprender padrões em grandes volumes de dados e gerar novos conteúdos.


<img src="https://i.ytimg.com/vi/JkoSAwJUwAo/hqdefault.jpg" height="300">

___

# 2017: Um marco na evolução da IA Generativa

A atual revolução da IA Generativa tem um de seus principais marcos em 2017, com a publicação do artigo [*Attention Is All You Need*](https://arxiv.org/abs/1706.03762), por pesquisadores do Google, que apresentou a arquitetura Transformer.

___

# Arquitetura original do Transformer

<img src="https://arxiv.org/html/1706.03762v7/Figures/ModalNet-21.png" height="600">


___

# Por que a IA Generativa ganhou tanta relevância recentemente?

<table>
  <thead>
    <tr>
      <th>Fator</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><small>Avanços tecnológicos</small></td>
      <td><small>Novas arquiteturas, como Transformers, e modelos LLMs.</small></td>
    </tr>
    <tr>
      <td><small>Capacidade computacional</small></td>
      <td><small>Evolução das GPUs e do processamento paralelo.</small></td>
    </tr>
    <tr>
      <td><small>Disponibilidade de dados</small></td>
      <td><small>Grandes volumes de dados para treinamento dos modelos.</small></td>
    </tr>
    <tr>
      <td><small>Novas categorias de software</small></td>
      <td><small>Assistentes inteligentes, geradores de conteúdo e agentes de IA.</small></td>
    </tr>
  </tbody>
</table>

___

# Spring AI

Spring AI facilita o desenvolvimento de aplicações que integram recursos de Inteligência Artificial Generativa.

___

# Criando um projeto

Crie um novo projeto spring com as dependências:

* Spring Web
* Spring Boot DevTools
* OpenAI

___

# Criando um projeto

Configure o application.properties

```
spring.ai.openai.api-key=SUA_CHAVE_DE_API
spring.ai.openai.base-url=https://openrouter.ai/api/v1
spring.ai.openai.chat.model=openrouter/free
```

___

# Criando uma chave de api


O uso de modelos de Inteligência Artificial via API pode ser cobrado de acordo com a quantidade de tokens processados. Alguns provedores também disponibilizam modelos com utilização gratuita e limitações. Por exemplo a [OpenRouter](https://openrouter.ai).


Crie uma chave com data de expiração e limitação de créditos.


Utilize as APIs com cuidado, e jamais, adicione o seu cartão de crédito!

___


# Criando um projeto


<img src="https://media.tenor.com/sLgNruA4tsgAAAAM/warning-lights.gif">

JAMAIS COMPARTILHA A SUA CHAVE API NA INTERNET, CHAT, WHATSAPP, EMAIL, REPOSITÓRIOS GITHUB, ETC.

Se isso acontecer, revogue IMEDIATAMENTE a chave

___

# Criando um projeto


Adicione o seguinte trecho a sua classe **SpringAiDemoApplication:**

```java
@Bean
public CommandLineRunner runner(ChatClient.Builder builder) {
  return args -> {

    ChatClient chatClient = builder.build();
      String response = chatClient
        .prompt("Quantos lados tem um quadrado?")
        .call().content();
    System.out.println(response);
  };
}

```

___

{{% slide-contracapa %}}

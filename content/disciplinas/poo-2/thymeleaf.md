---
title: "Thymeleaf"
slug: "thymeleaf"
description: "Introdução ao Thymeleaf com Spring Boot, controllers e templates HTML dinâmicos."
tags:
- thymeleaf
---


## Definição

**Thymeleaf** é um mecanismo de templates para Java (Java Template Engine), utilizado principalmente no desenvolvimento de aplicações web com Spring Boot para gerar páginas HTML dinâmicas no servidor.

Ele permite combinar HTML com expressões e atributos especiais que acessam dados enviados pelo controlador (Controller), exibindo informações, preenchendo formulários e criando páginas dinâmicas.

## Principais características

Thymeleaf fornece:

*  Integração com Spring Boot: facilita a comunicação entre controllers e páginas HTML.
* Renderização no servidor: o HTML é processado no servidor antes de ser enviado ao navegador.
* Acesso a dados: permite exibir atributos de objetos Java nas páginas.
* Formulários: facilita preencher, enviar e validar dados.
* HTML natural: os arquivos continuam sendo HTML válido, mesmo com os atributos do Thymeleaf.

## Documentação oficial

Página oficial do [Thymeleaf](https://www.thymeleaf.org)

Documentação do [Thymeleaf](https://www.thymeleaf.org/documentation.html)

## Hello World com Thymeleaf 

Crie uma aplicação web Spring Boot com a dependência Thymeleaf e Spring Web. Este [link do Spring Initializr](https://start.spring.io/) pode ajudar você a inicializar a aplicação.

Selecione as dependências:

* Spring Web
* Thymeleaf
* Spring Boot DevTools (opcional, para facilitar o desenvolvimento)


### Controller

Crie um controller `HelloController` que retorne uma página html.

```java
@Controller
@RequestMapping("/hello")
public class HelloController{
    
    @GetMapping
    public ModelAndView index(){
      ModelAndView mv = new ModelAndView("hello");

      return mv;
    }
}
```

A classe `ModelAndView` é responsável por combinar a visão (`hello.html`) com os objetos que devem ser manipulados pelo Thymeleaf. Para adicionar os objetos no `ModelAndView` se utiliza o método `addObject` informando a chave e o valor. A chave será utilizada para acessar o objeto dentro do arquivo html.

```java
@Controller
@RequestMapping("/hello")
public class HelloController{
    
    @GetMapping
    public ModelAndView index(){
      ModelAndView mv = new ModelAndView("hello");
      // usuario é a chave
      // Tom Cruise é o valor associado a chave "usuario"
      mv.addObject("usuario","Tom Cruise");
      
      return mv;
    }
}
```
A chave `usuario` será usada na expressão `${usuario}` no HTML.

É permitido adicionar vários objetos, desde que, cada um tenha uma chave única.

### Página HTML

A página `hello.html` deve ser criada na pasta `templates` nos `resources` do projeto (`src/main/resources/templates/hello.html`).

```html
<!DOCTYPE html>
<html lang="pt-BR" xmlns:th="http://www.thymeleaf.org">
  <head>
    <meta charset="UTF-8">
    <title>Hello World</title>
  </head>
  <body>
    <h1>Olá Thymeleaf</h1>
    <p>Bem vindo </p>
  </body>
</html>
```

### Utilizando o Thymeleaf

O Thymeleaf permite utilizar atributos especiais nos elementos HTML, geralmente identificados pelo prefixo `th`. Para exibir uma string ou outro valor como conteúdo textual de um elemento HTML, pode-se utilizar o atributo `th:text`.

```html
<p>Bem vindo <span th:text="${usuario}"></span></p>
```

Se o controller disponibilizar o atributo `usuario` com o valor `Tom Cruise`, o resultado será:

```html
<p>Bem vindo <span>Tom Cruise</span></p>
```

Além disso, o `th:text` escapa caracteres HTML especiais, ajudando a evitar que um valor fornecido pelo usuário seja interpretado como HTML.


## Condicionais

O Thymeleaf permite utilizar estruturas condicionais para controlar quais elementos HTML serão exibidos de acordo com determinadas condições. Para isso, disponibiliza os atributos `th:if`, `th:unless` e `th:switch`.

### th:if

O atributo `th:if` permite exibir um elemento HTML somente quando uma condição for verdadeira.

```html
<p th:if="${idade >= 18}">
    Maior de idade
</p>
```

Neste exemplo, o parágrafo será exibido somente se o atributo `idade` disponibilizado pelo Controller tiver um valor maior ou igual a 18.

Se a condição for falsa, o elemento não será incluído no HTML gerado.

### th:unless

O atributo `th:unless` funciona de maneira inversa ao `th:if`: o elemento será exibido quando a condição for falsa.

```html
<p th:unless="${idade >= 18}">
    Menor de idade
</p>
```

Neste exemplo, o parágrafo será exibido quando o valor de `idade` for menor que 18.

### th:switch e th:case

Os atributos `th:switch` e `th:case` permitem selecionar qual conteúdo será exibido de acordo com o valor de uma expressão. São semelhantes à estrutura `switch-case` da linguagem Java.

```html
<div th:switch="${dia}">
    <p th:case="1">Domingo</p>
    <p th:case="2">Segunda-feira</p>
    <p th:case="3">Terça-feira</p>
    <p th:case="4">Quarta-feira</p>
    <p th:case="5">Quinta-feira</p>
    <p th:case="6">Sexta-feira</p>
    <p th:case="7">Sábado</p>
    <p th:case="*">Dia inválido</p>
</div>
```

Neste exemplo, o valor do atributo `dia` determina qual parágrafo será exibido. Se o valor for `1`, será exibido o texto "Domingo"; se for `2`, será exibido "Segunda-feira", e assim sucessivamente.

O atributo `th:case="*"` funciona como a opção padrão, sendo utilizado quando nenhum dos casos anteriores corresponde ao valor informado.

Dessa forma, as estruturas condicionais do Thymeleaf permitem controlar dinamicamente a apresentação dos elementos HTML de acordo com os dados disponibilizados pela aplicação Java.

## Iteração

O Thymeleaf permite percorrer coleções de objetos e gerar elementos HTML dinamicamente. Para isso, utiliza-se o atributo `th:each`, que funciona de maneira semelhante às estruturas de repetição, como o `for-each` da linguagem Java.

### th:each

O atributo `th:each` permite percorrer uma coleção, como uma lista (`List`), e gerar um elemento HTML para cada item.

Considere um Controller que disponibiliza uma lista de nomes de países:

```java
@Controller
@RequestMapping("/paises")
public class PaisController {

    @GetMapping
    public ModelAndView listar() {
        ModelAndView mv = new ModelAndView("paises");

        List<String> paises = List.of(
            "Brasil",
            "Argentina",
            "Chile"
        );

        mv.addObject("paises", paises);

        return mv;
    }
}
```

Nesse exemplo, o método `addObject()` disponibiliza a lista de países com a chave `paises`, que será utilizada no template HTML.

Na página `paises.html`, podemos utilizar o atributo `th:each` para percorrer a lista:

```html
<!DOCTYPE html>
<html lang="pt-BR" xmlns:th="http://www.thymeleaf.org">
<head>
    <meta charset="UTF-8">
    <title>Países</title>
</head>
<body>
    <h1>Lista de países</h1>

    <ul>
        <li th:each="pais : ${paises}"
            th:text="${pais}">
        </li>
    </ul>
</body>
</html>
```

A expressão `th:each="pais : ${paises}"` indica que o Thymeleaf deve percorrer a coleção `paises`, atribuindo cada elemento à variável `pais`.

Para cada item da lista, será gerado um elemento HTML `<li>` com o nome do país correspondente.

O resultado será semelhante a:

```html
<ul>
    <li>Brasil</li>
    <li>Argentina</li>
    <li>Chile</li>
</ul>
```

### Iteração sobre uma lista de objetos

O `th:each` também pode ser utilizado para percorrer uma coleção de objetos Java e acessar seus atributos.

Considere a seguinte classe `Pais`:

```java
public class Pais {

    private String nome;
    private String capital;

    public Pais(String nome, String capital) {
        this.nome = nome;
        this.capital = capital;
    }

    public String getNome() {
        return nome;
    }

    public String getCapital() {
        return capital;
    }
}
```

O Controller pode disponibilizar uma lista de objetos `Pais`:

```java
List<Pais> paises = List.of(
    new Pais("Brasil", "Brasília"),
    new Pais("Argentina", "Buenos Aires"),
    new Pais("Chile", "Santiago")
);

mv.addObject("paises", paises);
```

No template HTML, podemos acessar as propriedades de cada objeto utilizando expressões do Thymeleaf:

```html
<table>
    <thead>
        <tr>
            <th>País</th>
            <th>Capital</th>
        </tr>
    </thead>
    <tbody>
        <tr th:each="pais : ${paises}">
            <td th:text="${pais.nome}"></td>
            <td th:text="${pais.capital}"></td>
        </tr>
    </tbody>
</table>
```

Nesse exemplo, o Thymeleaf percorre a lista `paises` e gera uma linha da tabela para cada objeto. As expressões `${pais.nome}` e `${pais.capital}` acessam as propriedades do objeto atual por meio dos métodos de acesso correspondentes.

Dessa forma, o `th:each` permite construir listas, tabelas e outros elementos HTML a partir de coleções de dados disponibilizadas pela aplicação Java.

## Navegação e URLs de imagens

O Thymeleaf disponibiliza atributos que permitem gerar URLs dinamicamente para links, formulários e imagens. Entre eles, destacam-se `th:href`, `th:action` e `th:src`.

### th:href

O atributo `th:href` permite definir dinamicamente o endereço de um link HTML. É útil para navegar entre páginas da aplicação e construir URLs que contenham parâmetros.

```html
<a th:href="@{/paises}">Listar países</a>
```

Nesse exemplo, o Thymeleaf gera um link para o caminho `/paises`, considerando o contexto da aplicação.

Também é possível incluir parâmetros na URL:

```html
<a th:href="@{/pais(id=1)}">Consultar país</a>
```

O Thymeleaf gera uma URL equivalente a `/pais?id=1`.

Para utilizar valores de variáveis na URL, pode-se escrever:

```html
<a th:href="@{/pais(id=${pais.id})}">
    Consultar país
</a>
```

Nesse caso, o valor de `pais.id` será utilizado como parâmetro da URL.

### th:action

O atributo `th:action` permite definir dinamicamente o endereço para o qual um formulário HTML será enviado.

```html
<form th:action="@{/paises}" method="get">
    <input type="text" name="nome">
    <button type="submit">Pesquisar</button>
</form>
```

Nesse exemplo, o formulário envia uma requisição HTTP GET para `/paises`, incluindo o valor digitado no campo `nome` como parâmetro da requisição.

O atributo `th:action` é especialmente útil em formulários de cadastro, edição e pesquisa.

### th:src

O atributo `th:src` permite definir dinamicamente o endereço de uma imagem. Pode ser utilizado tanto com imagens externas quanto com arquivos disponibilizados pela própria aplicação.

**Imagem externa**

```html
<img src="https://exemplo.com/imagens/brasil.png"
     alt="Bandeira do Brasil">
```

Se o endereço for fixo, o atributo HTML `src` é suficiente. O Thymeleaf não precisa ser utilizado nesse caso.

**Imagem com URL dinâmica**

```html
<img th:src="${pais.bandeira}"
     th:alt="|Bandeira de ${pais.nome}|">
```

Nesse exemplo, o endereço da imagem é obtido do atributo `bandeira` do objeto `pais`, enquanto o texto alternativo é construído com o nome do país.

**Imagem armazenada na aplicação**

Se a imagem estiver na pasta `src/main/resources/static/imagens`, ela poderá ser referenciada assim:

```html
<img th:src="@{/imagens/logo.png}"
     alt="Logo da aplicação">
```

O Thymeleaf gera a URL considerando o contexto da aplicação, facilitando o acesso ao arquivo estático.

### Resumo dos atributos

| Atributo | Finalidade |
|---|---|
| `th:href` | Define URLs de links. |
| `th:action` | Define o destino de formulários. |
| `th:src` | Define URLs de imagens e outros recursos compatíveis com `src`. |

Esses atributos permitem gerar URLs dinamicamente e integrar a navegação das páginas HTML aos dados e às rotas disponibilizados pela aplicação Spring Boot.

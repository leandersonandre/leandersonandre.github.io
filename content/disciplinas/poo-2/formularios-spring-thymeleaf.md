---
title: "Formulários com Spring Boot e Thymeleaf"
slug: "formularios-spring-thymeleaf"
description: "Aprenda a criar formulários HTML com Thymeleaf e processar dados com Spring Boot."
tags:
- spring-boot
- thymeleaf
- formularios
---

## Definição

Formulários HTML permitem que os usuários enviem informações para uma aplicação web, como dados de cadastro, pesquisa e edição.

Em aplicações desenvolvidas com Spring Boot e Thymeleaf, os formulários podem ser integrados aos controllers para receber, processar e apresentar os dados enviados pelo usuário.

O Thymeleaf disponibiliza atributos como `th:action`, `th:object` e `th:field`, que facilitam a associação entre os campos HTML e os objetos Java.

## Criando a classe de domínio

Para demonstrar o funcionamento de um formulário, será utilizado o cadastro de países.

Crie a classe `Pais` com os atributos `nome` e `capital`.

```java
public class Pais {

    private String nome;
    private String capital;

    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public String getCapital() {
        return capital;
    }

    public void setCapital(String capital) {
        this.capital = capital;
    }
}
```

Os métodos getters e setters permitem que o Spring e o Thymeleaf acessem e atualizem os atributos do objeto.

## Criando o Controller

O Controller será responsável por apresentar o formulário e receber os dados enviados pelo usuário.

Crie a classe `PaisController`:

```java
@Controller
@RequestMapping("/paises")
public class PaisController {

    @GetMapping("/novo")
    public ModelAndView novo() {
        ModelAndView mv = new ModelAndView("pais-form");
        mv.addObject("pais", new Pais());

        return mv;
    }

    @PostMapping
    public ModelAndView salvar(@ModelAttribute Pais pais) {
        ModelAndView mv = new ModelAndView("pais-resultado");
        mv.addObject("pais", pais);

        return mv;
    }
}
```

O método `novo()` responde a uma requisição HTTP GET para `/paises/novo`. Ele disponibiliza um objeto `Pais` vazio para preencher o formulário.

O método `salvar()` responde a uma requisição HTTP POST para `/paises`. O Spring utiliza os dados enviados pelo formulário para preencher o objeto `Pais`, recebido pelo parâmetro anotado com `@ModelAttribute`.

Neste exemplo, os dados são apenas recebidos e apresentados na resposta. O cadastro ainda não é persistido em um banco de dados.

## Criando o formulário HTML

Crie o arquivo `pais-form.html` na pasta `src/main/resources/templates`.

```html
<!DOCTYPE html>
<html lang="pt-BR" xmlns:th="http://www.thymeleaf.org">
<head>
    <meta charset="UTF-8">
    <title>Cadastro de país</title>
</head>
<body>
    <h1>Cadastro de país</h1>

    <form th:action="@{/paises}"
          th:object="${pais}"
          method="post">

        <label for="nome">Nome:</label>
        <input type="text"
               id="nome"
               th:field="*{nome}"
               required>

        <label for="capital">Capital:</label>
        <input type="text"
               id="capital"
               th:field="*{capital}"
               required>

        <button type="submit">Salvar</button>
    </form>
</body>
</html>
```

O formulário utiliza três atributos importantes do Thymeleaf:

- `th:action="@{/paises}"`: define o endereço para o qual os dados serão enviados.
- `th:object="${pais}"`: associa o formulário ao objeto `pais` disponibilizado pelo Controller.
- `th:field="*{nome}"` e `th:field="*{capital}"`: associam os campos HTML aos atributos do objeto.

A expressão `*{...}` acessa propriedades do objeto definido em `th:object`. Dessa forma, `*{nome}` corresponde à propriedade `nome` do objeto `pais`.

O atributo `method="post"` indica que o formulário enviará os dados por meio de uma requisição HTTP POST.

## Exibindo os dados enviados

Após o envio do formulário, o Controller disponibiliza o objeto preenchido para a página `pais-resultado.html`.

Crie o arquivo em `src/main/resources/templates/pais-resultado.html`:

```html
<!DOCTYPE html>
<html lang="pt-BR" xmlns:th="http://www.thymeleaf.org">
<head>
    <meta charset="UTF-8">
    <title>País cadastrado</title>
</head>
<body>
    <h1>Dados recebidos</h1>

    <p>
        País:
        <span th:text="${pais.nome}"></span>
    </p>

    <p>
        Capital:
        <span th:text="${pais.capital}"></span>
    </p>

    <a th:href="@{/paises/novo}">Cadastrar outro país</a>
</body>
</html>
```

O atributo `th:text` apresenta os valores recebidos do Controller. Como o Thymeleaf escapa caracteres HTML especiais por padrão nessa expressão, os valores são exibidos como texto, em vez de serem interpretados como marcação HTML.

## Testando a aplicação

Execute a aplicação Spring Boot e acesse o endereço:

`http://localhost:8080/paises/novo`

Preencha os campos com o nome de um país e sua capital e clique em **Salvar**.

O navegador enviará uma requisição POST para `/paises`. O Spring preencherá o objeto `Pais` com os valores informados e o Controller retornará a página com os dados recebidos.

## Resumo

Neste exemplo, foram utilizados os seguintes recursos:

- `@GetMapping`: disponibiliza a página do formulário.
- `@PostMapping`: recebe os dados enviados pelo formulário.
- `@ModelAttribute`: associa os dados da requisição a um objeto Java.
- `th:action`: define o destino do formulário.
- `th:object`: associa o formulário a um objeto.
- `th:field`: associa os campos do formulário às propriedades do objeto.
- `th:text`: apresenta os dados na página HTML.

Essa integração permite criar formulários dinâmicos com HTML e Thymeleaf, processando as requisições com Spring Boot. Em uma aplicação real, o próximo passo seria adicionar validação dos dados e persistência em um banco de dados.

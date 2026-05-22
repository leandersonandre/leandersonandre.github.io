---
title: "Formulários"
slug: "formularios"
description: "Formularios em HTML"
tags:
- html
- formularios
- inputs
---

Um formulário é utilizado para coletar dados do usuário. Geralmente os dados são enviados para um servidor para ser processado.

```html
<form>

</form>
```

### Elemento input

O elemento input é um dos campos mais utilizados para coletar os dados do usuário. O elemento input permite informar uma gama diferente de informações. O atributo ```type``` define o tipo de campo e layout.

```html
<input type="button">
<input type="checkbox">
<input type="color">
<input type="date">
<input type="datetime-local">
<input type="email">
<input type="file">
<input type="hidden">
<input type="image">
<input type="month">
<input type="number">
<input type="password">
<input type="radio">
<input type="range">
<input type="reset">
<input type="search">
<input type="submit">
<input type="tel">
<input type="text">
<input type="time">
<input type="url">
<input type="week">
```

O layout e tipo de informação do campo depende do navegador utilizado. Caso o navegador não suportar, o campo input assume o tipo ```text```.


### Atributos do input

O elemento input possui os atributos ```id```, ```name```, ```value``` e ```placeholder```.

```html
<input
    type="text"
    id="nome"
    name="nome"
    value="João"
    placeholder="Digite seu nome">
```
| Atributo      | Descrição                                                                                                  |
| ------------- | ---------------------------------------------------------------------------------------------------------- |
| `id`          | Identifica unicamente o elemento na página. É muito usado para CSS, JavaScript e associação com `<label>`. |
| `name`        | Define o nome do campo enviado ao servidor quando o formulário é submetido.                                |
| `value`       | Define o valor inicial do campo ou o valor associado ao input.                                             |
| `placeholder` | Exibe um texto de exemplo ou dica dentro do campo enquanto ele estiver vazio.                              |


## Labels

O elemento `label` define um texto para explicar qual conteúdo deve ser informado em um campo de formulário (`input`).

O `label` é associado a um `input` por meio do atributo `for`, cujo valor deve ser igual ao atributo `id` do `input` correspondente.

```html
<label for="nome">Nome:</label>
<input type="text" id="nome" name="nome" placeholder="Digite seu nome">
```

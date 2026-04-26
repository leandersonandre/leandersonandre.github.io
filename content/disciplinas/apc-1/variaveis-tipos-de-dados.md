---
title: "Variáveis e tipos de dados"
slug: variaveis-tipos-de-dados
description: "Variáveis e tipos de dados em Python"
tags:
- python
- variável
- tipo de dados
---


Em Python, uma variável é utilizada para armazenar valores na memória. Esses valores podem ser utilizados, modificados e reutilizados ao longo do programa.

## Variáveis

Para criar uma variável, basta atribuir um valor utilizando o operador `=`.

```python
x = 10
nome = "Ana"
```

Neste caso, `x` armazena um número e `nome` armazena um texto.

O nome da variável deve seguir algumas regras:
- Não pode começar com número
- Não pode conter espaços
- Deve evitar palavras reservadas da linguagem


## Tipagem dinâmica

Python é uma linguagem de tipagem dinâmica. Isso significa que não é necessário declarar o tipo da variável, pois ele é definido automaticamente.

```python
x = 10       # inteiro
x = "texto"  # agora é uma string
```

A variável pode mudar de tipo ao longo do programa.


## Tipos básicos de dados

### Inteiros (int)

Representam números inteiros.

```python
idade = 25
```


### Números reais (float)

Representam números com casas decimais.

```python
altura = 1.75
```


### Texto (str)

Representa sequências de caracteres.

```python
nome = "João"
mensagem = 'Olá mundo'
```


### Booleano (bool)

Representa valores lógicos: verdadeiro ou falso.

```python
ativo = True
aprovado = False
```


## Verificando o tipo

A função `type()` permite verificar o tipo de uma variável.

```python
x = 10
print(type(x))
```


## Conversão de tipos

É possível converter valores entre diferentes tipos de dados.

```python
x = "10"
y = int(x)

z = 3.5
w = int(z)
```

Outras conversões comuns:

- `int()` → inteiro  
- `float()` → número real  
- `str()` → texto  
- `bool()` → booleano  


## Entrada de dados

A função `input()` permite ler dados do usuário. O valor lido é sempre do tipo string.

```python
nome = input("Digite seu nome: ")
print(nome)
```

Para trabalhar com números, é necessário converter o valor:

```python
idade = int(input("Digite sua idade: "))
```

## Observação

Variáveis são fundamentais para armazenar e manipular informações. O tipo de dado define quais operações podem ser realizadas com cada valor.

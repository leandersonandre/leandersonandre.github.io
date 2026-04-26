---
title: "Decisões"
slug: "decisoes"
description: "Estrutura de decisões em Python"
tags:
- python
- if-else-elif
- decisões
---

A linguagem Python permite controlar o fluxo de execução de um programa através de estruturas de decisão. Essas estruturas permitem executar diferentes blocos de código com base em condições.

## If

A estrutura **if** é utilizada para executar um bloco de código somente se uma condição for verdadeira.

```python
idade = 18

if idade >= 18:
    print("Maior de idade")
``` 

Neste caso, a mensagem será exibida apenas se a condição `idade >= 18` for verdadeira.


## If e else

A estrutura **if-else** permite definir um caminho alternativo quando a condição não é satisfeita.

```python
idade = 16

if idade >= 18:
    print("Maior de idade")
else:
    print("Menor de idade")
```

Se a condição for verdadeira, o bloco do `if` é executado. Caso contrário, o bloco do `else` será executado.


## If, elif e else

Quando existem múltiplas condições, utiliza-se o **elif** (else if).

```python
nota = 7

if nota >= 9:
    print("Excelente")
elif nota >= 7:
    print("Bom")
elif nota >= 5:
    print("Regular")
else:
    print("Reprovado")
```

As condições são avaliadas de cima para baixo. Assim que uma condição é verdadeira, as demais não são executadas.


## Condições

As decisões são baseadas em expressões que resultam em verdadeiro ou falso.

```python
x = 10

if x > 5:
    print("Maior que 5")
```

Operadores comuns em condições:

* `==` igual
* `!=` diferente
* `>` maior
* `<` menor
* `>=` maior ou igual
* `<=` menor ou igual


## Operadores lógicos

É possível combinar múltiplas condições utilizando operadores lógicos.

```python
idade = 20
tem_carteira = True

if idade >= 18 and tem_carteira:
    print("Pode dirigir")
```

Também existem:

* `and` → e
* `or` → ou
* `not` → negação


## Estruturas aninhadas

Assim como nos laços, estruturas de decisão podem ser aninhadas.

```python
idade = 20

if idade >= 18:
    if idade >= 65:
        print("Idoso")
    else:
        print("Adulto")
else:
    print("Menor de idade")
```


## Expressão condicional (forma reduzida)

Python permite escrever decisões simples em uma única linha.

```python
idade = 18
resultado = "Maior" if idade >= 18 else "Menor"
print(resultado)
```

Essa forma é útil para simplificar atribuições condicionais.


## Observação

A identação (espaços no início das linhas) é obrigatória em Python e define quais comandos pertencem a cada bloco de decisão.

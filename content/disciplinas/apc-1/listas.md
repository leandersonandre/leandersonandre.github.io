---
title: "Listas"
slug: "listas"
description: "Listas em Python"
tags:
- python
- lista
---

Uma **lista** é uma estrutura de dados lineares que permite armazenar uma coleção de objetos. Os objetos podem ser acessados através de um índice, ou seja, a posição na lista.


## Criando uma lista

A lista é definida com os valores entre colchetes [ ] e separados por vírgula.

```python
# lista vazia
lista = []
print(lista)

# lista com elementos
lista = [1, 2, 3, 4]
print(lista)
```

## Tamanho da lista

A função `len` calcula o tamanho de uma lista.

```python
lista = [1, 2, 3, 4]
tamanho = len(lista)
print("Tamaho da lista:",tamanho)
```

## Obter um elemento pela posição


O acesso de uma posição em uma lista é feita com os []. A primeira posição da lista é o Zero.

```python
lista = [1, 2, 3, 4]
elemento = lista[2]
print("Elemento na posição 2:",elemento)
```

Acessar uma posição inválida na lista irá lançar uma exceção.

```python
lista = [1, 2, 3, 4]
# acesso a uma posição inválida
elemento = lista[20]
```

## Modificar o elemento na posição

```python
lista = [1, 2, 3, 4]
tamanho = len(lista)
print("Tamaho da lista:",tamanho)
```

## Percorrer a lista

## Adicionar elementos na lista

## Remover elementos na lista

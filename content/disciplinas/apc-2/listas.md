---
title: "Listas"
description: "Estrutura de dados utilizada para representar sequências de objetos em Python"
slug: listas
tags:
  - estruturas-de-dados
  - listas
  - python
  - list
---

Uma **lista** (`list`) é uma estrutura de dados utilizada para representar uma **sequência de objetos** em Python.

Em uma lista, a **ordem dos elementos importa** e um mesmo objeto pode aparecer **mais de uma vez**.

Por exemplo:

```python
frutas = ["maçã", "banana", "laranja", "banana"]
```

Nesse caso, `"banana"` aparece duas vezes e ocupa posições diferentes na sequência.

A ordem também faz parte da informação armazenada:

```python
lista1 = ["A", "B", "C"]
lista2 = ["C", "B", "A"]

print(lista1 == lista2)
```

Resultado:

```text
False
```

Embora as duas listas possuam os mesmos elementos, elas representam sequências diferentes porque a ordem não é a mesma.

## Estrutura

Uma lista em Python é representada por elementos separados por vírgulas e delimitados por colchetes `[]`.

```python
frutas = ["maçã", "banana", "laranja", "uva"]
```

Cada elemento ocupa uma posição, chamada de **índice**.

Os índices começam em `0`:

```text
Índice:    0         1          2        3
          ┌─────────┬──────────┬────────┬─────┐
Lista:    │  maçã   │ banana   │ laranja│ uva │
          └─────────┴──────────┴────────┴─────┘
```

Assim:

```python
print(frutas[0])  # maçã
print(frutas[1])  # banana
print(frutas[2])  # laranja
```

Python também permite utilizar índices negativos para acessar elementos a partir do final da lista:

```python
print(frutas[-1])  # uva
print(frutas[-2])  # laranja
```

## Criação de listas

Uma lista pode ser criada utilizando colchetes:

```python
numeros = [10, 20, 30, 40, 50]
```

Também é possível criar uma lista vazia:

```python
lista = []
```

Ou utilizando o construtor `list()`:

```python
lista = list()
```

Uma lista pode armazenar objetos de diferentes tipos:

```python
dados = [10, "Python", 3.14, True]
```

Também podemos criar listas contendo outras listas:

```python
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
```

## Acesso a elementos

O acesso aos elementos de uma lista é realizado utilizando o índice:

```python
frutas = ["maçã", "banana", "laranja"]

print(frutas[0])
print(frutas[1])
print(frutas[2])
```

Resultado:

```text
maçã
banana
laranja
```

Tentar acessar um índice que não existe gera uma exceção `IndexError`:

```python
print(frutas[5])
```

## Atualização de elementos

Os elementos de uma lista podem ser modificados diretamente utilizando seus índices.

```python
frutas = ["maçã", "banana", "laranja"]

frutas[1] = "abacaxi"

print(frutas)
```

Resultado:

```text
["maçã", "abacaxi", "laranja"]
```

A atualização modifica o objeto armazenado naquela posição, mas não altera a quantidade de elementos da lista.

## Adição de elementos

O método `append()` adiciona um elemento ao final da lista.

```python
frutas = ["maçã", "banana"]

frutas.append("laranja")

print(frutas)
```

Resultado:

```text
["maçã", "banana", "laranja"]
```

Também é possível adicionar vários elementos utilizando `extend()`:

```python
frutas = ["maçã", "banana"]

frutas.extend(["laranja", "uva"])

print(frutas)
```

Resultado:

```text
["maçã", "banana", "laranja", "uva"]
```

É importante perceber a diferença entre `append()` e `extend()`.

Com `append()`, a lista recebida é adicionada como **um único elemento**:

```python
lista = [1, 2]

lista.append([3, 4])

print(lista)
```

Resultado:

```text
[1, 2, [3, 4]]
```

Com `extend()`, os elementos da outra sequência são adicionados individualmente:

```python
lista = [1, 2]

lista.extend([3, 4])

print(lista)
```

Resultado:

```text
[1, 2, 3, 4]
```

## Inserção em uma posição específica

O método `insert()` permite adicionar um elemento em uma posição determinada.

```python
frutas = ["maçã", "banana", "laranja"]

frutas.insert(1, "uva")

print(frutas)
```

Resultado:

```text
["maçã", "uva", "banana", "laranja"]
```

O novo elemento passa a ocupar a posição indicada e os elementos seguintes são deslocados.

## Remoção de elementos

Python oferece diferentes formas de remover elementos de uma lista.

### Remover pelo valor

O método `remove()` remove a primeira ocorrência de determinado valor.

```python
frutas = ["maçã", "banana", "laranja", "banana"]

frutas.remove("banana")

print(frutas)
```

Resultado:

```text
["maçã", "laranja", "banana"]
```

Observe que apenas a primeira ocorrência de `"banana"` foi removida.

Caso o elemento não exista, `remove()` gera uma exceção `ValueError`.

### Remover pelo índice

O método `pop()` remove um elemento utilizando seu índice.

```python
frutas = ["maçã", "banana", "laranja"]

removida = frutas.pop(1)

print(removida)
print(frutas)
```

Resultado:

```text
banana
["maçã", "laranja"]
```

Se nenhum índice for informado, `pop()` remove o último elemento:

```python
frutas = ["maçã", "banana", "laranja"]

frutas.pop()

print(frutas)
```

Resultado:

```text
["maçã", "banana"]
```

### Remover utilizando `del`

Também é possível utilizar `del`:

```python
frutas = ["maçã", "banana", "laranja"]

del frutas[1]

print(frutas)
```

Resultado:

```text
["maçã", "laranja"]
```

## Tamanho da lista

A função `len()` retorna a quantidade de elementos existentes na lista.

```python
frutas = ["maçã", "banana", "laranja"]

print(len(frutas))
```

Resultado:

```text
3
```

É importante diferenciar o **tamanho da lista** do **maior índice**.

Em uma lista com três elementos:

```text
Índices:   0     1     2
Elementos: A     B     C
```

O tamanho é `3`, mas o último índice é `2`.

## Verificar se um elemento existe

O operador `in` permite verificar se determinado elemento está presente na lista.

```python
frutas = ["maçã", "banana", "laranja"]

print("banana" in frutas)
```

Resultado:

```text
True
```

Também é possível utilizar `not in`:

```python
print("uva" not in frutas)
```

Resultado:

```text
True
```

## Percorrer a lista

Uma das operações mais comuns é percorrer todos os elementos utilizando um laço `for`.

```python
frutas = ["maçã", "banana", "laranja"]

for fruta in frutas:
    print(fruta)
```

Resultado:

```text
maçã
banana
laranja
```

Também é possível percorrer a lista utilizando os índices:

```python
for i in range(len(frutas)):
    print(frutas[i])
```

Quando o índice não é necessário, utilizar diretamente o elemento costuma deixar o código mais simples.

## Slicing

Python possui uma funcionalidade chamada *slicing*, que permite obter uma parte da lista.

A sintaxe básica é:

```python
lista[inicio:fim]
```

Por exemplo:

```python
numeros = [10, 20, 30, 40, 50]

print(numeros[1:4])
```

Resultado:

```text
[20, 30, 40]
```

O índice inicial é incluído, mas o índice final não.

Também podemos utilizar:

```python
numeros[:3]    # primeiros três elementos
numeros[2:]    # a partir do índice 2
numeros[:]     # todos os elementos
```

É possível ainda utilizar um passo:

```python
numeros[::2]
```

Nesse caso, os elementos são obtidos de dois em dois.

## Ordenação

O método `sort()` permite ordenar os elementos da própria lista.

```python
numeros = [50, 10, 40, 20, 30]

numeros.sort()

print(numeros)
```

Resultado:

```text
[10, 20, 30, 40, 50]
```

Também é possível ordenar em ordem decrescente:

```python
numeros.sort(reverse=True)

print(numeros)
```

Resultado:

```text
[50, 40, 30, 20, 10]
```

Outra alternativa é utilizar a função `sorted()`, que retorna uma nova lista ordenada:

```python
numeros = [50, 10, 40, 20, 30]

ordenados = sorted(numeros)

print(ordenados)
```

Nesse caso, a lista original não é modificada.

## Contagem e localização

O método `count()` informa quantas vezes determinado elemento aparece na lista:

```python
numeros = [10, 20, 10, 30, 10]

print(numeros.count(10))
```

Resultado:

```text
3
```

Já o método `index()` retorna a posição da primeira ocorrência:

```python
frutas = ["maçã", "banana", "laranja"]

print(frutas.index("banana"))
```

Resultado:

```text
1
```

## Listas podem conter objetos repetidos

Uma característica importante de uma lista é permitir elementos repetidos.

```python
notas = [10, 8, 10, 7, 10]

print(notas)
```

Resultado:

```text
[10, 8, 10, 7, 10]
```

Cada ocorrência possui sua própria posição na sequência.

```python
print(notas[0])  # 10
print(notas[2])  # 10
print(notas[4])  # 10
```

Portanto, uma lista não deve ser confundida com uma estrutura que representa apenas um conjunto de valores distintos.

## Listas são sequências

A ideia de **sequência** é fundamental para compreender `list` em Python.

Uma sequência possui uma ordem definida:

```python
sequencia = ["A", "B", "C", "D"]
```

Podemos identificar cada elemento pela sua posição:

```text
A → posição 0
B → posição 1
C → posição 2
D → posição 3
```

A ordem faz parte da informação representada pela lista.

Por isso:

```python
["A", "B", "C"] != ["C", "B", "A"]
```

Além disso, uma sequência pode conter elementos repetidos:

```python
["A", "B", "A", "C", "A"]
```

Nesse caso, as três ocorrências de `"A"` fazem parte da sequência.

## Exemplo completo

O exemplo abaixo demonstra algumas das principais operações realizadas com uma lista em Python:

```python
frutas = ["maçã", "banana", "laranja"]

print("Lista inicial:")
print(frutas)

print("\nPrimeiro elemento:")
print(frutas[0])

frutas.append("uva")

print("\nApós adicionar:")
print(frutas)

frutas.insert(1, "abacaxi")

print("\nApós inserir:")
print(frutas)

removida = frutas.pop(2)

print("\nElemento removido:")
print(removida)

print("\nApós remoção:")
print(frutas)

frutas[0] = "morango"

print("\nApós atualização:")
print(frutas)

print("\nElementos:")
for fruta in frutas:
    print(fruta)
```

## Conclusão

A `list` é uma das principais estruturas de dados do Python e representa uma **sequência de objetos**.

Suas principais características são:

* Os elementos possuem uma ordem.
* Cada elemento possui uma posição.
* Os índices começam em `0`.
* Elementos podem ser repetidos.
* A lista pode ser modificada.
* Elementos podem ser adicionados e removidos.
* Uma lista pode armazenar diferentes tipos de objetos.
* Python fornece diversos métodos para sua manipulação.

Compreender `list` é fundamental para trabalhar com coleções de dados em Python e para avançar no estudo de estruturas de dados e algoritmos.

---

title: "Matrizes"
description: "Estrutura de dados utilizada para representar dados organizados em linhas e colunas utilizando listas de listas em Python"
slug: matrizes
tags:
  - estruturas-de-dados
  - matrizes
  - listas
  - python
  - list
---

Uma **matriz** é uma estrutura de dados utilizada para representar informações organizadas em **linhas e colunas**.

Em Python, uma matriz pode ser representada utilizando uma **lista de listas**.

Por exemplo:

```python
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
```

Nesse caso, temos uma matriz com **3 linhas e 3 colunas**.

Podemos visualizá-la da seguinte forma:

```text
        Colunas
          0   1   2
        ┌───┬───┬───┐
Linha 0 │ 1 │ 2 │ 3 │
        ├───┼───┼───┤
Linha 1 │ 4 │ 5 │ 6 │
        ├───┼───┼───┤
Linha 2 │ 7 │ 8 │ 9 │
        └───┴───┴───┘
```

Cada linha da matriz é representada por uma lista.

## Estrutura

Uma matriz é criada colocando listas dentro de outra lista:

```python
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
```

Podemos interpretar essa estrutura como:

```text
matriz
 ├── linha 0 → [1, 2, 3]
 ├── linha 1 → [4, 5, 6]
 └── linha 2 → [7, 8, 9]
```

A lista externa representa as **linhas**, enquanto cada lista interna representa os elementos daquela linha.

## Acesso aos elementos

Como uma matriz é uma lista de listas, precisamos utilizar dois índices para acessar um elemento.

O primeiro índice representa a **linha** e o segundo representa a **coluna**:

```python
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

print(matriz[0][0])
print(matriz[1][2])
print(matriz[2][1])
```

Resultado:

```text
1
6
8
```

Por exemplo:

```python
matriz[1][2]
```

pode ser interpretado como:

```text
matriz[linha][coluna]
matriz[1][2]
        ↓  ↓
      linha coluna
```

Portanto, `matriz[1][2]` representa o elemento localizado na **linha 1 e coluna 2**.

## Índices

Assim como acontece com listas, os índices começam em `0`.

Para a matriz:

```python
matriz = [
    [10, 20, 30],
    [40, 50, 60],
    [70, 80, 90]
]
```

Temos:

```text
             Coluna
              0    1    2
           ┌────┬────┬────┐
Linha 0    │ 10 │ 20 │ 30 │
           ├────┼────┼────┤
Linha 1    │ 40 │ 50 │ 60 │
           ├────┼────┼────┤
Linha 2    │ 70 │ 80 │ 90 │
           └────┴────┴────┘
```

Assim:

```python
print(matriz[0][1])  # 20
print(matriz[1][0])  # 40
print(matriz[2][2])  # 90
```

## Atualização de elementos

Os elementos de uma matriz podem ser modificados utilizando seus índices.

```python
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

matriz[1][1] = 50

print(matriz)
```

Resultado:

```text
[[1, 2, 3], [4, 50, 6], [7, 8, 9]]
```

Nesse caso, o elemento localizado na linha `1` e coluna `1` foi alterado.

## Quantidade de linhas

Como a matriz é uma lista, podemos utilizar `len()` para descobrir a quantidade de linhas:

```python
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

print(len(matriz))
```

Resultado:

```text
3
```

Nesse caso, a matriz possui três linhas.

## Quantidade de colunas

Para descobrir a quantidade de elementos de uma linha, também utilizamos `len()`:

```python
print(len(matriz[0]))
```

Resultado:

```text
3
```

Portanto, essa matriz possui:

```text
3 linhas
3 colunas
```

Podemos obter essas informações:

```python
linhas = len(matriz)
colunas = len(matriz[0])

print("Linhas:", linhas)
print("Colunas:", colunas)
```

## Percorrer uma matriz

Como uma matriz é formada por listas dentro de uma lista, podemos utilizar dois laços `for` para percorrer todos os seus elementos.

```python
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

for linha in matriz:
    for elemento in linha:
        print(elemento)
```

Resultado:

```text
1
2
3
4
5
6
7
8
9
```

O primeiro `for` percorre as linhas:

```python
for linha in matriz:
```

O segundo `for` percorre os elementos de cada linha:

```python
for elemento in linha:
```

## Exibir uma matriz

Podemos utilizar um `for` para exibir cada linha da matriz:

```python
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

for linha in matriz:
    print(linha)
```

Resultado:

```text
[1, 2, 3]
[4, 5, 6]
[7, 8, 9]
```

Se quisermos exibir apenas os valores, podemos utilizar dois laços:

```python
for linha in matriz:
    for elemento in linha:
        print(elemento, end=" ")
    print()
```

Resultado:

```text
1 2 3
4 5 6
7 8 9
```

## Percorrer utilizando índices

Também podemos percorrer uma matriz utilizando seus índices:

```python
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

for i in range(len(matriz)):
    for j in range(len(matriz[i])):
        print(matriz[i][j])
```

Nesse exemplo:

```text
i → índice da linha
j → índice da coluna
```

O acesso ao elemento é realizado por:

```python
matriz[i][j]
```

Quando não precisamos dos índices, percorrer diretamente as linhas e os elementos costuma deixar o código mais simples.

## Adicionar uma linha

Como cada linha é uma lista, podemos utilizar `append()` para adicionar uma nova linha:

```python
matriz = [
    [1, 2, 3],
    [4, 5, 6]
]

matriz.append([7, 8, 9])

print(matriz)
```

Resultado:

```text
[[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```

A nova lista foi adicionada como uma nova linha da matriz.

## Adicionar um elemento a uma linha

Também podemos adicionar um elemento diretamente em uma linha:

```python
matriz = [
    [1, 2],
    [3, 4]
]

matriz[0].append(5)

print(matriz)
```

Resultado:

```text
[[1, 2, 5], [3, 4]]
```

Nesse caso, o `5` foi adicionado apenas à primeira linha.

É importante perceber que listas de listas **não precisam necessariamente ter o mesmo tamanho**:

```python
matriz = [
    [1, 2, 3],
    [4, 5],
    [6, 7, 8, 9]
]
```

Essa estrutura continua sendo uma lista de listas, mas possui linhas com quantidades diferentes de elementos.

## Remover uma linha

Podemos utilizar `pop()` para remover uma linha:

```python
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

matriz.pop(1)

print(matriz)
```

Resultado:

```text
[[1, 2, 3], [7, 8, 9]]
```

A linha de índice `1` foi removida.

## Remover um elemento

Também podemos remover um elemento de uma determinada linha:

```python
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

matriz[1].pop(1)

print(matriz)
```

Resultado:

```text
[[1, 2, 3], [4, 6], [7, 8, 9]]
```

Nesse caso, o elemento da linha `1` e coluna `1` foi removido.

## Exemplo com notas

Matrizes podem ser utilizadas para representar dados organizados em linhas e colunas.

Por exemplo, podemos representar as notas de estudantes:

```python
notas = [
    [8, 7, 9],
    [6, 8, 7],
    [10, 9, 8]
]
```

Podemos interpretar:

```text
             Prova 1  Prova 2  Prova 3
Aluno 1         8        7        9
Aluno 2         6        8        7
Aluno 3        10        9        8
```

Para acessar a nota do segundo aluno na terceira prova:

```python
print(notas[1][2])
```

Resultado:

```text
7
```

## Exemplo completo

O exemplo abaixo demonstra algumas das principais operações realizadas com uma matriz:

```python
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

print("Matriz:")
for linha in matriz:
    print(linha)

print("\nElemento da linha 1, coluna 2:")
print(matriz[1][2])

matriz[0][0] = 10

print("\nApós atualização:")
for linha in matriz:
    print(linha)

matriz.append([11, 12, 13])

print("\nApós adicionar uma linha:")
for linha in matriz:
    print(linha)

matriz[1].pop(1)

print("\nApós remover um elemento:")
for linha in matriz:
    print(linha)
```

## Conclusão

Em Python, uma matriz pode ser representada utilizando uma **lista de listas**.

Sua estrutura pode ser compreendida como:

```text
lista externa
     ↓
  ┌───────────────┐
  │ lista → linha │
  │ lista → linha │
  │ lista → linha │
  └───────────────┘
```

As principais características são:

* Cada linha é representada por uma lista.
* A matriz é representada por uma lista contendo essas listas.
* O primeiro índice representa a linha.
* O segundo índice representa a coluna.
* Os índices começam em `0`.
* Os elementos podem ser atualizados.
* Linhas e elementos podem ser adicionados ou removidos.
* Podemos percorrer a matriz utilizando laços `for`.
* As linhas podem possuir tamanhos diferentes, embora matrizes tradicionais normalmente utilizem linhas com a mesma quantidade de elementos.

Compreender **listas de listas** é fundamental para trabalhar com matrizes em Python e para representar dados organizados em linhas e colunas.

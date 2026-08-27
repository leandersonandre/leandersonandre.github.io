---

title: "Fila"
description: "Estrutura de dados linear baseada no princípio FIFO para armazenar e processar elementos em ordem de chegada"
slug: fila
tags:
  - estruturas-de-dados
  - fila
  - queue
  - python
---

Uma **fila** (*queue*) é uma estrutura de dados linear que organiza os elementos de acordo com o princípio **FIFO — First In, First Out**, ou seja, **o primeiro elemento inserido é o primeiro a ser removido**.

Um exemplo do cotidiano é uma fila de pessoas esperando para serem atendidas.

```text
Entrada
   ↓

┌─────────┬─────────┬─────────┐
│   Ana   │  Bruno  │  Carlos │
└─────────┴─────────┴─────────┘
    ↑                         ↑
  primeiro                 último
   a sair                  a entrar
```

Se uma nova pessoa entrar na fila, ela será adicionada ao final.

Quando uma pessoa for atendida, será removida a primeira pessoa da fila.

```text
Entrada: A → B → C

Saída:   A → B → C
```

Essa característica define o comportamento de uma fila:

> **O primeiro elemento que entra é o primeiro elemento que sai.**

## Utilizando uma `list`

Em Python, podemos utilizar uma `list` para representar uma fila.

```python
fila = []
```

Nesse momento, a fila está vazia.

Podemos visualizar a fila como uma sequência em que:

```text
início → [ A | B | C ] ← final
           ↑       ↑
         saída   entrada
```

O primeiro elemento representa o próximo elemento que será removido, enquanto novos elementos são adicionados ao final.

## Enqueue — adicionar elementos

Para adicionar um elemento ao final da fila, utilizamos `append()`.

```python
fila = []

fila.append("A")
fila.append("B")
fila.append("C")

print(fila)
```

Resultado:

```text
["A", "B", "C"]
```

Os elementos entram na ordem:

```text
A → B → C
```

O elemento `"A"` é o primeiro da fila e `"C"` é o último.

Podemos adicionar outro elemento:

```python
fila.append("D")

print(fila)
```

Resultado:

```text
["A", "B", "C", "D"]
```

O novo elemento é sempre colocado no final.

## Dequeue — remover elementos

Para remover o primeiro elemento da fila, utilizamos `pop(0)`.

```python
fila = ["A", "B", "C"]

elemento = fila.pop(0)

print(elemento)
print(fila)
```

Resultado:

```text
A
["B", "C"]
```

O elemento `"A"` foi o primeiro a entrar e, portanto, foi o primeiro a sair.

Podemos continuar removendo:

```python
fila.pop(0)
```

Remove `"B"`.

Depois:

```python
fila.pop(0)
```

Remove `"C"`.

A sequência de remoção será:

```text
Entrada: A → B → C

Saída:   A → B → C
```

## Front — consultar o primeiro elemento

Para consultar o primeiro elemento sem removê-lo, podemos utilizar o índice `0`.

```python
fila = ["A", "B", "C"]

print(fila[0])
```

Resultado:

```text
A
```

O elemento continua na fila:

```python
print(fila)
```

Resultado:

```text
["A", "B", "C"]
```

## Verificar se a fila está vazia

Podemos verificar se uma fila possui elementos utilizando uma estrutura condicional.

```python
fila = []

if not fila:
    print("A fila está vazia.")
```

Resultado:

```text
A fila está vazia.
```

Quando a fila possui elementos:

```python
fila = ["A", "B"]

if fila:
    print("A fila possui elementos.")
```

Resultado:

```text
A fila possui elementos.
```

## Exemplo completo

O exemplo abaixo demonstra as principais operações de uma fila utilizando `list`:

```python
fila = []

# Enqueue
fila.append("A")
fila.append("B")
fila.append("C")

print("Fila:")
print(fila)

# Front
print("\nPrimeiro elemento:")
print(fila[0])

# Dequeue
elemento = fila.pop(0)

print("\nElemento removido:")
print(elemento)

print("\nFila após remoção:")
print(fila)

# Verificar se está vazia
if not fila:
    print("\nA fila está vazia.")
else:
    print("\nA fila possui elementos.")
```

Resultado:

```text
Fila:
["A", "B", "C"]

Primeiro elemento:
A

Elemento removido:
A

Fila após remoção:
["B", "C"]

A fila possui elementos.
```

## Resumo

Uma fila segue o princípio **FIFO — First In, First Out**.

As principais operações são:

```text
Enqueue  → adiciona no final
Dequeue  → remove do início
Front    → consulta o primeiro
```

Utilizando uma `list` em Python:

```python
fila = []

fila.append(valor)  # Enqueue
fila.pop(0)         # Dequeue
fila[0]             # Front
```

A ideia fundamental é simples:

> **Em uma fila, o primeiro elemento que entra é o primeiro elemento que sai.**

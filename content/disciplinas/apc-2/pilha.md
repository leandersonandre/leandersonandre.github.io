---
title: "Pilha"
description: "Estrutura de dados linear baseada no princípio LIFO para armazenar e manipular elementos"
slug: pilha
tags:
  - estruturas-de-dados
  - pilha
  - stack
  - python
---

Uma **pilha** (*stack*) é uma estrutura de dados linear que organiza os elementos de acordo com o princípio **LIFO — Last In, First Out**, ou seja, **o último elemento inserido é o primeiro a ser removido**.

Um exemplo do cotidiano é uma pilha de pratos:

```text
        ┌─────────┐
        │  Prato  │ ← último a entrar
        ├─────────┤
        │  Prato  │
        ├─────────┤
        │  Prato  │ ← primeiro a entrar
        └─────────┘
             ↑
          topo
```

Se colocarmos um novo prato na pilha, ele ficará no topo.

Quando retirarmos um prato, será retirado primeiro aquele que está no topo.

```text
Entrada:  A → B → C

Saída:    C → B → A
```

Essa característica define o comportamento de uma pilha: **o elemento que entrou por último é o primeiro a sair**.

## Operações de uma pilha

As operações fundamentais de uma pilha são:

* **Push** — adiciona um elemento ao topo.
* **Pop** — remove o elemento do topo.
* **Peek/Top** — consulta o elemento do topo sem removê-lo.
* **isEmpty** — verifica se a pilha está vazia.

Em Python, uma `list` pode ser utilizada para representar uma pilha.

## Criando uma pilha

Podemos criar uma pilha utilizando uma lista vazia:

```python
pilha = []
```

Nesse momento, a pilha não possui nenhum elemento.

```text
Pilha:

┌─────────┐
│         │
└─────────┘
```

## Push — adicionar elementos

Para adicionar um elemento ao topo da pilha, podemos utilizar `append()`.

```python
pilha = []

pilha.append("A")
pilha.append("B")
pilha.append("C")

print(pilha)
```

Resultado:

```text
["A", "B", "C"]
```

O elemento `"C"` está no topo da pilha:

```text
┌─────────┐
│    C    │ ← topo
├─────────┤
│    B    │
├─────────┤
│    A    │
└─────────┘
```

Cada chamada de `append()` adiciona um novo elemento ao topo.

## Pop — remover elementos

Para remover o elemento do topo, utilizamos `pop()`.

```python
pilha = ["A", "B", "C"]

elemento = pilha.pop()

print(elemento)
print(pilha)
```

Resultado:

```text
C
["A", "B"]
```

O elemento `"C"` foi o último a entrar e, portanto, foi o primeiro a sair.

Podemos continuar removendo:

```python
pilha.pop()
```

Remove `"B"`.

Depois:

```python
pilha.pop()
```

Remove `"A"`.

A sequência de remoção será:

```text
Entrada: A → B → C

Saída:   C → B → A
```

## Peek — consultar o topo

Para consultar o elemento que está no topo sem removê-lo, podemos acessar o último elemento da lista utilizando o índice `-1`.

```python
pilha = ["A", "B", "C"]

print(pilha[-1])
```

Resultado:

```text
C
```

O elemento continua na pilha:

```python
print(pilha)
```

Resultado:

```text
["A", "B", "C"]
```

## Verificar se a pilha está vazia

Podemos verificar se uma pilha possui elementos utilizando uma estrutura condicional.

```python
pilha = []

if not pilha:
    print("A pilha está vazia.")
```

Resultado:

```text
A pilha está vazia.
```

Quando a pilha possui elementos:

```python
pilha = ["A", "B"]

if pilha:
    print("A pilha possui elementos.")
```

Resultado:

```text
A pilha possui elementos.
```

## Exemplo completo

O exemplo abaixo demonstra as principais operações de uma pilha:

```python
pilha = []

# Push
pilha.append("A")
pilha.append("B")
pilha.append("C")

print("Pilha:")
print(pilha)

# Peek
print("\nTopo:")
print(pilha[-1])

# Pop
elemento = pilha.pop()

print("\nElemento removido:")
print(elemento)

print("\nPilha após remoção:")
print(pilha)

# Verificar se está vazia
if not pilha:
    print("\nA pilha está vazia.")
else:
    print("\nA pilha possui elementos.")
```

Resultado:

```text
Pilha:
["A", "B", "C"]

Topo:
C

Elemento removido:
C

Pilha após remoção:
["A", "B"]

A pilha possui elementos.
```

## Resumo

Uma pilha segue o princípio **LIFO — Last In, First Out**.

As principais operações são:

```text
Push  → adiciona no topo
Pop   → remove do topo
Peek  → consulta o topo
```

Em Python, podemos utilizar uma `list` de maneira simples para representar uma pilha:

```python
pilha = []

pilha.append(valor)  # Push
pilha.pop()          # Pop
pilha[-1]            # Peek
```

A ideia fundamental é simples:

> **Em uma pilha, o último elemento que entra é o primeiro elemento que sai.**

---
title: "Operadores Relacionais e Lógicos"
slug: operadores-relacionais-logicos
description: "Operadores Relacionais e Lógicos em Python"
tags:
- python
- operadores relacionais
- operadores lógicos
---


Os operadores relacionais e lógicos são utilizados para construir condições em estruturas de decisão e repetição. Eles permitem comparar valores e combinar múltiplas condições.

## Operadores relacionais

Os operadores relacionais comparam valores e retornam um resultado do tipo booleano (`True` ou `False`).

| Operador | Descrição           | Exemplo     | Resultado |
|----------|--------------------|-------------|-----------|
| `==`     | Igual              | `5 == 5`    | `True`    |
| `!=`     | Diferente          | `5 != 3`    | `True`    |
| `>`      | Maior              | `5 > 3`     | `True`    |
| `<`      | Menor              | `3 < 5`     | `True`    |
| `>=`     | Maior ou igual     | `5 >= 5`    | `True`    |
| `<=`     | Menor ou igual     | `3 <= 5`    | `True`    |

```python
x = 10
y = 5

print(x > y)
print(x == y)
```

---

## Operadores lógicos

Os operadores lógicos permitem combinar múltiplas condições.

| Operador | Descrição | Exemplo                     | Resultado |
|----------|----------|------------------------------|-----------|
| `and`    | E lógico | `True and False`             | `False`   |
| `or`     | Ou lógico| `True or False`              | `True`    |
| `not`    | Negação  | `not True`                   | `False`   |

```python
idade = 20
tem_carteira = True

if idade >= 18 and tem_carteira:
    print("Pode dirigir")
```

---

## Precedência dos operadores lógicos

A ordem de avaliação é:

1. `not`  
2. `and`  
3. `or`  

Parênteses podem ser utilizados para deixar a expressão mais clara.

```python
resultado = not (True and False)
```

---

## Observação

Os operadores relacionais são usados para comparar valores, enquanto os operadores lógicos são usados para combinar condições. Ambos são fundamentais para controlar o fluxo de execução de programas.

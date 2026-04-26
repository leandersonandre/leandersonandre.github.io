---
title: "Operadores Aritméticos e Funções Matemáticas"
description: "Operadores Aritméticos e Funções Matemáticas em Python"
tags:
- python
- operadores aritméticos
- math
---

Em Python, os operadores aritméticos permitem realizar cálculos básicos. Além disso, a biblioteca padrão oferece funções matemáticas mais avançadas por meio do módulo `math`.

## Operadores aritméticos

Os principais operadores aritméticos são:

| Operador | Descrição                  | Exemplo     | Resultado  |
|----------|----------------------------|-------------|------------|
| `+`      | Adição                     | `2 + 3`     | `5`        |
| `-`      | Subtração                  | `5 - 2`     | `3`        |
| `*`      | Multiplicação              | `4 * 3`     | `12`       |
| `/`      | Divisão                    | `10 / 3`    | `3.333...` |
| `//`     | Divisão inteira            | `10 // 3`   | `3`        |
| `%`      | Resto da divisão (módulo)  | `10 % 3`    | `1`        |
| `**`     | Exponenciação              | `2 ** 3`    | `8`        |

```python
a = 10
b = 3

print(a + b)   # 13
print(a - b)   # 7
print(a * b)   # 30
print(a / b)   # 3.333...
print(a // b)  # 3
print(a % b)   # 1
print(a ** b)  # 1000
```



## Ordem de precedência

Os operadores seguem uma ordem de execução:

1. `**` (exponenciação)  
2. `*`, `/`, `//`, `%`  
3. `+`, `-`  

Parênteses podem ser utilizados para alterar a ordem.

```python
resultado = 2 + 3 * 4      # 14
resultado = (2 + 3) * 4    # 20
```



## Módulo math

O módulo `math` fornece funções matemáticas mais avançadas. Para utilizá-lo, é necessário importá-lo.

```python
import math
```



## Funções básicas

```python
import math

print(math.sqrt(9))    # raiz quadrada
print(math.pow(2, 3))  # potência
print(math.ceil(2.3))  # arredonda para cima
print(math.floor(2.7)) # arredonda para baixo
```



## Constantes

```python
import math

print(math.pi)  # valor de π
print(math.e)   # número de Euler
```



## Valor absoluto

```python
print(abs(-10))  # 10
```



## Máximo e mínimo

```python
print(max(3, 7, 2))
print(min(3, 7, 2))
```


## Observação

Os operadores aritméticos são utilizados para cálculos básicos, enquanto o módulo `math` oferece funções mais completas para aplicações científicas e matemáticas.

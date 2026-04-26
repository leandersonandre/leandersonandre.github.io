---
title: "Formatação de Números"
slug: formatacao-de-numeros
description: "Formatação de números em Python"
tags:
- python
- format
- round
---


Em Python, é possível controlar como números são exibidos utilizando formatação. Isso é útil para limitar casas decimais, alinhar valores e melhorar a leitura dos dados.

## Formatação com f-string

A forma mais comum e moderna de formatar números é utilizando **f-strings**.

```python
valor = 3.14159
print(f"{valor:.2f}")
```

Neste caso:
- `.2f` indica que o número será exibido com **2 casas decimais**

Saída:
```
3.14
```


## Casas decimais

```python
valor = 10

print(f"{valor:.2f}")
```

Saída:
```
10.00
```


## Largura e alinhamento

É possível definir a largura do campo e o alinhamento.

```python
valor = 42

print(f"{valor:5}")   # largura 5
print(f"{valor:>5}")  # alinhado à direita
print(f"{valor:<5}")  # alinhado à esquerda
print(f"{valor:^5}")  # centralizado
```


## Preenchimento com zeros

```python
numero = 7
print(f"{numero:03}")
```

Saída:
```
007
```


## Separador de milhar

```python
valor = 1000000
print(f"{valor:,}")
```

Saída:
```
1,000,000
```


## Formatação percentual

```python
taxa = 0.85
print(f"{taxa:.2%}")
```

Saída:
```
85.00%
```


## Arredondamento

A função `round()` pode ser utilizada para arredondar números.

```python
valor = 3.14159
print(round(valor, 2))
```

Saída:
```
3.14
```


## Observação

A formatação de números melhora a apresentação dos dados e é muito utilizada em relatórios, interfaces e exibição de resultados.

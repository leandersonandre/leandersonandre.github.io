---
title: "Teste de Mesa"
slug: "teste-de-mesa"
description: "Simulação passo a passo de algoritmos"
tags:
- algoritmos
- lógica
- teste-de-mesa
---

O **teste de mesa** é uma técnica utilizada para simular a execução de um algoritmo manualmente. Ele permite acompanhar, passo a passo, os valores das variáveis e entender como o algoritmo se comporta.

Essa técnica é muito útil para:

- Identificar erros lógicos
- Entender o fluxo de execução
- Validar algoritmos antes de executar no computador


## Tabela de acompanhamento

Para realizar o teste de mesa, normalmente utilizamos uma tabela para registrar cada passo da execução.

| Passo | Instrução | Saída | Variáveis |
|------|----------|------|----------|
| 1 |  |  |  |
| 2 |  |  |  |
| ... |  |  |  |

Essa tabela ajuda a visualizar como os valores das variáveis mudam ao longo do tempo.


## Exemplo 1

```python
x = 10
y = 8
z = 5 * 2 + y
x = x - 1
y = z - x
z = y + x - 4
print(x)
print(y)
print(z)
````

## Teste de mesa

| Passo | Instrução     | Saída | x  | y | z  |
| ----- | ------------- | ----- | -- | - | -- |
| 1     | x = 10        |       | 10 |   |    |
| 2     | y = 8         |       | 10 | 8 |    |
| 3     | z = 5*2 + y   |       | 10 | 8 | 18 |
| 4     | x = x - 1     |       | 9  | 8 | 18 |
| 5     | y = z - x     |       | 9  | 9 | 18 |
| 6     | z = y + x - 4 |       | 9  | 9 | 14 |
| 7     | print(x)      | 9     | 9  | 9 | 14 |
| 8     | print(y)      | 9     | 9  | 9 | 14 |
| 9     | print(z)      | 14    | 9  | 9 | 14 |

Ao final da execução, os valores impressos serão:

* x = 9
* y = 9
* z = 14

## Exemplo com decisão

```python
idade = int(input("Digite a sua idade"))

if idade < 18:
    print("Você não pode dirigir um carro")

if idade > 17:
    print("Você pode dirigir um carro")
```

## Teste de mesa (idade = 18)

| Passo | Instrução  | Saída                      | idade |
| ----- | ---------- | -------------------------- | ----- |
| 1     | input      | Digite a sua idade         | 18    |
| 2     | idade < 18 | false                      | 18    |
| 3     | idade > 17 | true                       | 18    |
| 4     | print      | Você pode dirigir um carro | 18    |

## Teste de mesa (idade = 14)

| Passo | Instrução  | Saída                          | idade |
| ----- | ---------- | ------------------------------ | ----- |
| 1     | input      | Digite a sua idade             | 14    |
| 2     | idade < 18 | true                           | 14    |
| 3     | print      | Você não pode dirigir um carro | 14    |
| 4     | idade > 17 | false                          | 14    |

Note que os dois `if` são independentes, ou seja, ambos podem ser avaliados.

## Exemplo 3

Programa que determina o maior valor entre três números:

```python
A = int(input("Digite o primeiro número"))
B = int(input("Digite o segundo número"))
C = int(input("Digite o terceiro número"))

maior = (A + B + abs(A - B)) / 2
maior = (maior + C + abs(maior - C)) / 2
maior = int(maior)

print(maior, "eh o maior")
```

## Teste de mesa (A = 3, B = 1, C = 2)

| Passo | Instrução | Saída        | A | B | C | maior |
| ----- | --------- | ------------ | - | - | - | ----- |
| 1     | input     | Digite A     | 3 |   |   |       |
| 2     | input     | Digite B     | 3 | 1 |   |       |
| 3     | input     | Digite C     | 3 | 1 | 2 |       |
| 4     | cálculo   |              | 3 | 1 | 2 | 3.0   |
| 5     | cálculo   |              | 3 | 1 | 2 | 3.0   |
| 6     | int       |              | 3 | 1 | 2 | 3     |
| 7     | print     | 3 eh o maior | 3 | 1 | 2 | 3     |

## Observação

O teste de mesa deve ser feito com atenção à ordem de execução das instruções.

Cada linha do algoritmo deve ser analisada sequencialmente, atualizando os valores das variáveis conforme necessário.

Essa prática é essencial para desenvolver uma boa lógica de programação.

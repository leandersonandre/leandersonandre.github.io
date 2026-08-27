---
title: "Questões sobre Matrizes"
description: "Questões sobre matrizes utilizando listas de listas em Python"
slug: matrizes-questoes
tags:
- python
- matrizes
- listas
- questões
---

{{< lista-questoes >}}

{{< questao >}}
Em Python, como uma matriz pode ser representada utilizando listas?

{{< alternativa >}} Como uma lista de listas. {{< /alternativa >}}
{{< alternativa >}} Como uma única string. {{< /alternativa >}}
{{< alternativa >}} Como um conjunto de valores sem organização. {{< /alternativa >}}
{{< alternativa >}} Como uma tupla obrigatoriamente. {{< /alternativa >}}
{{< solucao letra="A" >}}
Uma matriz pode ser representada em Python utilizando uma lista contendo outras listas. Cada lista interna pode representar uma linha da matriz.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere a matriz abaixo:

{{< code >}}
matriz = [
    [1, 2, 3],
    [4, 5, 6]
]
{{< /code >}}

Quantas linhas essa matriz possui?

{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 6 {{< /alternativa >}}
{{< solucao letra="B" >}}
A matriz possui duas listas internas, portanto possui duas linhas.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere a matriz abaixo:

{{< code >}}
matriz = [
    [1, 2, 3],
    [4, 5, 6]
]
{{< /code >}}

Quantas colunas essa matriz possui?

{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 6 {{< /alternativa >}}
{{< solucao letra="B" >}}
Cada linha possui três elementos. Portanto, a matriz possui três colunas.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere a matriz abaixo:

{{< code >}}
matriz = [
    [10, 20, 30],
    [40, 50, 60]
]
{{< /code >}}

Qual valor está na primeira linha e segunda coluna?

{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 40 {{< /alternativa >}}
{{< alternativa >}} 50 {{< /alternativa >}}
{{< solucao letra="B" >}}
A primeira linha possui índice 0 e a segunda coluna possui índice 1. Portanto, `matriz[0][1]` corresponde ao valor 20.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere a matriz abaixo:

{{< code >}}
matriz = [
    [10, 20, 30],
    [40, 50, 60]
]
{{< /code >}}

Qual expressão acessa o valor `50`?

{{< alternativa >}} `matriz[0][1]` {{< /alternativa >}}
{{< alternativa >}} `matriz[0][2]` {{< /alternativa >}}
{{< alternativa >}} `matriz[1][1]` {{< /alternativa >}}
{{< alternativa >}} `matriz[2][1]` {{< /alternativa >}}
{{< solucao letra="C" >}}
O valor 50 está na segunda linha e segunda coluna. Como os índices começam em 0, seu acesso é feito com `matriz[1][1]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
matriz = [
    [1, 2],
    [3, 4]
]

print(matriz[0][0])
{{< /code >}}

{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< solucao letra="A" >}}
`matriz[0][0]` acessa a primeira linha e a primeira coluna. O valor é 1.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
matriz = [
    [1, 2],
    [3, 4]
]

print(matriz[1][0])
{{< /code >}}

{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< solucao letra="C" >}}
`matriz[1][0]` acessa a segunda linha e a primeira coluna. O valor é 3.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
matriz = [
    [1, 2, 3],
    [4, 5, 6]
]

print(matriz[1][2])
{{< /code >}}

{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 6 {{< /alternativa >}}
{{< solucao letra="D" >}}
`matriz[1][2]` acessa a segunda linha e a terceira coluna. O valor é 6.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
matriz = [
    [1, 2],
    [3, 4]
]

print(len(matriz))
{{< /code >}}

{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< solucao letra="B" >}}
`len(matriz)` retorna a quantidade de elementos da lista externa. Como ela possui duas listas internas, o resultado é 2.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere a matriz abaixo:

{{< code >}}
matriz = [
    [1, 2, 3],
    [4, 5, 6]
]
{{< /code >}}

Qual expressão pode ser utilizada para descobrir a quantidade de colunas?

{{< alternativa >}} `len(matriz)` {{< /alternativa >}}
{{< alternativa >}} `len(matriz[0])` {{< /alternativa >}}
{{< alternativa >}} `len(matriz[0][0])` {{< /alternativa >}}
{{< alternativa >}} `len(matriz[1][0])` {{< /alternativa >}}
{{< solucao letra="B" >}}
`matriz[0]` representa a primeira linha. Como ela possui três elementos, `len(matriz[0])` retorna a quantidade de colunas.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
matriz = [
    [1, 2, 3],
    [4, 5, 6]
]

print(matriz[0])
{{< /code >}}

{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} [1, 2, 3] {{< /alternativa >}}
{{< alternativa >}} [4, 5, 6] {{< /alternativa >}}
{{< alternativa >}} 6 {{< /alternativa >}}
{{< solucao letra="B" >}}
`matriz[0]` acessa a primeira linha inteira da matriz, que é `[1, 2, 3]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
matriz = [
    [1, 2, 3],
    [4, 5, 6]
]

print(matriz[1])
{{< /code >}}

{{< alternativa >}} [1, 2, 3] {{< /alternativa >}}
{{< alternativa >}} [4, 5, 6] {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< alternativa >}} 6 {{< /alternativa >}}
{{< solucao letra="B" >}}
`matriz[1]` acessa a segunda linha inteira da matriz, que é `[4, 5, 6]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
matriz = [
    [1, 2],
    [3, 4]
]

for linha in matriz:
    print(linha)
{{< /code >}}

{{< alternativa >}} 1 e 2 {{< /alternativa >}}
{{< alternativa >}} [1, 2] e [3, 4] {{< /alternativa >}}
{{< alternativa >}} 1, 2, 3 e 4 em uma única linha {{< /alternativa >}}
{{< alternativa >}} Apenas [1, 2] {{< /alternativa >}}
{{< solucao letra="B" >}}
A variável `linha` recebe cada lista interna da matriz. Portanto, serão impressas as duas linhas: `[1, 2]` e `[3, 4]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
matriz = [
    [1, 2],
    [3, 4]
]

for linha in matriz:
    for valor in linha:
        print(valor)
{{< /code >}}

{{< alternativa >}} 1, 2, 3, 4 {{< /alternativa >}}
{{< alternativa >}} 1, 3, 2, 4 {{< /alternativa >}}
{{< alternativa >}} 4, 3, 2, 1 {{< /alternativa >}}
{{< alternativa >}} [1, 2] e [3, 4] {{< /alternativa >}}
{{< solucao letra="A" >}}
O primeiro `for` percorre as linhas e o segundo percorre os elementos de cada linha. Assim, os valores são impressos na ordem 1, 2, 3 e 4.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual estrutura de repetição é normalmente utilizada para percorrer todos os elementos de uma matriz representada por listas de listas?

{{< alternativa >}} Um único `if`. {{< /alternativa >}}
{{< alternativa >}} Dois `for` aninhados. {{< /alternativa >}}
{{< alternativa >}} Apenas um `while` sem condição. {{< /alternativa >}}
{{< alternativa >}} Um `print()` para cada elemento. {{< /alternativa >}}
{{< solucao letra="B" >}}
É comum utilizar dois `for` aninhados: o primeiro percorre as linhas e o segundo percorre os elementos de cada linha.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
matriz = [
    [1, 2, 3],
    [4, 5, 6]
]

soma = 0

for linha in matriz:
    for valor in linha:
        soma += valor

print(soma)
{{< /code >}}

{{< alternativa >}} 6 {{< /alternativa >}}
{{< alternativa >}} 15 {{< /alternativa >}}
{{< alternativa >}} 21 {{< /alternativa >}}
{{< alternativa >}} 12 {{< /alternativa >}}
{{< solucao letra="C" >}}
A soma dos elementos é `1 + 2 + 3 + 4 + 5 + 6`, que resulta em 21.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
matriz = [
    [1, 2, 3],
    [4, 5, 6]
]

soma = 0

for valor in matriz[0]:
    soma += valor

print(soma)
{{< /code >}}

{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 6 {{< /alternativa >}}
{{< alternativa >}} 15 {{< /alternativa >}}
{{< alternativa >}} 21 {{< /alternativa >}}
{{< solucao letra="B" >}}
`matriz[0]` representa a primeira linha. A soma dos seus elementos é `1 + 2 + 3`, resultando em 6.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere a matriz abaixo:

{{< code >}}
matriz = [
    [1, 2],
    [3, 4]
]
{{< /code >}}

Qual comando altera o valor 4 para 10?

{{< alternativa >}} `matriz[0][0] = 10` {{< /alternativa >}}
{{< alternativa >}} `matriz[0][1] = 10` {{< /alternativa >}}
{{< alternativa >}} `matriz[1][0] = 10` {{< /alternativa >}}
{{< alternativa >}} `matriz[1][1] = 10` {{< /alternativa >}}
{{< solucao letra="D" >}}
O valor 4 está na segunda linha e segunda coluna, portanto seu acesso é `matriz[1][1]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o conteúdo final da matriz.

{{< code >}}
matriz = [
    [1, 2],
    [3, 4]
]

matriz[0][1] = 10

print(matriz)
{{< /code >}}

{{< alternativa >}} [[1, 2], [3, 4]] {{< /alternativa >}}
{{< alternativa >}} [[10, 2], [3, 4]] {{< /alternativa >}}
{{< alternativa >}} [[1, 10], [3, 4]] {{< /alternativa >}}
{{< alternativa >}} [[1, 2], [10, 4]] {{< /alternativa >}}
{{< solucao letra="C" >}}
`matriz[0][1]` representa a primeira linha e a segunda coluna. Portanto, o valor 2 é alterado para 10.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere a matriz abaixo:

{{< code >}}
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
{{< /code >}}

Qual é o valor que está na segunda linha e terceira coluna?

{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 6 {{< /alternativa >}}
{{< alternativa >}} 8 {{< /alternativa >}}
{{< solucao letra="C" >}}
A segunda linha possui índice 1 e a terceira coluna possui índice 2. Portanto, `matriz[1][2]` é 6.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere a matriz abaixo:

{{< code >}}
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]
{{< /code >}}

Qual é o valor da diagonal principal?

{{< alternativa >}} 1, 2 e 3 {{< /alternativa >}}
{{< alternativa >}} 3, 5 e 7 {{< /alternativa >}}
{{< alternativa >}} 1, 5 e 9 {{< /alternativa >}}
{{< alternativa >}} 7, 8 e 9 {{< /alternativa >}}
{{< solucao letra="C" >}}
A diagonal principal é formada pelos elementos em que o índice da linha é igual ao índice da coluna: `matriz[0][0]`, `matriz[1][1]` e `matriz[2][2]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
matriz = [
    [1, 2],
    [3, 4]
]

for i in range(2):
    for j in range(2):
        print(matriz[i][j])
{{< /code >}}

{{< alternativa >}} 1, 2, 3, 4 {{< /alternativa >}}
{{< alternativa >}} 1, 3, 2, 4 {{< /alternativa >}}
{{< alternativa >}} 4, 3, 2, 1 {{< /alternativa >}}
{{< alternativa >}} 1, 4, 2, 3 {{< /alternativa >}}
{{< solucao letra="A" >}}
O primeiro `for` percorre as linhas e o segundo percorre as colunas. Os elementos são acessados na ordem `matriz[0][0]`, `matriz[0][1]`, `matriz[1][0]` e `matriz[1][1]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere a matriz abaixo:

{{< code >}}
matriz = [
    [1, 2],
    [3, 4]
]
{{< /code >}}

Qual expressão acessa a primeira linha da matriz?

{{< alternativa >}} `matriz[0]` {{< /alternativa >}}
{{< alternativa >}} `matriz[1]` {{< /alternativa >}}
{{< alternativa >}} `matriz[0][0]` {{< /alternativa >}}
{{< alternativa >}} `matriz[1][1]` {{< /alternativa >}}
{{< solucao letra="A" >}}
`matriz[0]` acessa a primeira lista interna, que representa a primeira linha da matriz.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere a matriz abaixo:

{{< code >}}
matriz = [
    [10, 20, 30],
    [40, 50, 60]
]
{{< /code >}}

Qual expressão acessa a terceira coluna da primeira linha?

{{< alternativa >}} `matriz[0][0]` {{< /alternativa >}}
{{< alternativa >}} `matriz[0][1]` {{< /alternativa >}}
{{< alternativa >}} `matriz[0][2]` {{< /alternativa >}}
{{< alternativa >}} `matriz[1][2]` {{< /alternativa >}}
{{< solucao letra="C" >}}
A primeira linha possui índice 0 e a terceira coluna possui índice 2. Portanto, o acesso é `matriz[0][2]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
matriz = [
    [1, 2],
    [3, 4]
]

for linha in matriz:
    print(sum(linha))
{{< /code >}}

{{< alternativa >}} 3 e 7 {{< /alternativa >}}
{{< alternativa >}} 4 e 6 {{< /alternativa >}}
{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 1, 2, 3 e 4 {{< /alternativa >}}
{{< solucao letra="A" >}}
A soma da primeira linha é 3 e a soma da segunda linha é 7.
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

---
title: "Exercícios sobre Dividir para Conquistar"
description: "Exercícios sobre Dividir para Conquistar"
slug: dividir-conquistar-exercicios
tags:
- python
- dividir-conquistar
- exercicios
---


{{< lista-questoes >}}

{{< questao >}}
Dado um vetor de números ordenado <i>v</i>, verifique se existe o elemento <i>alvo</i>. Caso existir, retorne a posição do elemento. Caso contrário retorne -1. Implemente o algortimo de busca binária.

<br><br>

<b>Exemplo:</b>

{{< code >}}
Entrada:
v = [1 ,3 ,5 ,10, 15, 19, 89]
alvo = 3

Saída: 2
{{< /code >}}
<br><br>
<b>Exemplo 2:</b>

{{< code >}}
Entrada:
v = [1 ,3 ,5 ,10, 15, 19, 89]
alvo = 7

Saída: -1

{{< /code >}}

{{< solucao letra=" " >}}


{{< /solucao >}}


{{< /questao >}}


{{< questao >}}
Dado um vetor de números <i>v</i>, realize a ordenação dos elementos em ordem crescente. Implemente o algortimo de ordenação quick-sort.

<br><br>

<b>Exemplo:</b>

{{< code >}}
Entrada:
v = [1 ,3 ,5 ,10, 15, 19, 89]

Saída: [1 ,3 ,5 ,10, 15, 19, 89]
{{< /code >}}
<br><br>
<b>Exemplo 2:</b>

{{< code >}}
Entrada:
v = [8, 7, 9, -1, 19]

Saída:  [-1, 8, 7, 9, 19]

{{< /code >}}

{{< solucao letra=" " >}}


{{< /solucao >}}


{{< /questao >}}


{{< questao >}}
Um terreno retangular possui largura L e altura A. Deseja-se dividir esse terreno em quadrados iguais, tão grandes quanto possível, sem que haja sobras. Implemente um algoritmo utilizando o paradigma Dividir para Conquistar para determinar o tamanho do lado desses quadrados.

<img src="https://www.shutterstock.com/image-vector/seamless-hand-drawn-square-grid-260nw-2754856577.jpg" alt="Grade de quadrados">

<br><br>

<b>Exemplo 1:</b>

{{< code >}}
Entrada:
L = 168
A = 64

Saída: 8
{{< /code >}}

<br><br>

<b>Exemplo 2:</b>

{{< code >}}
Entrada:
L = 24
A = 16

Saída: 8
{{< /code >}}

{{< solucao letra=" " >}}

{{< /solucao >}}

{{< /questao >}}


{{< questao >}}
Você possui 9 moedas visualmente idênticas, sendo que uma delas é falsa e pesa menos que as demais. As outras 8 moedas possuem exatamente o mesmo peso.
<br><br>
Você dispõe de uma balança de dois pratos, que permite comparar dois grupos de moedas e informar qual grupo é mais leve ou se ambos possuem o mesmo peso.
<br><br>
Implemente um algoritmo utilizando o paradigma Dividir para Conquistar para descobrir qual moeda é falsa, realizando o menor número possível de pesagens.
<br><br>
Considere que existe uma função `pesar(grupo1, grupo2)` que recebe dois grupos de moedas e retorna qual grupo é mais leve ou se ambos possuem o mesmo peso. Você pode utilizar essa função, mas não conhece previamente a moeda falsa.

<br><br>

<b>Exemplo 1:</b>

{{< code >}}
Entrada:
moedas = [1, 2, 3, 4, 5, 6, 7, 8, 9]

Saída:
Moeda falsa: 7
Número de pesagens: 2
{{< /code >}}
<br>
<b>Exemplo 2:</b>

{{< code >}}
Entrada:
moedas = [1, 2, 3, 4, 5, 6, 7, 8, 9]

Saída:
Moeda falsa: 3
Número de pesagens: 2
{{< /code >}}

Os exemplos representam execuções diferentes. A moeda falsa não é informada na entrada; ela deve ser descoberta pelo algoritmo por meio das pesagens.

{{< solucao letra=" " >}}

{{< /solucao >}}

{{< /questao >}}

{{< /lista-questoes >}}

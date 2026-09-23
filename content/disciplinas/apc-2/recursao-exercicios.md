---
title: "Exercícios sobre Recursão"
description: "Exercícios sobre recursão"
slug: recursao-exercicios
tags:
- python
- recursao
- exercicios
---


{{< lista-questoes >}}

{{< questao >}}
Faça uma função recursiva para somar todos os elementos em uma lista.
{{< solucao letra=" ">}}
def somar(lista, pos=0):
  if pos == len(lista):
    return 0
  return somar(lista,pos+1)+lista[pos]
{{< /solucao >}}

{{< /questao >}}

{{< questao >}}
Faça uma função recursiva para calcular a média dos valores em uma lista.
{{< /questao >}}

{{< questao >}}
Faça uma função recursiva para encontrar o maior valor em uma lista.
{{< /questao >}}

{{< questao >}}
Faça uma função recursiva para encontrar o menor valor em uma lista.
{{< /questao >}}

{{< questao >}}
Faça uma função recursiva que some dois números inteiro não negativos, x e y, usando apenas incrementos e decrementos unitários.
{{< /questao >}}


{{< questao >}}
Faça uma função recursiva que multiplique dois números inteiro positivos, x e y, usando apenas somas e subtrações.
{{< /questao >}}

{{< questao >}}
Faça uma função recursiva que calcule o Máximo Divisor Comum entre dois números inteiros não negativos. Confira o algoritmo de Euclides.
{{< /questao >}}

{{< questao >}}
Faça uma função recursiva que verifique se uma determinada string é um palíndromo.
{{< /questao >}}

{{< questao >}}
Faça uma função recursiva que inverta uma String.
{{< /questao >}}

{{< questao >}}
Faça uma função recursiva que, dado um número inteiro positivo n, retorne a representação binária de n.
{{< /questao >}}

{{< questao >}}
Faça uma função recursiva que, dada uma string s e um caractere c, conte o número de ocorrências do caractere c na string s.
{{< /questao >}}

{{< questao >}}
Faça uma função recursiva que calcule o fatorial de um número inteiro não negativo n.
{{< /questao >}}

{{< questao >}}
Faça uma função recursiva que calcule o n-ésimo termo da sequência de Fibonacci.
{{< /questao >}}

{{< questao >}}
Faça uma função recursiva que determine se um número inteiro positivo é primo.
{{< /questao >}}

{{< questao >}}
Faça uma função recursiva que verifique se uma lista está ordenada em ordem crescente.
{{< /questao >}}

{{< questao >}}
Faça uma função recursiva que encontre o segundo maior elemento de uma lista.
{{< /questao >}}

{{< questao >}}
Faça uma função recursiva que remova todas as ocorrências de um determinado valor de uma lista.
{{< /questao >}}

{{< /lista-questoes >}}

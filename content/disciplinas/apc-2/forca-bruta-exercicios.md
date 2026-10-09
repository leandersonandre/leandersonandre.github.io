---
title: "Exercícios sobre Força Bruta"
description: "Exercícios sobre Força Bruta"
slug: forca-bruta-exercicios
tags:
- python
- forca-bruta
- exercicios
---


{{< lista-questoes >}}

{{< questao >}}

<b>Maior subarray:</b>
Dado um vetor de números, encontrar o intervalo contíguo cuja soma seja
máxima.
<br>

{{< code >}}
Exemplo 01:
Entrada: Vetor [ 1, 2, 3, 4, 5]
Saída: Vetor [ 2, 3, 4, 5]

Exemplo 02:
Entrada: Vetor [ -1, 2, -3, 4, -5]
Saída: Vetor [4]
{{< /code >}}

 {{< solucao   letra=" " >}} 


{{< code >}}
def maior_subarray(lista):,
        # define o tamanho do subarray,
        # 1, 2, 3, ...,
        # indices do subarray com a maior soma,
        subarray = [],
        maior_soma = 0,
        for tamanho in range(1,len(lista)):,
            for i in range(len(lista)):,
                soma = 0,
                temp_subarray = [],
                # evita acessar posições inválidas,
                # além do tamanho da lista,
                if i + tamanho <= len(lista):,
                    for j in range(tamanho):,
                        temp_subarray.append(lista[i+j]),
                        soma += lista[i+j],
                # se ainda não foi definido um subarray,
                if len(subarray) == 0:,
                    subarray = temp_subarray,
                    maior_soma = soma,
                # se encontrei um subarray com uma soma maior,
                elif maior_soma < soma:,
                    subarray = temp_subarray,
                    maior_soma = soma,
        return subarray,
    print(maior_subarray([1,2,3,4])),
    print(maior_subarray([-1,2,-2,-4,8])),
    print(maior_subarray([0,0,0,0]))

{{< /code >}}

 {{< /solucao >}} 

{{< /questao >}}

{{< questao >}}
Dado um conjunto de números e um valor <i>S</i>, verificar se existe algum
subconjunto cuja soma seja igual a <i>S</i>.

<br><br>
<b>Entrada:</b>
Um conjunto de números inteiros e um valor <i>S</i>, que representa a soma procurada.
<br><br>
<b>Saída:</b>
Os elementos de um subconjunto cuja soma seja igual a <i>S</i> ou uma mensagem informando que não existe tal subconjunto.
<br><br>
<b>Exemplo:</b>

{{< code >}}
Entrada:
2 4 7 10 15
17

Saída:
Subconjunto encontrado: 2 15
{{< /code >}}
<br><br>
<b>Exemplo 2:</b>

{{< code >}}
Entrada:
3 5 8 12 20
16

Saída:
Subconjunto encontrado: 3 5 8
{{< /code >}}
<br><br>
<b>Exemplo 3:</b>

{{< code >}}
Entrada:
2 4 6 9 11
20

Saída:
Subconjunto não encontrado.
{{< /code >}}


{{< /questao >}}

{{< questao >}}
Considere um cadeado que utiliza uma combinação de 4 dígitos, sendo que cada posição pode assumir um valor de 0 a 9.
<br>
O objetivo é desenvolver um algoritmo que utilize a técnica de força bruta (brute force) para descobrir a combinação correta do cadeado.
<br>
O algoritmo deve testar, de forma sistemática, todas as combinações possíveis, começando por 0000 e avançando até 9999, até encontrar a combinação que corresponde à senha definida.

Por exemplo, se a combinação correta for 5732, o algoritmo deverá testar:
{{< code >}}
0000
0001
0002
...
5730
5731
5732  ← combinação encontrada
{{< /code >}}
O algoritmo deve informar a combinação encontrada e a quantidade de tentativas realizadas até descobri-la.

{{< solucao letra=" " >}}


{{< /solucao >}}

{{< /questao >}}

{{< questao >}}
Considere uma sequência de DNA representada pelos caracteres A, C, G e T. Dada uma sequência de DNA maior e uma sequência menor, o objetivo é descobrir se a sequência menor aparece como uma substring dentro da sequência maior.

Por exemplo, considere a seguinte entrada:

{{< code >}}
Sequência de DNA:
ACGTACGTTACGGAATCG

Sequência procurada:
TACG
{{< /code >}}

A sequência TACG aparece dentro da sequência de DNA, começando na posição 4.
<br><br>
O algoritmo deve realizar a busca comparando a sequência procurada com cada possível posição da sequência de DNA. Caso encontre uma correspondência completa, deve informar a posição onde ela começa. Caso contrário, deve informar que a sequência não foi encontrada.
<br><br>
<b>Entrada:</b>
Duas sequências de DNA, sendo a primeira a sequência onde será realizada a busca e a segunda a sequência que deve ser procurada.
<br><br>
<b>Saída:</b>
A posição em que a sequência procurada foi encontrada ou uma mensagem informando que ela não existe na sequência.
<br><br>
<b>Exemplo:</b>

{{< code >}}
Entrada:
ACGTACGTTACGGAATCG
TACG

Saída:
Sequência encontrada na posição 4.

{{< /code >}}

<br>
{{< /questao >}}


{{< /lista-questoes >}}

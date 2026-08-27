---
title: "Exercícios sobre Listas"
description: "Exercícios sobre a estrutura de dados lista em Python"
slug: listas-exercicios
tags:
- python
- listas
- exercícios
---

{{< lista-questoes >}}

{{< questao >}}
Crie uma lista chamada `frutas` contendo as seguintes frutas: `"maçã"`, `"banana"`, `"laranja"` e `"uva"`. Depois, exiba a lista na tela.
{{< solucao letra=" " >}}

{{< code >}}
frutas = ["maçã", "banana", "laranja", "uva"]

print(frutas)
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Crie uma lista chamada `numeros` contendo os números `10`, `20`, `30`, `40` e `50`. Depois, exiba o primeiro e o último elemento da lista.
{{< solucao letra=" " >}}

{{< code >}}
numeros = [10, 20, 30, 40, 50]

print(numeros[0])
print(numeros[-1])
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Crie uma lista chamada `nomes` contendo cinco nomes. Depois, peça ao usuário um número de índice e exiba o nome armazenado nessa posição da lista.
{{< solucao letra=" " >}}

{{< code >}}
nomes = ["Ana", "Bruno", "Carlos", "Daniela", "Eduardo"]

indice = int(input())

print(nomes[indice])
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Crie uma lista chamada `cores` contendo `"vermelho"`, `"verde"` e `"azul"`. Depois, adicione a cor `"amarelo"` ao final da lista e exiba a lista.
{{< solucao letra=" " >}}

{{< code >}}
cores = ["vermelho", "verde", "azul"]

cores.append("amarelo")

print(cores)
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Crie uma lista chamada `frutas` contendo `"maçã"`, `"banana"` e `"laranja"`. Depois, insira `"uva"` na segunda posição da lista e exiba a lista.
{{< solucao letra=" " >}}

{{< code >}}
frutas = ["maçã", "banana", "laranja"]

frutas.insert(1, "uva")

print(frutas)
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Crie uma lista chamada `animais` contendo `"cachorro"`, `"gato"`, `"coelho"` e `"peixe"`. Depois, remova `"coelho"` da lista e exiba a lista.
{{< solucao letra=" " >}}

{{< code >}}
animais = ["cachorro", "gato", "coelho", "peixe"]

animais.remove("coelho")

print(animais)
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Crie uma lista chamada `numeros` contendo os números `5`, `10`, `15`, `20` e `25`. Depois, remova o último elemento da lista e exiba a lista.
{{< solucao letra=" " >}}

{{< code >}}
numeros = [5, 10, 15, 20, 25]

numeros.pop()

print(numeros)
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Crie uma lista chamada `alunos` contendo os nomes `"Ana"`, `"Bruno"`, `"Carlos"` e `"Daniela"`. Depois, peça ao usuário um nome e informe se esse nome está ou não na lista.
{{< solucao letra=" " >}}

{{< code >}}
alunos = ["Ana", "Bruno", "Carlos", "Daniela"]

nome = input()

if nome in alunos:
    print("Está na lista")
else:
    print("Não está na lista")
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Crie uma lista chamada `numeros` contendo os números `10`, `20`, `30`, `40` e `50`. Depois, informe quantos elementos existem na lista.
{{< solucao letra=" " >}}

{{< code >}}
numeros = [10, 20, 30, 40, 50]

print(len(numeros))
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Crie uma lista contendo cinco números inteiros. Depois, calcule e exiba a soma de todos os elementos da lista.
{{< solucao letra=" " >}}

{{< code >}}
numeros = [10, 20, 30, 40, 50]

print(sum(numeros))
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Crie uma lista contendo cinco números inteiros. Depois, exiba o maior e o menor número da lista.
{{< solucao letra=" " >}}

{{< code >}}
numeros = [15, 8, 32, 21, 10]

print(max(numeros))
print(min(numeros))
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Crie uma lista contendo cinco números inteiros. Depois, peça ao usuário um número e informe quantas vezes esse número aparece na lista.
{{< solucao letra=" " >}}

{{< code >}}
numeros = [10, 20, 10, 30, 10]

numero = int(input())

print(numeros.count(numero))
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Crie uma lista contendo cinco números inteiros. Depois, ordene os elementos em ordem crescente e exiba a lista.
{{< solucao letra=" " >}}

{{< code >}}
numeros = [50, 10, 40, 20, 30]

numeros.sort()

print(numeros)
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Crie uma lista contendo cinco números inteiros. Depois, exiba os elementos da lista um por um utilizando uma estrutura de repetição.
{{< solucao letra=" " >}}

{{< code >}}
numeros = [10, 20, 30, 40, 50]

for numero in numeros:
    print(numero)
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Crie uma lista contendo cinco números inteiros. Depois, percorra a lista e exiba apenas os números pares.
{{< solucao letra=" " >}}

{{< code >}}
numeros = [10, 15, 22, 31, 40]

for numero in numeros:
    if numero % 2 == 0:
        print(numero)
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Faça um programa que leia cinco números inteiros e armazene-os em uma lista. Depois, exiba todos os números armazenados na lista.
{{< solucao letra=" " >}}

{{< code >}}
numeros = []

for i in range(5):
    numero = int(input())
    numeros.append(numero)

print(numeros)
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Faça um programa que leia cinco números inteiros e armazene-os em uma lista. Depois, calcule e exiba a soma dos números armazenados.
{{< solucao letra=" " >}}

{{< code >}}
numeros = []

for i in range(5):
    numero = int(input())
    numeros.append(numero)

print(sum(numeros))
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Faça um programa que leia cinco números inteiros e armazene-os em uma lista. Depois, percorra a lista e exiba somente os números maiores que 10.
{{< solucao letra=" " >}}

{{< code >}}
numeros = []

for i in range(5):
    numero = int(input())
    numeros.append(numero)

for numero in numeros:
    if numero > 10:
        print(numero)
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Faça um programa que leia dez números inteiros e armazene-os em uma lista. Depois, percorra a lista e conte quantos números são pares e quantos são ímpares.
{{< solucao letra=" " >}}

{{< code >}}
numeros = []

for i in range(10):
    numero = int(input())
    numeros.append(numero)

pares = 0
impares = 0

for numero in numeros:
    if numero % 2 == 0:
        pares += 1
    else:
        impares += 1

print(pares)
print(impares)
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Faça um programa que leia cinco notas, armazene-as em uma lista e calcule a média das notas. Depois, informe a média e quantas notas são maiores ou iguais a 7.
{{< solucao letra=" " >}}

{{< code >}}
notas = []

for i in range(5):
    nota = float(input())
    notas.append(nota)

media = sum(notas) / len(notas)

aprovados = 0

for nota in notas:
    if nota >= 7:
        aprovados += 1

print(media)
print(aprovados)
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Faça um programa que leia dez números inteiros e armazene-os em uma lista. Depois, crie uma segunda lista contendo apenas os números positivos da primeira lista.
{{< solucao letra=" " >}}

{{< code >}}
numeros = []

for i in range(10):
    numero = int(input())
    numeros.append(numero)

positivos = []

for numero in numeros:
    if numero > 0:
        positivos.append(numero)

print(positivos)
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Faça um programa que leia uma lista de números inteiros e, depois, crie uma nova lista contendo os elementos da primeira lista em ordem inversa.
{{< solucao letra=" " >}}

{{< code >}}
numeros = [10, 20, 30, 40, 50]

inversa = []

for i in range(len(numeros) - 1, -1, -1):
    inversa.append(numeros[i])

print(inversa)
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Faça um programa que leia dez números inteiros e armazene-os em uma lista. Depois, peça ao usuário um número e informe a posição em que ele aparece pela primeira vez na lista. Caso o número não esteja na lista, informe que ele não foi encontrado.
{{< solucao letra=" " >}}

{{< code >}}
numeros = []

for i in range(10):
    numero = int(input())
    numeros.append(numero)

busca = int(input())

if busca in numeros:
    print(numeros.index(busca))
else:
    print("Não encontrado")
{{< /code >}}

{{< /solucao >}}
{{< /questao >}}


{{< /lista-questoes >}}

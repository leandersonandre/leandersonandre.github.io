---
title: "Exercícios"
description: "Exercícios"
slug: exercicios-01
tags:
- python
- exercícios
---

{{< lista-questoes >}}


{{< questao >}}

Faça um programa que exibe no terminal um Triângulo de Pascal. O programa deve pedir a quantidades de linhas que o triângulo deverá ter.

<table style="text-align:left; border-collapse: collapse;">
  <tr>
    <td>1</td>
  </tr>
  <tr>
    <td>1</td><td>1</td>
  </tr>
  <tr>
    <td>1</td><td>2</td><td>1</td>
  </tr>
  <tr>
    <td>1</td><td>3</td><td>3</td><td>1</td>
  </tr>
  <tr>
    <td>1</td><td>4</td><td>6</td><td>4</td><td>1</td>
  </tr>
  <tr>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
  </tr>
</table>

{{< solucao letra=" " >}}
{{< code >}}
linhas = int(input("Digite a quantidade de linhas: "))

for i in range(linhas):
    valor = 1

    for j in range(i + 1):
        print(valor, end="\t")

        # Calcula o próximo número da linha
        valor = valor * (i - j) // (j + 1)

    print()

{{< /code >}}
{{< /solucao >}}

{{< /questao >}}


{{< questao >}}

Modifique o programa do Triângulo de pascal utilizando as demais  estruturas de repetição ( ENQUANTO-FAÇA, REPITA-ATÉ, PARA=ATÉ-FAÇA).

{{< /questao >}}

{{< questao >}}

Modifique o programa do Triângulo de Pascal para que imprima o triângulo alinhado a direita.

<table style="text-align:right; border-collapse: collapse;">
  <tr>
    <td colspan="5">1</td>
  </tr>
  <tr>
    <td colspan="4">1</td><td>1</td>
  </tr>
  <tr>
    <td colspan="3">1</td><td>2</td><td>1</td>
  </tr>
  <tr>
    <td colspan="2">1</td><td>3</td><td>3</td><td>1</td>
  </tr>
  <tr>
    <td>1</td><td>4</td><td>6</td><td>4</td><td>1</td>
  </tr>
  <tr>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
  </tr>
</table>

{{< solucao letra=" " >}}
{{< code >}}
linhas = int(input("Digite a quantidade de linhas: "))

for i in range(linhas):
    valor = 1

    # Espaços para alinhar à direita
    for espaco in range(linhas - i - 1):
        print("    ", end="")

    # Impressão dos valores da linha
    for j in range(i + 1):
        print(f"{valor:4}", end="")

        # Calcula o próximo valor
        valor = valor * (i - j) // (j + 1)

    print()
{{< /code >}}
{{< /solucao >}}

{{< /questao >}}


{{< questao >}}

Escreva um programa que permita a entrada de um número N inteiro e então exiba a decomposição desse número em seus fatores primos, exemplo:
<br><br>
6 = 2 (1) 3(1)
<br>
9 = 3(2)
<br>
24 = 2(3) 3(1)
<br><br>
Onde, o número entre parênteses indica a potência do fator.

{{< solucao letra=" " >}}
{{< code >}}
n = int(input("Digite um número inteiro: "))

numero = n
divisor = 2

print(f"{n} =", end=" ")

while numero > 1:
    contador = 0

    # Conta quantas vezes o divisor divide o número
    while numero % divisor == 0:
        numero = numero // divisor
        contador += 1

    # Exibe o fator e sua potência
    if contador > 0:
        print(f"{divisor}({contador})", end=" ")

    divisor += 1
{{< /code >}}
{{< /solucao >}}

{{< /questao >}}


{{< questao >}}

<b>Problema A - Atenção a Reunião (Maratona Fase Regional 2025)</b>
<br>

 <a href="https://github.com/univille-cp/cadernos-de-problemas/blob/main/maratona-de-programacao/regional/2024.pdf">Descrição da questão </a>

<br>
<a href="https://codeforces.com/gym/105327/problem/A">
    Submeta a sua solução no CodeForces</a>

{{< solucao letra=" " >}}
{{< code >}}
diretores = int(input())
tempo = int(input())
tempo_que_sobra = tempo - (diretores-1)
tempoDeCadaFala = int(tempo_que_sobra / diretores)
print(tempoDeCadaFala)
{{< /code >}}
{{< /solucao >}}

{{< /questao >}}

{{< /lista-questoes >}}

---
title: "Exercícios sobre Repetições"
description: "Exercícios sobre Estrutura de repetições em Python"
slug: repeticoes-exercicios
tags:
- python
- while-for
- repetições
- questões
---

{{< lista-questoes >}}

{{< questao >}}
Faça um programa que calcule a soma dos números inteiros de 1 a 100.
{{< solucao letra="A" >}}

{{< code >}}
soma = 0
for i in range(1, 101):
    soma += i

print(soma)

{{< /code >}}

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Escreva um programa que pergunte ao usuário um número e imprima a soma de 1 até o número informado. Exemplo: 5 → 1 + 2 + 3 + 4 + 5 = 15.
{{< solucao letra="B" >}}

{{< code >}}
n = int(input())

soma = 0
for i in range(1, n + 1):
    soma += i

print(soma)

{{< /code >}}

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Faça um programa que peça dois números (base e expoente) e calcule a potência sem utilizar funções prontas da linguagem.
{{< solucao letra="C" >}}

{{< code >}}
base = int(input())
expoente = int(input())

resultado = 1
for i in range(expoente):
    resultado *= base

print(resultado)

{{< /code >}}

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Construa um programa que exiba a tabuada de 1 até N, onde N é informado pelo usuário.
{{< solucao letra="D" >}}

{{< code >}}
n = int(input())

for i in range(1, n + 1):
    for j in range(1, 11):
        print(i, "x", j, "=", i * j)
    print()

{{< /code >}}

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Faça um programa para calcular e imprimir a soma dos cubos dos números pares compreendidos entre A e B (B > A). A e B são lidos pelo teclado.
{{< solucao letra="E" >}}

{{< code >}}
a = int(input())
b = int(input())

soma = 0
for i in range(a, b + 1):
    if i % 2 == 0:
        soma += i ** 3

print(soma)

{{< /code >}}

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Faça um programa que receba um valor que foi depositado na poupança e exiba o valor com rendimento mês a mês durante o período de um ano. Considere fixo o juros da poupança em 0,5% a. m.
{{< solucao letra="F" >}}

{{< code >}}
valor = float(input())

for i in range(12):
    valor *= 1.005
    print(valor)

{{< /code >}}

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Número primo é aquele que só é divisível por ele mesmo e pelo número 1. Faça um programa que peça um número inteiro ao usuário e determine se o número informado é primo ou não.
{{< solucao letra="G" >}}

{{< code >}}
n = int(input())

primo = True

if n <= 1:
    primo = False
else:
    for i in range(2, n):
        if n % i == 0:
            primo = False
            break

if primo:
    print("Primo")
else:
    print("Não primo")

{{< /code >}}

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Faça um programa que calcule o resultado dos 50 primeiros números da seguinte sequência:

1000/1 - 997/2 + 994/3 - 991/4 + ...
{{< solucao letra="H" >}}

{{< code >}}
numerador = 1000
soma = 0

for i in range(1, 51):
    termo = numerador / i
    if i % 2 == 0:
        soma -= termo
    else:
        soma += termo
    numerador -= 3

print(soma)

{{< /code >}}

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Faça um programa para calcular e imprimir a seguinte equação:

37 × (38/1) + 38 × (36/2) + 35 × (36/3) + ... + 1 × (2/37)
{{< solucao letra="I" >}}

{{< code >}}
soma = 0

for i in range(1, 38):
    soma += (38 - i + 1) * ((38 - i * 2 + 2) / i)

print(soma)

{{< /code >}}

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Anacleto tem 1,50m e cresce 2 centímetros por ano, enquanto Felisberto tem 1,10m e cresce 3 centímetros por ano. Construa um programa que calcule e apresente quantos anos serão necessários para que Felisberto seja maior que Anacleto.
{{< solucao letra="J" >}}

{{< code >}}
a = 1.50
f = 1.10
anos = 0

while f <= a:
    a += 0.02
    f += 0.03
    anos += 1

print(anos)

{{< /code >}}

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Um determinado material radioativo perde metade de sua massa a cada 50 segundos. Dada a massa inicial, em gramas, faça um programa que determine o tempo necessário para que essa massa se torne menor que 0,05 gramas.
{{< solucao letra="K" >}}

{{< code >}}
massa = float(input())
tempo = 0

while massa >= 0.05:
    massa /= 2
    tempo += 50

print(tempo)

{{< /code >}}

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Supondo que a população de um país A seja da ordem de 80.000 habitantes com uma taxa anual de crescimento de 3% e que a população de B seja 200.000 habitantes com uma taxa de crescimento de 1,5%. Faça um programa que calcule e imprima o número de anos necessários para que a população do país A ultrapasse ou iguale a população do país B, mantidas as taxas de crescimento.
{{< solucao letra="L" >}}

{{< code >}}
a = 80000
b = 200000
anos = 0

while a <= b:
    a *= 1.03
    b *= 1.015
    anos += 1

print(anos)

{{< /code >}}

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Uma rainha requisitou os serviços de um monge e disse-lhe que pagaria qualquer preço. O monge, necessitando de alimentos, indagou à rainha sobre o pagamento, se poderia ser feito com grãos de trigo dispostos em um tabuleiro de xadrez (que possui 64 casas), de tal forma que o primeiro quadro deveria conter apenas um grão e os quadros subsequentes, o dobro do quadro anterior. Crie um programa para calcular o total de grãos que o monge recebeu.
{{< solucao letra="M" >}}

{{< code >}}
graos = 1
total = 0

for i in range(64):
    total += graos
    graos *= 2

print(total)

{{< /code >}}

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Escreva um programa que determine o fatorial de um número. Para este problema, tem-se como entrada o valor do número do qual se deseja calcular o fatorial.
{{< solucao letra="N" >}}

{{< code >}}
n = int(input())

fatorial = 1
for i in range(1, n + 1):
    fatorial *= i

print(fatorial)

{{< /code >}}

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Faça um programa que peça para o usuário ir informando números até que ele informe 0 (zero). Após isto apresente os dados solicitados.
{{< solucao letra="O" >}}

{{< code >}}
maior = None
menor = None
soma = 0
pares = 0
impares = 0
cont = 0

while True:
    n = int(input())
    if n == 0:
        break

    soma += n
    cont += 1

    if maior is None or n > maior:
        maior = n

    if menor is None or n < menor:
        menor = n

    if n % 2 == 0:
        pares += 1
    else:
        impares += 1

media = soma / cont if cont > 0 else 0

print(maior)
print(menor)
print(soma)
print(media)
print(pares)
print(impares)

{{< /code >}}

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Leia um número positivo do usuário, então, calcule e imprima a sequência Fibonacci até o primeiro número superior ao número lido.
{{< solucao letra="P" >}}

{{< code >}}
n = int(input())

a, b = 0, 1

while a <= n:
    print(a)
    a, b = b, a + b

{{< /code >}}

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Faça um programa que peça ao usuário pensar em um número de 1 a 1000, o programa então tentará adivinhar o número pensando.
{{< solucao letra="Q" >}}
Confira sobre busca binária.

{{< code >}}
low = 1
high = 1000

for i in range(10):
    mid = (low + high) // 2
    print(mid)

    resp = input()

    if resp == "acertou":
        break
    elif resp == "maior":
        low = mid + 1
    else:
        high = mid - 1

{{< /code >}}

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O seguinte programa em Python não está funcionando e lhe foi pedido para que seja corrigido. Apenas olhando o código, qual foi o erro de programação?
{{< code >}}
cont1 = 0
cont2 = 0
brancos = 0
nulos = 0
voto = int(input())
while voto != -1:
    if voto == 1:
        cont1 += 1
    elif voto == 2:
        cont2 += 1
    elif voto == 0:
        brancos += 1
    else:
        nulos += 1
print(cont1)
print(cont2)
print(brancos)
print(nulos)
{{< /code >}}
{{< solucao letra="R" >}}

{{< code >}}
# O erro é que a variável "voto" não é atualizada dentro do laço.
# Isso provoca loop infinito.

cont1 = 0
cont2 = 0
brancos = 0
nulos = 0

while True:
    voto = int(input())
    if voto == -1:
        break

    if voto == 1:
        cont1 += 1
    elif voto == 2:
        cont2 += 1
    elif voto == 0:
        brancos += 1
    else:
        nulos += 1

print(cont1)
print(cont2)
print(brancos)
print(nulos)

{{< /code >}}

{{< /solucao >}}
{{< /questao >}}




{{< /lista-questoes >}}

---
title: "Questões sobre Listas"
description: "Questões sobre a estrutura de dados lista em Python"
slug: listas-questoes
tags:
- python
- listas
- questões
---

{{< lista-questoes >}}

{{< questao >}}
O que é uma lista em Python?

{{< alternativa >}} Uma estrutura utilizada para representar uma sequência de objetos. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que pode armazenar apenas números inteiros. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que não permite alterar seus elementos. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura utilizada exclusivamente para armazenar textos. {{< /alternativa >}}
{{< solucao letra="A" >}}
Uma lista é uma estrutura de dados utilizada para representar uma sequência de objetos em Python.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Sobre listas em Python, qual alternativa está correta?

{{< alternativa >}} Uma lista não pode conter elementos repetidos. {{< /alternativa >}}
{{< alternativa >}} Uma lista mantém uma ordem para seus elementos e pode conter elementos repetidos. {{< /alternativa >}}
{{< alternativa >}} Uma lista pode armazenar somente elementos do mesmo tipo. {{< /alternativa >}}
{{< alternativa >}} Os elementos de uma lista não possuem posições. {{< /alternativa >}}
{{< solucao letra="B" >}}
Listas representam sequências ordenadas e permitem que um mesmo elemento apareça várias vezes.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual dos códigos abaixo cria corretamente uma lista contendo os números 10, 20 e 30?

{{< alternativa >}} `numeros = (10, 20, 30)` {{< /alternativa >}}
{{< alternativa >}} `numeros = {10, 20, 30}` {{< /alternativa >}}
{{< alternativa >}} `numeros = [10, 20, 30]` {{< /alternativa >}}
{{< alternativa >}} `numeros = <10, 20, 30>` {{< /alternativa >}}
{{< solucao letra="C" >}}
Listas em Python são definidas utilizando colchetes `[]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
frutas = ["maçã", "banana", "laranja"]

print(frutas[0])
{{< /code >}}

{{< alternativa >}} maçã {{< /alternativa >}}
{{< alternativa >}} banana {{< /alternativa >}}
{{< alternativa >}} laranja {{< /alternativa >}}
{{< alternativa >}} Nada será impresso {{< /alternativa >}}
{{< solucao letra="A" >}}
O primeiro elemento de uma lista está no índice 0.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = [10, 20, 30, 40]

print(numeros[2])
{{< /code >}}

{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 30 {{< /alternativa >}}
{{< alternativa >}} 40 {{< /alternativa >}}
{{< solucao letra="C" >}}
Os índices começam em 0. Portanto, o elemento no índice 2 é o número 30.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
frutas = ["maçã", "banana", "laranja"]

print(frutas[-1])
{{< /code >}}

{{< alternativa >}} maçã {{< /alternativa >}}
{{< alternativa >}} banana {{< /alternativa >}}
{{< alternativa >}} laranja {{< /alternativa >}}
{{< alternativa >}} Será gerado um erro {{< /alternativa >}}
{{< solucao letra="C" >}}
O índice `-1` representa o último elemento da lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = [10, 20, 30, 40]

print(numeros[-2])
{{< /code >}}

{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 30 {{< /alternativa >}}
{{< alternativa >}} 40 {{< /alternativa >}}
{{< solucao letra="C" >}}
O índice `-1` representa o último elemento e `-2` representa o penúltimo. Portanto, o resultado é 30.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = [10, 20, 30]

numeros[1] = 50

print(numeros)
{{< /code >}}

{{< alternativa >}} [10, 20, 30] {{< /alternativa >}}
{{< alternativa >}} [50, 20, 30] {{< /alternativa >}}
{{< alternativa >}} [10, 50, 30] {{< /alternativa >}}
{{< alternativa >}} [10, 20, 50] {{< /alternativa >}}
{{< solucao letra="C" >}}
O elemento localizado no índice 1 é substituído por 50.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a função do método <b>append()</b> em uma lista?

{{< alternativa >}} Remove o último elemento da lista. {{< /alternativa >}}
{{< alternativa >}} Adiciona um elemento ao final da lista. {{< /alternativa >}}
{{< alternativa >}} Ordena os elementos da lista. {{< /alternativa >}}
{{< alternativa >}} Retorna o tamanho da lista. {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `append()` adiciona um elemento ao final da lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = [10, 20, 30]

numeros.append(40)

print(numeros)
{{< /code >}}

{{< alternativa >}} [10, 20, 30] {{< /alternativa >}}
{{< alternativa >}} [40, 10, 20, 30] {{< /alternativa >}}
{{< alternativa >}} [10, 20, 40, 30] {{< /alternativa >}}
{{< alternativa >}} [10, 20, 30, 40] {{< /alternativa >}}
{{< solucao letra="D" >}}
O `append()` adiciona o elemento ao final da lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a função do método <b>insert()</b> em uma lista?

{{< alternativa >}} Remove um elemento da lista. {{< /alternativa >}}
{{< alternativa >}} Adiciona um elemento em uma posição específica da lista. {{< /alternativa >}}
{{< alternativa >}} Retorna o último elemento da lista. {{< /alternativa >}}
{{< alternativa >}} Ordena a lista em ordem crescente. {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `insert()` permite adicionar um elemento em uma posição específica da lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
frutas = ["maçã", "laranja"]

frutas.insert(1, "banana")

print(frutas)
{{< /code >}}

{{< alternativa >}} ["banana", "maçã", "laranja"] {{< /alternativa >}}
{{< alternativa >}} ["maçã", "banana", "laranja"] {{< /alternativa >}}
{{< alternativa >}} ["maçã", "laranja", "banana"] {{< /alternativa >}}
{{< alternativa >}} ["banana", "laranja", "maçã"] {{< /alternativa >}}
{{< solucao letra="B" >}}
O `insert(1, "banana")` insere `"banana"` no índice 1.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a função do método <b>remove()</b> em uma lista?

{{< alternativa >}} Remove o elemento informado da lista. {{< /alternativa >}}
{{< alternativa >}} Remove sempre o primeiro elemento da lista. {{< /alternativa >}}
{{< alternativa >}} Remove sempre o último elemento da lista. {{< /alternativa >}}
{{< alternativa >}} Remove todos os elementos da lista. {{< /alternativa >}}
{{< solucao letra="A" >}}
O método `remove()` remove da lista a primeira ocorrência do valor informado.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
frutas = ["maçã", "banana", "laranja", "banana"]

frutas.remove("banana")

print(frutas)
{{< /code >}}

{{< alternativa >}} ["maçã", "banana", "laranja", "banana"] {{< /alternativa >}}
{{< alternativa >}} ["maçã", "laranja", "banana"] {{< /alternativa >}}
{{< alternativa >}} ["maçã", "banana", "laranja"] {{< /alternativa >}}
{{< alternativa >}} ["maçã", "laranja"] {{< /alternativa >}}
{{< solucao letra="B" >}}
O `remove()` remove apenas a primeira ocorrência do valor informado.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a função do método <b>pop()</b> quando utilizado sem argumentos?

{{< alternativa >}} Remove e retorna o primeiro elemento da lista. {{< /alternativa >}}
{{< alternativa >}} Remove e retorna o último elemento da lista. {{< /alternativa >}}
{{< alternativa >}} Remove todos os elementos da lista. {{< /alternativa >}}
{{< alternativa >}} Apenas retorna o último elemento sem removê-lo. {{< /alternativa >}}
{{< solucao letra="B" >}}
Quando utilizado sem argumentos, `pop()` remove e retorna o último elemento da lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = [10, 20, 30, 40]

x = numeros.pop()

print(x)
{{< /code >}}

{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 30 {{< /alternativa >}}
{{< alternativa >}} 40 {{< /alternativa >}}
{{< solucao letra="D" >}}
Sem argumentos, `pop()` remove e retorna o último elemento da lista, que é 40.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual função pode ser utilizada para descobrir a quantidade de elementos de uma lista?

{{< alternativa >}} `size()` {{< /alternativa >}}
{{< alternativa >}} `length()` {{< /alternativa >}}
{{< alternativa >}} `len()` {{< /alternativa >}}
{{< alternativa >}} `countAll()` {{< /alternativa >}}
{{< solucao letra="C" >}}
A função `len()` retorna a quantidade de elementos de uma lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
frutas = ["maçã", "banana", "laranja", "uva"]

print(len(frutas))
{{< /code >}}

{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} Será gerado um erro {{< /alternativa >}}
{{< solucao letra="B" >}}
A lista possui quatro elementos, portanto `len(frutas)` retorna 4.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = [10, 20, 30, 20, 40]

print(numeros.count(20))
{{< /code >}}

{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< solucao letra="B" >}}
O número 20 aparece duas vezes na lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual operador pode ser utilizado para verificar se um elemento pertence a uma lista?

{{< alternativa >}} `has` {{< /alternativa >}}
{{< alternativa >}} `contains` {{< /alternativa >}}
{{< alternativa >}} `in` {{< /alternativa >}}
{{< alternativa >}} `exists` {{< /alternativa >}}
{{< solucao letra="C" >}}
O operador `in` verifica se um elemento está presente na lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
frutas = ["maçã", "banana", "laranja"]

print("banana" in frutas)
{{< /code >}}

{{< alternativa >}} True {{< /alternativa >}}
{{< alternativa >}} False {{< /alternativa >}}
{{< alternativa >}} banana {{< /alternativa >}}
{{< alternativa >}} Será gerado um erro {{< /alternativa >}}
{{< solucao letra="A" >}}
Como `"banana"` está presente na lista, a expressão `"banana" in frutas` resulta em `True`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = [10, 20, 30]

print(40 in numeros)
{{< /code >}}

{{< alternativa >}} True {{< /alternativa >}}
{{< alternativa >}} False {{< /alternativa >}}
{{< alternativa >}} 40 {{< /alternativa >}}
{{< alternativa >}} Nada será impresso {{< /alternativa >}}
{{< solucao letra="B" >}}
O número 40 não está presente na lista, portanto a expressão resulta em `False`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a função do método <b>index()</b> em uma lista?

{{< alternativa >}} Retornar o número de elementos da lista. {{< /alternativa >}}
{{< alternativa >}} Retornar a posição da primeira ocorrência de um elemento. {{< /alternativa >}}
{{< alternativa >}} Adicionar um elemento à lista. {{< /alternativa >}}
{{< alternativa >}} Remover um elemento da lista. {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `index()` retorna o índice da primeira ocorrência do elemento informado.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
frutas = ["maçã", "banana", "laranja"]

print(frutas.index("laranja"))
{{< /code >}}

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< solucao letra="C" >}}
`"laranja"` está na posição de índice 2.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = [30, 10, 40, 20]

numeros.sort()

print(numeros)
{{< /code >}}

{{< alternativa >}} [30, 10, 40, 20] {{< /alternativa >}}
{{< alternativa >}} [10, 20, 30, 40] {{< /alternativa >}}
{{< alternativa >}} [40, 30, 20, 10] {{< /alternativa >}}
{{< alternativa >}} [20, 40, 10, 30] {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `sort()` ordena os elementos da lista em ordem crescente por padrão.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método pode ser utilizado para ordenar uma lista diretamente?

{{< alternativa >}} `order()` {{< /alternativa >}}
{{< alternativa >}} `sort()` {{< /alternativa >}}
{{< alternativa >}} `organize()` {{< /alternativa >}}
{{< alternativa >}} `arrange()` {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `sort()` ordena os elementos da própria lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = [1, 2, 3, 4, 5]

for numero in numeros:
    print(numero)
{{< /code >}}

{{< alternativa >}} Apenas o primeiro número {{< /alternativa >}}
{{< alternativa >}} Os números 1, 2, 3, 4 e 5, um por linha {{< /alternativa >}}
{{< alternativa >}} Apenas o número 5 {{< /alternativa >}}
{{< alternativa >}} Nada será impresso {{< /alternativa >}}
{{< solucao letra="B" >}}
O `for` percorre os elementos da lista, atribuindo cada elemento à variável `numero` e executando o `print`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = [2, 4, 6, 8]

for numero in numeros:
    if numero > 5:
        print(numero)
{{< /code >}}

{{< alternativa >}} 2 e 4 {{< /alternativa >}}
{{< alternativa >}} 4 e 6 {{< /alternativa >}}
{{< alternativa >}} 6 e 8 {{< /alternativa >}}
{{< alternativa >}} 2, 4, 6 e 8 {{< /alternativa >}}
{{< solucao letra="C" >}}
Durante a repetição, somente os elementos maiores que 5 são impressos: 6 e 8.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = [10, 20, 30]

for i in range(len(numeros)):
    print(numeros[i])
{{< /code >}}

{{< alternativa >}} Apenas 10 {{< /alternativa >}}
{{< alternativa >}} 10, 20 e 30 {{< /alternativa >}}
{{< alternativa >}} 0, 1 e 2 {{< /alternativa >}}
{{< alternativa >}} Será gerado um erro {{< /alternativa >}}
{{< solucao letra="B" >}}
`range(len(numeros))` gera os índices 0, 1 e 2, que são utilizados para acessar os elementos da lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = [10, 20, 30, 40]

print(numeros[1:3])
{{< /code >}}

{{< alternativa >}} [10, 20] {{< /alternativa >}}
{{< alternativa >}} [20, 30] {{< /alternativa >}}
{{< alternativa >}} [20, 30, 40] {{< /alternativa >}}
{{< alternativa >}} [10, 20, 30] {{< /alternativa >}}
{{< solucao letra="B" >}}
O fatiamento `[1:3]` começa no índice 1 e termina antes do índice 3, resultando em `[20, 30]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = [10, 20, 30, 40, 50]

print(numeros[:3])
{{< /code >}}

{{< alternativa >}} [10, 20, 30] {{< /alternativa >}}
{{< alternativa >}} [20, 30, 40] {{< /alternativa >}}
{{< alternativa >}} [30, 40, 50] {{< /alternativa >}}
{{< alternativa >}} [10, 20, 30, 40] {{< /alternativa >}}
{{< solucao letra="A" >}}
Quando o início não é informado, o fatiamento começa no primeiro elemento. O índice 3 não é incluído.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = [10, 20, 30, 40, 50]

print(numeros[2:])
{{< /code >}}

{{< alternativa >}} [10, 20] {{< /alternativa >}}
{{< alternativa >}} [20, 30, 40] {{< /alternativa >}}
{{< alternativa >}} [30, 40, 50] {{< /alternativa >}}
{{< alternativa >}} [30, 40] {{< /alternativa >}}
{{< solucao letra="C" >}}
Quando o final não é informado, o fatiamento vai até o final da lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = [1, 2, 3]

copia = numeros

copia.append(4)

print(numeros)
{{< /code >}}

{{< alternativa >}} [1, 2, 3] {{< /alternativa >}}
{{< alternativa >}} [1, 2, 3, 4] {{< /alternativa >}}
{{< alternativa >}} [4] {{< /alternativa >}}
{{< alternativa >}} Será gerado um erro {{< /alternativa >}}
{{< solucao letra="B" >}}
A atribuição `copia = numeros` faz as duas variáveis referenciarem a mesma lista. Por isso, a alteração feita por `copia` também aparece em `numeros`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual das alternativas cria uma lista vazia?

{{< alternativa >}} `lista = ()` {{< /alternativa >}}
{{< alternativa >}} `lista = {}` {{< /alternativa >}}
{{< alternativa >}} `lista = []` {{< /alternativa >}}
{{< alternativa >}} `lista = ""` {{< /alternativa >}}
{{< solucao letra="C" >}}
Os colchetes `[]` são utilizados para criar uma lista vazia.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
lista = []

lista.append("Python")
lista.append("Java")
lista.append("C")

print(len(lista))
{{< /code >}}

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< solucao letra="D" >}}
Foram adicionados três elementos à lista, portanto seu tamanho é 3.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = [5, 10, 15, 20]

total = 0

for numero in numeros:
    total += numero

print(total)
{{< /code >}}

{{< alternativa >}} 30 {{< /alternativa >}}
{{< alternativa >}} 40 {{< /alternativa >}}
{{< alternativa >}} 50 {{< /alternativa >}}
{{< alternativa >}} 50.0 {{< /alternativa >}}
{{< solucao letra="C" >}}
A soma dos elementos é `5 + 10 + 15 + 20`, resultando em 50.
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

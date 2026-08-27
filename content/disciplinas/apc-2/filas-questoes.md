---
title: "Questões sobre Filas"
description: "Questões sobre a implementação de filas utilizando listas em Python"
slug: filas-questoes
tags:
- python
- filas
- questões
---

{{< lista-questoes >}}

{{< questao >}}
O que é uma fila em uma estrutura de dados?

{{< alternativa >}} Uma estrutura em que o último elemento inserido é o primeiro a sair. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura em que o primeiro elemento inserido é o primeiro a sair. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que não permite remover elementos. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que armazena apenas números. {{< /alternativa >}}
{{< solucao letra="B" >}}
Uma fila segue o princípio FIFO (First In, First Out): o primeiro elemento inserido é o primeiro a ser removido.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que significa FIFO?

{{< alternativa >}} First In, First Out. {{< /alternativa >}}
{{< alternativa >}} First In, Final Out. {{< /alternativa >}}
{{< alternativa >}} Fast In, Fast Out. {{< /alternativa >}}
{{< alternativa >}} Final In, First Out. {{< /alternativa >}}
{{< solucao letra="A" >}}
FIFO significa First In, First Out, ou seja, primeiro a entrar, primeiro a sair.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere uma fila representada pela lista abaixo:

{{< code >}}
fila = [10, 20, 30, 40]
{{< /code >}}

Qual é o primeiro elemento da fila?

{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 30 {{< /alternativa >}}
{{< alternativa >}} 40 {{< /alternativa >}}
{{< solucao letra="A" >}}
Em uma fila implementada com uma lista, o primeiro elemento da lista representa o primeiro elemento da fila.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere uma fila inicialmente vazia. Qual comando deve ser utilizado para adicionar o elemento `10` ao final da fila?

{{< alternativa >}} `fila.insert(0, 10)` {{< /alternativa >}}
{{< alternativa >}} `fila.append(10)` {{< /alternativa >}}
{{< alternativa >}} `fila.pop(10)` {{< /alternativa >}}
{{< alternativa >}} `fila.remove(10)` {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `append()` adiciona um elemento ao final da lista, sendo adequado para representar a entrada de um elemento na fila.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual comando pode ser utilizado para remover o primeiro elemento de uma fila implementada com uma lista?

{{< alternativa >}} `fila.pop()` {{< /alternativa >}}
{{< alternativa >}} `fila.pop(0)` {{< /alternativa >}}
{{< alternativa >}} `fila.remove()` {{< /alternativa >}}
{{< alternativa >}} `fila.delete(0)` {{< /alternativa >}}
{{< solucao letra="B" >}}
`pop(0)` remove e retorna o elemento que está no índice 0, ou seja, o primeiro elemento da fila.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
fila = []

fila.append(10)
fila.append(20)
fila.append(30)

print(fila)
{{< /code >}}

{{< alternativa >}} [30, 20, 10] {{< /alternativa >}}
{{< alternativa >}} [10, 20, 30] {{< /alternativa >}}
{{< alternativa >}} [10, 30, 20] {{< /alternativa >}}
{{< alternativa >}} [] {{< /alternativa >}}
{{< solucao letra="B" >}}
Cada `append()` adiciona um elemento ao final da lista. Portanto, a fila fica `[10, 20, 30]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
fila = [10, 20, 30]

elemento = fila.pop(0)

print(elemento)
{{< /code >}}

{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 30 {{< /alternativa >}}
{{< alternativa >}} 0 {{< /alternativa >}}
{{< solucao letra="A" >}}
`pop(0)` remove e retorna o elemento que está na primeira posição da lista. Portanto, o resultado é 10.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
fila = [10, 20, 30]

fila.pop(0)

print(fila)
{{< /code >}}

{{< alternativa >}} [10, 20, 30] {{< /alternativa >}}
{{< alternativa >}} [20, 30] {{< /alternativa >}}
{{< alternativa >}} [10, 30] {{< /alternativa >}}
{{< alternativa >}} [30] {{< /alternativa >}}
{{< solucao letra="B" >}}
`pop(0)` remove o primeiro elemento, que é 10. Os elementos restantes são 20 e 30.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere a fila inicialmente vazia. Analise as operações abaixo.

{{< code >}}
fila = []

fila.append("Ana")
fila.append("Bruno")
fila.append("Carlos")

fila.pop(0)
{{< /code >}}

Qual pessoa será removida da fila?

{{< alternativa >}} Ana {{< /alternativa >}}
{{< alternativa >}} Bruno {{< /alternativa >}}
{{< alternativa >}} Carlos {{< /alternativa >}}
{{< alternativa >}} Nenhuma pessoa {{< /alternativa >}}
{{< solucao letra="A" >}}
Ana foi a primeira pessoa adicionada à fila. Como a fila segue FIFO, ela será a primeira a sair.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere a fila abaixo:

{{< code >}}
fila = ["Ana", "Bruno", "Carlos", "Daniel"]
{{< /code >}}

Se for executado `fila.pop(0)` duas vezes, quais elementos serão removidos?

{{< alternativa >}} Ana e Bruno {{< /alternativa >}}
{{< alternativa >}} Bruno e Carlos {{< /alternativa >}}
{{< alternativa >}} Carlos e Daniel {{< /alternativa >}}
{{< alternativa >}} Daniel e Carlos {{< /alternativa >}}
{{< solucao letra="A" >}}
A primeira execução remove Ana e a segunda remove Bruno, pois os elementos saem pela frente da fila.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
fila = [10, 20, 30]

fila.append(40)
fila.pop(0)

print(fila)
{{< /code >}}

{{< alternativa >}} [10, 20, 30, 40] {{< /alternativa >}}
{{< alternativa >}} [20, 30, 40] {{< /alternativa >}}
{{< alternativa >}} [40, 20, 30] {{< /alternativa >}}
{{< alternativa >}} [10, 20, 40] {{< /alternativa >}}
{{< solucao letra="B" >}}
O `append(40)` adiciona 40 ao final. Depois, `pop(0)` remove 10. A fila fica `[20, 30, 40]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual alternativa representa corretamente as operações de uma fila implementada utilizando uma lista?

{{< alternativa >}} Adicionar no início com `insert()` e remover no final com `pop()`. {{< /alternativa >}}
{{< alternativa >}} Adicionar no final com `append()` e remover no início com `pop(0)`. {{< /alternativa >}}
{{< alternativa >}} Adicionar no início com `append()` e remover no início com `pop()`. {{< /alternativa >}}
{{< alternativa >}} Adicionar no final com `insert()` e remover no final com `pop(0)`. {{< /alternativa >}}
{{< solucao letra="B" >}}
Uma forma simples de implementar uma fila com `list` é utilizar `append()` para adicionar elementos ao final e `pop(0)` para remover elementos do início.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
fila = []

fila.append(1)
fila.append(2)
fila.append(3)

print(fila.pop(0))
print(fila.pop(0))
{{< /code >}}

{{< alternativa >}} 1 e 2 {{< /alternativa >}}
{{< alternativa >}} 2 e 3 {{< /alternativa >}}
{{< alternativa >}} 3 e 2 {{< /alternativa >}}
{{< alternativa >}} 1 e 3 {{< /alternativa >}}
{{< solucao letra="A" >}}
Os elementos entram na ordem 1, 2 e 3. As duas operações `pop(0)` removem primeiro 1 e depois 2.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o conteúdo final da fila.

{{< code >}}
fila = []

fila.append("A")
fila.append("B")
fila.append("C")

fila.pop(0)

fila.append("D")
{{< /code >}}

{{< alternativa >}} ["A", "B", "C", "D"] {{< /alternativa >}}
{{< alternativa >}} ["B", "C", "D"] {{< /alternativa >}}
{{< alternativa >}} ["D", "B", "C"] {{< /alternativa >}}
{{< alternativa >}} ["C", "D"] {{< /alternativa >}}
{{< solucao letra="B" >}}
O primeiro `pop(0)` remove `"A"`. Depois, `"D"` é adicionado ao final da fila. O resultado é `["B", "C", "D"]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
fila = [10, 20, 30]

if len(fila) > 0:
    print("Fila possui elementos")
else:
    print("Fila vazia")
{{< /code >}}

{{< alternativa >}} Fila possui elementos {{< /alternativa >}}
{{< alternativa >}} Fila vazia {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} Nada será impresso {{< /alternativa >}}
{{< solucao letra="A" >}}
A lista possui três elementos, portanto `len(fila) > 0` é verdadeiro.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
fila = []

if len(fila) > 0:
    print("Fila possui elementos")
else:
    print("Fila vazia")
{{< /code >}}

{{< alternativa >}} Fila possui elementos {{< /alternativa >}}
{{< alternativa >}} Fila vazia {{< /alternativa >}}
{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} Nada será impresso {{< /alternativa >}}
{{< solucao letra="B" >}}
A lista está vazia, portanto `len(fila)` é 0 e a condição é falsa.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual código verifica corretamente se uma fila está vazia?

{{< alternativa >}} `if fila == 0:` {{< /alternativa >}}
{{< alternativa >}} `if len(fila) == 0:` {{< /alternativa >}}
{{< alternativa >}} `if fila.length == 0:` {{< /alternativa >}}
{{< alternativa >}} `if fila.empty():` {{< /alternativa >}}
{{< solucao letra="B" >}}
A função `len()` retorna a quantidade de elementos da lista. Portanto, `len(fila) == 0` verifica se a fila está vazia.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
fila = [10, 20, 30, 40]

print(len(fila))
{{< /code >}}

{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 40 {{< /alternativa >}}
{{< solucao letra="B" >}}
A fila possui quatro elementos, portanto `len(fila)` retorna 4.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere uma fila inicialmente vazia. Analise o código.

{{< code >}}
fila = []

for i in range(5):
    fila.append(i)

print(fila)
{{< /code >}}

{{< alternativa >}} [1, 2, 3, 4, 5] {{< /alternativa >}}
{{< alternativa >}} [0, 1, 2, 3, 4] {{< /alternativa >}}
{{< alternativa >}} [0, 1, 2, 3, 4, 5] {{< /alternativa >}}
{{< alternativa >}} [5, 4, 3, 2, 1] {{< /alternativa >}}
{{< solucao letra="B" >}}
`range(5)` produz os valores de 0 até 4. Cada valor é adicionado ao final da fila.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere uma fila inicialmente vazia. Analise o código.

{{< code >}}
fila = []

for i in range(5):
    fila.append(i)

for i in range(5):
    print(fila.pop(0))
{{< /code >}}

Qual será a ordem dos elementos impressos?

{{< alternativa >}} 4, 3, 2, 1, 0 {{< /alternativa >}}
{{< alternativa >}} 0, 1, 2, 3, 4 {{< /alternativa >}}
{{< alternativa >}} 1, 2, 3, 4, 5 {{< /alternativa >}}
{{< alternativa >}} 0, 2, 4, 1, 3 {{< /alternativa >}}
{{< solucao letra="B" >}}
Os elementos são inseridos na ordem 0, 1, 2, 3 e 4. Como `pop(0)` remove sempre o primeiro elemento, eles são removidos nessa mesma ordem.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Uma fila possui os elementos abaixo:

{{< code >}}
fila = ["Ana", "Bruno", "Carlos"]
{{< /code >}}

Qual será o conteúdo da fila depois de executar:

{{< code >}}
fila.pop(0)
fila.append("Daniel")
{{< /code >}}

{{< alternativa >}} ["Ana", "Bruno", "Carlos", "Daniel"] {{< /alternativa >}}
{{< alternativa >}} ["Bruno", "Carlos", "Daniel"] {{< /alternativa >}}
{{< alternativa >}} ["Daniel", "Bruno", "Carlos"] {{< /alternativa >}}
{{< alternativa >}} ["Carlos", "Daniel"] {{< /alternativa >}}
{{< solucao letra="B" >}}
`pop(0)` remove `"Ana"` e `append("Daniel")` adiciona `"Daniel"` ao final. A fila fica `["Bruno", "Carlos", "Daniel"]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
fila = [10, 20, 30]

primeiro = fila.pop(0)

print(primeiro)
print(fila)
{{< /code >}}

{{< alternativa >}} 10 e [10, 20, 30] {{< /alternativa >}}
{{< alternativa >}} 10 e [20, 30] {{< /alternativa >}}
{{< alternativa >}} 20 e [10, 30] {{< /alternativa >}}
{{< alternativa >}} 30 e [10, 20] {{< /alternativa >}}
{{< solucao letra="B" >}}
`pop(0)` retorna o primeiro elemento, 10, e também o remove da lista. Por isso, a fila passa a ser `[20, 30]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual das alternativas abaixo implementa corretamente uma operação para adicionar uma pessoa ao final de uma fila?

{{< alternativa >}} `fila.pop(0)` {{< /alternativa >}}
{{< alternativa >}} `fila.remove(0)` {{< /alternativa >}}
{{< alternativa >}} `fila.append(pessoa)` {{< /alternativa >}}
{{< alternativa >}} `fila.pop()` {{< /alternativa >}}
{{< solucao letra="C" >}}
`append()` adiciona o novo elemento ao final da lista, que representa o final da fila.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual das alternativas abaixo implementa corretamente uma operação para atender a primeira pessoa de uma fila?

{{< alternativa >}} `fila.append(0)` {{< /alternativa >}}
{{< alternativa >}} `fila.pop()` {{< /alternativa >}}
{{< alternativa >}} `fila.pop(0)` {{< /alternativa >}}
{{< alternativa >}} `fila.insert(0)` {{< /alternativa >}}
{{< solucao letra="C" >}}
A primeira pessoa está no índice 0. Portanto, `pop(0)` remove e retorna o primeiro elemento da fila.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
fila = ["A", "B", "C"]

while len(fila) > 0:
    print(fila.pop(0))
{{< /code >}}

{{< alternativa >}} A, B e C, nessa ordem {{< /alternativa >}}
{{< alternativa >}} C, B e A, nessa ordem {{< /alternativa >}}
{{< alternativa >}} Apenas A {{< /alternativa >}}
{{< alternativa >}} O programa entra em um loop infinito {{< /alternativa >}}
{{< solucao letra="A" >}}
Enquanto a fila não estiver vazia, `pop(0)` remove seu primeiro elemento. Assim, os elementos são impressos na ordem A, B e C.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere uma fila de atendimento representada por uma lista. Qual código atende todas as pessoas da fila até que ela fique vazia?

{{< alternativa >}} `while fila: fila.append()` {{< /alternativa >}}
{{< alternativa >}} `while len(fila) > 0: fila.pop(0)` {{< /alternativa >}}
{{< alternativa >}} `while len(fila) == 0: fila.pop()` {{< /alternativa >}}
{{< alternativa >}} `for fila: pop(0)` {{< /alternativa >}}
{{< solucao letra="B" >}}
O `while` continua enquanto existem elementos na fila e `pop(0)` remove cada elemento pela frente.
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

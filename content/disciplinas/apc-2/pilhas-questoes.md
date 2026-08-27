---
title: "Questões sobre Pilhas"
description: "Questões sobre a estrutura de dados pilha em Python"
slug: pilhas-questoes
tags:
- python
- pilhas
- questões
---

{{< lista-questoes >}}

{{< questao >}}
O que é uma pilha em uma estrutura de dados?

{{< alternativa >}} Uma estrutura em que o primeiro elemento inserido é o primeiro a sair. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura em que o último elemento inserido é o primeiro a sair. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que não permite remover elementos. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que permite remover qualquer elemento sem regras. {{< /alternativa >}}
{{< solucao letra="B" >}}
Uma pilha segue o princípio LIFO (Last In, First Out): o último elemento inserido é o primeiro a ser removido.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que significa LIFO?

{{< alternativa >}} Last In, First Out. {{< /alternativa >}}
{{< alternativa >}} Last In, Final Out. {{< /alternativa >}}
{{< alternativa >}} Last Item, First Object. {{< /alternativa >}}
{{< alternativa >}} First In, First Out. {{< /alternativa >}}
{{< solucao letra="A" >}}
LIFO significa Last In, First Out, ou seja, último a entrar, primeiro a sair.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual situação do cotidiano representa melhor o funcionamento de uma pilha?

{{< alternativa >}} Pessoas aguardando atendimento em uma fila. {{< /alternativa >}}
{{< alternativa >}} Uma pilha de pratos. {{< /alternativa >}}
{{< alternativa >}} Pessoas entrando em um ônibus por ordem de chegada. {{< /alternativa >}}
{{< alternativa >}} Uma agenda organizada por data. {{< /alternativa >}}
{{< solucao letra="B" >}}
Em uma pilha de pratos, normalmente o último prato colocado é o primeiro a ser retirado, seguindo o princípio LIFO.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere uma pilha inicialmente vazia. Após inserir os elementos `10`, `20` e `30`, qual elemento deverá ser removido primeiro?

{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 30 {{< /alternativa >}}
{{< alternativa >}} Nenhum elemento {{< /alternativa >}}
{{< solucao letra="C" >}}
O elemento 30 foi o último a ser inserido. Como a pilha segue o princípio LIFO, ele será o primeiro a sair.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Em uma pilha, onde um novo elemento normalmente é inserido?

{{< alternativa >}} No início da pilha. {{< /alternativa >}}
{{< alternativa >}} No final da pilha. {{< /alternativa >}}
{{< alternativa >}} Em qualquer posição. {{< /alternativa >}}
{{< alternativa >}} No meio da pilha. {{< /alternativa >}}
{{< solucao letra="B" >}}
Uma pilha possui uma única extremidade utilizada para inserção e remoção. Em uma implementação com lista, essa extremidade pode ser representada pelo final da lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Em uma pilha implementada utilizando uma lista, qual método pode ser utilizado para adicionar um elemento?

{{< alternativa >}} `append()` {{< /alternativa >}}
{{< alternativa >}} `remove()` {{< /alternativa >}}
{{< alternativa >}} `pop()` {{< /alternativa >}}
{{< alternativa >}} `clear()` {{< /alternativa >}}
{{< solucao letra="A" >}}
O método `append()` adiciona um elemento ao final da lista, que pode representar o topo da pilha.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Em uma pilha implementada utilizando uma lista, qual método pode ser utilizado para remover o elemento do topo?

{{< alternativa >}} `append()` {{< /alternativa >}}
{{< alternativa >}} `remove()` {{< /alternativa >}}
{{< alternativa >}} `pop()` {{< /alternativa >}}
{{< alternativa >}} `insert()` {{< /alternativa >}}
{{< solucao letra="C" >}}
O método `pop()` remove e retorna o último elemento da lista, que pode representar o topo da pilha.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
pilha = []

pilha.append(10)
pilha.append(20)
pilha.append(30)

print(pilha)
{{< /code >}}

{{< alternativa >}} [30, 20, 10] {{< /alternativa >}}
{{< alternativa >}} [10, 20, 30] {{< /alternativa >}}
{{< alternativa >}} [10, 30, 20] {{< /alternativa >}}
{{< alternativa >}} [] {{< /alternativa >}}
{{< solucao letra="B" >}}
Cada `append()` adiciona um elemento ao final da lista. Portanto, a pilha fica `[10, 20, 30]`, sendo 30 o elemento do topo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
pilha = [10, 20, 30]

elemento = pilha.pop()

print(elemento)
{{< /code >}}

{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 30 {{< /alternativa >}}
{{< alternativa >}} 0 {{< /alternativa >}}
{{< solucao letra="C" >}}
`pop()` sem argumentos remove e retorna o último elemento da lista. Nesse caso, o elemento é 30.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
pilha = [10, 20, 30]

pilha.pop()

print(pilha)
{{< /code >}}

{{< alternativa >}} [10, 20, 30] {{< /alternativa >}}
{{< alternativa >}} [20, 30] {{< /alternativa >}}
{{< alternativa >}} [10, 20] {{< /alternativa >}}
{{< alternativa >}} [30] {{< /alternativa >}}
{{< solucao letra="C" >}}
`pop()` remove o último elemento da lista, que é 30. A pilha passa a ser `[10, 20]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere a pilha inicialmente vazia. Analise as operações abaixo.

{{< code >}}
pilha = []

pilha.append("A")
pilha.append("B")
pilha.append("C")

pilha.pop()
{{< /code >}}

Qual elemento será removido?

{{< alternativa >}} A {{< /alternativa >}}
{{< alternativa >}} B {{< /alternativa >}}
{{< alternativa >}} C {{< /alternativa >}}
{{< alternativa >}} Nenhum elemento {{< /alternativa >}}
{{< solucao letra="C" >}}
"C" foi o último elemento inserido e está no topo da pilha. Portanto, será o primeiro a ser removido.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere a pilha abaixo:

{{< code >}}
pilha = [10, 20, 30, 40]
{{< /code >}}

Qual elemento está no topo da pilha?

{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 30 {{< /alternativa >}}
{{< alternativa >}} 40 {{< /alternativa >}}
{{< solucao letra="D" >}}
Em uma pilha implementada com `list`, o final da lista pode representar o topo da pilha. Nesse caso, o topo é 40.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
pilha = [10, 20, 30]

pilha.append(40)
pilha.pop()

print(pilha)
{{< /code >}}

{{< alternativa >}} [10, 20, 30] {{< /alternativa >}}
{{< alternativa >}} [20, 30, 40] {{< /alternativa >}}
{{< alternativa >}} [10, 20, 40] {{< /alternativa >}}
{{< alternativa >}} [40, 10, 20, 30] {{< /alternativa >}}
{{< solucao letra="A" >}}
40 é adicionado ao topo e imediatamente removido pelo `pop()`. A pilha volta a ser `[10, 20, 30]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
pilha = []

pilha.append(1)
pilha.append(2)
pilha.append(3)

print(pilha.pop())
print(pilha.pop())
{{< /code >}}

{{< alternativa >}} 1 e 2 {{< /alternativa >}}
{{< alternativa >}} 2 e 3 {{< /alternativa >}}
{{< alternativa >}} 3 e 2 {{< /alternativa >}}
{{< alternativa >}} 3 e 1 {{< /alternativa >}}
{{< solucao letra="C" >}}
A pilha fica `[1, 2, 3]`. O primeiro `pop()` remove 3 e o segundo remove 2.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere a pilha abaixo:

{{< code >}}
pilha = ["A", "B", "C", "D"]
{{< /code >}}

Se dois elementos forem removidos utilizando `pop()`, quais elementos serão removidos?

{{< alternativa >}} A e B {{< /alternativa >}}
{{< alternativa >}} B e C {{< /alternativa >}}
{{< alternativa >}} C e D {{< /alternativa >}}
{{< alternativa >}} D e C {{< /alternativa >}}
{{< solucao letra="D" >}}
O topo da pilha é `"D"`. O primeiro `pop()` remove D e o segundo remove C.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere uma pilha inicialmente vazia. Analise o código.

{{< code >}}
pilha = []

pilha.append("A")
pilha.append("B")
pilha.pop()
pilha.append("C")

print(pilha)
{{< /code >}}

{{< alternativa >}} ["A", "B", "C"] {{< /alternativa >}}
{{< alternativa >}} ["A", "C"] {{< /alternativa >}}
{{< alternativa >}} ["B", "C"] {{< /alternativa >}}
{{< alternativa >}} ["C", "A"] {{< /alternativa >}}
{{< solucao letra="B" >}}
A pilha fica `["A", "B"]`. O `pop()` remove B. Depois, C é inserido no topo. O resultado é `["A", "C"]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual alternativa representa corretamente as operações de uma pilha implementada utilizando uma lista?

{{< alternativa >}} Adicionar no início com `insert()` e remover no final com `pop()`. {{< /alternativa >}}
{{< alternativa >}} Adicionar no final com `append()` e remover do final com `pop()`. {{< /alternativa >}}
{{< alternativa >}} Adicionar no início com `append()` e remover do início com `pop()`. {{< /alternativa >}}
{{< alternativa >}} Adicionar no final com `append()` e remover do início com `pop(0)`. {{< /alternativa >}}
{{< solucao letra="B" >}}
Uma forma simples de implementar uma pilha com `list` é utilizar `append()` para inserir elementos no final e `pop()` para remover elementos do final.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a principal diferença entre uma pilha e uma fila?

{{< alternativa >}} A pilha utiliza FIFO e a fila utiliza LIFO. {{< /alternativa >}}
{{< alternativa >}} A pilha utiliza LIFO e a fila utiliza FIFO. {{< /alternativa >}}
{{< alternativa >}} Ambas utilizam FIFO. {{< /alternativa >}}
{{< alternativa >}} Ambas utilizam LIFO. {{< /alternativa >}}
{{< solucao letra="B" >}}
A pilha segue o princípio LIFO, enquanto a fila segue o princípio FIFO.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
pilha = [10, 20, 30]

if len(pilha) > 0:
    print("Pilha possui elementos")
else:
    print("Pilha vazia")
{{< /code >}}

{{< alternativa >}} Pilha possui elementos {{< /alternativa >}}
{{< alternativa >}} Pilha vazia {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} Nada será impresso {{< /alternativa >}}
{{< solucao letra="A" >}}
A lista possui três elementos, portanto `len(pilha) > 0` é verdadeiro.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
pilha = []

if len(pilha) > 0:
    print("Pilha possui elementos")
else:
    print("Pilha vazia")
{{< /code >}}

{{< alternativa >}} Pilha possui elementos {{< /alternativa >}}
{{< alternativa >}} Pilha vazia {{< /alternativa >}}
{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} Nada será impresso {{< /alternativa >}}
{{< solucao letra="B" >}}
A lista está vazia, portanto `len(pilha)` é 0 e a condição é falsa.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual código verifica corretamente se uma pilha está vazia?

{{< alternativa >}} `if pilha == 0:` {{< /alternativa >}}
{{< alternativa >}} `if len(pilha) == 0:` {{< /alternativa >}}
{{< alternativa >}} `if pilha.length == 0:` {{< /alternativa >}}
{{< alternativa >}} `if pilha.empty():` {{< /alternativa >}}
{{< solucao letra="B" >}}
A função `len()` retorna a quantidade de elementos da lista. Portanto, `len(pilha) == 0` verifica se a pilha está vazia.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
pilha = []

for i in range(5):
    pilha.append(i)

print(pilha)
{{< /code >}}

{{< alternativa >}} [1, 2, 3, 4, 5] {{< /alternativa >}}
{{< alternativa >}} [0, 1, 2, 3, 4] {{< /alternativa >}}
{{< alternativa >}} [0, 1, 2, 3, 4, 5] {{< /alternativa >}}
{{< alternativa >}} [5, 4, 3, 2, 1] {{< /alternativa >}}
{{< solucao letra="B" >}}
`range(5)` produz os valores de 0 até 4. Cada valor é adicionado ao topo da pilha.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique a ordem em que os elementos serão impressos.

{{< code >}}
pilha = []

for i in range(5):
    pilha.append(i)

while len(pilha) > 0:
    print(pilha.pop())
{{< /code >}}

{{< alternativa >}} 0, 1, 2, 3, 4 {{< /alternativa >}}
{{< alternativa >}} 4, 3, 2, 1, 0 {{< /alternativa >}}
{{< alternativa >}} 1, 2, 3, 4, 5 {{< /alternativa >}}
{{< alternativa >}} 5, 4, 3, 2, 1 {{< /alternativa >}}
{{< solucao letra="B" >}}
Os elementos são inseridos na ordem 0, 1, 2, 3 e 4. Como `pop()` remove sempre o último elemento, eles serão removidos na ordem inversa: 4, 3, 2, 1 e 0.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere uma pilha de números representada por uma lista. Qual código remove todos os elementos da pilha até que ela fique vazia?

{{< alternativa >}} `while len(pilha) > 0: pilha.pop()` {{< /alternativa >}}
{{< alternativa >}} `while len(pilha) == 0: pilha.append()` {{< /alternativa >}}
{{< alternativa >}} `for pilha: pop()` {{< /alternativa >}}
{{< alternativa >}} `while pilha: pilha.append()` {{< /alternativa >}}
{{< solucao letra="A" >}}
Enquanto a pilha possuir elementos, `pop()` remove o elemento que está no topo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
pilha = [10, 20, 30, 40]

topo = pilha[-1]

print(topo)
{{< /code >}}

{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 30 {{< /alternativa >}}
{{< alternativa >}} 40 {{< /alternativa >}}
{{< solucao letra="D" >}}
O índice `-1` representa o último elemento da lista. Como o topo da pilha está no final da lista, o resultado é 40.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
pilha = [1, 2, 3]

elemento = pilha.pop()

print(elemento)
print(len(pilha))
{{< /code >}}

{{< alternativa >}} 1 e 3 {{< /alternativa >}}
{{< alternativa >}} 3 e 2 {{< /alternativa >}}
{{< alternativa >}} 2 e 3 {{< /alternativa >}}
{{< alternativa >}} 3 e 3 {{< /alternativa >}}
{{< solucao letra="B" >}}
O `pop()` remove e retorna o último elemento, que é 3. Depois da remoção, permanecem dois elementos na pilha.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Uma pilha possui os elementos abaixo:

{{< code >}}
pilha = ["A", "B", "C", "D"]
{{< /code >}}

Após executar três vezes `pop()`, qual será o conteúdo da pilha?

{{< alternativa >}} ["A"] {{< /alternativa >}}
{{< alternativa >}} ["D"] {{< /alternativa >}}
{{< alternativa >}} ["A", "B", "C"] {{< /alternativa >}}
{{< alternativa >}} [] {{< /alternativa >}}
{{< solucao letra="A" >}}
Os três elementos do topo, D, C e B, serão removidos. Restará apenas A.
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

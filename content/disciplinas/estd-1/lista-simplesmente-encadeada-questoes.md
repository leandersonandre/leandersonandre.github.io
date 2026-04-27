---
title: "Questões sobre Lista Simplesmente Encadeada"
description: "Questões sobre Lista Simplesmente Encadeada"
slug: lista-simplesmente-encadeada-questoes
tags:
  - estruturas-de-dados
  - questões
  - linked-list
---

{{< questao >}}
O que caracteriza uma lista simplesmente encadeada?
{{< alternativa >}} Elementos armazenados em posições contíguas na memória {{< /alternativa >}}
{{< alternativa >}} Elementos conectados por ponteiros (referências) entre nós {{< /alternativa >}}
{{< alternativa >}} Elementos organizados automaticamente em ordem crescente {{< /alternativa >}}
{{< alternativa >}} Estrutura que não utiliza memória dinâmica {{< /alternativa >}}
{{< solucao letra="B" >}}
Uma lista simplesmente encadeada é formada por nós conectados por referências (ponteiros), sem necessidade de memória contígua.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que cada nó de uma lista simplesmente encadeada armazena?
{{< alternativa >}} Apenas um índice e um valor {{< /alternativa >}}
{{< alternativa >}} Um valor e uma referência para o nó anterior {{< /alternativa >}}
{{< alternativa >}} Um valor e uma referência para o próximo nó {{< /alternativa >}}
{{< alternativa >}} Apenas um valor numérico fixo {{< /alternativa >}}
{{< solucao letra="C" >}}
Cada nó armazena um valor e uma referência (ponteiro) para o próximo nó da lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é o papel do ponteiro "inicio" em uma lista simplesmente encadeada?
{{< alternativa >}} Apontar para o último elemento {{< /alternativa >}}
{{< alternativa >}} Apontar para um elemento aleatório {{< /alternativa >}}
{{< alternativa >}} Apontar para o primeiro elemento da lista {{< /alternativa >}}
{{< alternativa >}} Apontar para o elemento do meio {{< /alternativa >}}
{{< solucao letra="C" >}}
O ponteiro inicio sempre aponta para o primeiro nó da lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é o papel do ponteiro "fim" na lista simplesmente encadeada?
{{< alternativa >}} Apontar para o primeiro elemento {{< /alternativa >}}
{{< alternativa >}} Apontar para o último elemento {{< /alternativa >}}
{{< alternativa >}} Apontar para o elemento nulo sempre {{< /alternativa >}}
{{< alternativa >}} Apontar para o segundo elemento {{< /alternativa >}}
{{< solucao letra="B" >}}
O ponteiro fim aponta diretamente para o último nó da lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Após executar a operação abaixo, qual será o estado da lista?

{{< code >}}
Lista vazia
adicionarInicio(20)
adicionarInicio(10)
{{< /code >}}

{{< alternativa >}} [20, 10] {{< /alternativa >}}
{{< alternativa >}} [10, 20] {{< /alternativa >}}
{{< alternativa >}} [10] {{< /alternativa >}}
{{< alternativa >}} [20] {{< /alternativa >}}
{{< solucao letra="B" >}}
O último inserido no início vira o primeiro da lista, resultando em [10, 20].
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a complexidade da operação adicionarFim quando há ponteiro fim?
{{< alternativa >}} O(n) {{< /alternativa >}}
{{< alternativa >}} O(log n) {{< /alternativa >}}
{{< alternativa >}} O(1) {{< /alternativa >}}
{{< alternativa >}} O(n²) {{< /alternativa >}}
{{< solucao letra="C" >}}
Com o ponteiro fim, a inserção no final é feita em tempo constante O(1).
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece ao remover o primeiro elemento da lista?
{{< alternativa >}} O ponteiro fim é sempre removido {{< /alternativa >}}
{{< alternativa >}} O ponteiro inicio é atualizado para o próximo nó {{< /alternativa >}}
{{< alternativa >}} A lista é completamente apagada {{< /alternativa >}}
{{< alternativa >}} A ordem dos elementos é invertida {{< /alternativa >}}
{{< solucao letra="B" >}}
Ao remover o início, o ponteiro inicio passa a apontar para o próximo nó.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que ocorre quando removemos o último elemento da lista?
{{< alternativa >}} O ponteiro inicio é sempre perdido {{< /alternativa >}}
{{< alternativa >}} A lista é duplicada {{< /alternativa >}}
{{< alternativa >}} É necessário percorrer a lista até o penúltimo nó {{< /alternativa >}}
{{< alternativa >}} A operação é O(1) sempre {{< /alternativa >}}
{{< solucao letra="C" >}}
Para remover o fim, é necessário percorrer a lista até o penúltimo nó.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Após executar o código abaixo, qual será o elemento na posição 2?

{{< code >}}
Lista: 10 -> 20 -> 30 -> 40
obter(2)
{{< /code >}}

{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 30 {{< /alternativa >}}
{{< alternativa >}} 40 {{< /alternativa >}}
{{< solucao letra="C" >}}
O índice 2 corresponde ao terceiro elemento, que é 30.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece na operação inserir(indice, valor) em uma lista encadeada?
{{< alternativa >}} O array é redimensionado {{< /alternativa >}}
{{< alternativa >}} Os nós são reorganizados por ordenação automática {{< /alternativa >}}
{{< alternativa >}} A lista é percorrida até a posição e os ponteiros são ajustados {{< /alternativa >}}
{{< alternativa >}} O elemento substitui sempre o primeiro nó {{< /alternativa >}}
{{< solucao letra="C" >}}
A lista é percorrida até a posição desejada e os ponteiros são ajustados para inserir o novo nó.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Após executar a operação abaixo, qual será o estado final da lista?

{{< code >}}
Lista: 10 -> 20 -> 30
remover(1)
{{< /code >}}

{{< alternativa >}} 10 -> 20 -> 30 {{< /alternativa >}}
{{< alternativa >}} 10 -> 30 {{< /alternativa >}}
{{< alternativa >}} 20 -> 30 {{< /alternativa >}}
{{< alternativa >}} 10 -> 20 {{< /alternativa >}}
{{< solucao letra="B" >}}
O elemento da posição 1 (20) é removido e o nó anterior aponta para o próximo (30).
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual operação tem custo O(n) em uma lista simplesmente encadeada?
{{< alternativa >}} adicionarInicio {{< /alternativa >}}
{{< alternativa >}} obterInicio {{< /alternativa >}}
{{< alternativa >}} adicionarFim (com ponteiro fim) {{< /alternativa >}}
{{< alternativa >}} removerFim {{< /alternativa >}}
{{< solucao letra="D" >}}
Remover o fim exige percorrer a lista até o penúltimo nó, resultando em O(n).
{{< /solucao >}}
{{< /questao >}}

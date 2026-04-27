---
title: "Questões sobre Lista baseada em Arranjos"
description: "Questões sobre Lista baseada em Arranjos"
slug: lista-baseada-em-arranjos-questoes
tags:

- estruturas-de-dados
- arraylist
- questões

---


{{< questao >}}
O que caracteriza uma lista baseada em arranjo?
{{< alternativa >}} Uma estrutura que não usa memória contínua {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que utiliza um array interno para armazenar elementos sequenciais {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que só permite inserção no início {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que não permite atualização de valores {{< /alternativa >}}
{{< solucao letra="B" >}}
A lista baseada em arranjo utiliza um array interno para armazenar elementos de forma sequencial.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece quando uma lista baseada em arranjo atinge sua capacidade máxima?
{{< alternativa >}} Ela impede qualquer nova inserção permanentemente {{< /alternativa >}}
{{< alternativa >}} Ela apaga elementos antigos automaticamente {{< /alternativa >}}
{{< alternativa >}} Ela cria um novo array maior e copia os elementos {{< /alternativa >}}
{{< alternativa >}} Ela converte automaticamente para lista encadeada {{< /alternativa >}}
{{< solucao letra="C" >}}
Quando atinge a capacidade, a lista realiza redimensionamento criando um novo array maior e copiando os elementos.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece com os elementos após uma inserção no meio da lista?
{{< alternativa >}} Os elementos são removidos para abrir espaço {{< /alternativa >}}
{{< alternativa >}} Os elementos são deslocados para a direita {{< /alternativa >}}
{{< alternativa >}} A lista perde a ordem dos elementos {{< /alternativa >}}
{{< alternativa >}} A lista é reinicializada {{< /alternativa >}}
{{< solucao letra="B" >}}
Na inserção no meio, os elementos à direita são deslocados para a direita para abrir espaço.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Após executar a operação abaixo, qual será o estado da lista?

{{< code >}}
Lista: [10, 20, 30]
inserir(1, 99)
{{< /code >}}

{{< alternativa >}} [10, 20, 30, 99] {{< /alternativa >}}
{{< alternativa >}} [99, 10, 20, 30] {{< /alternativa >}}
{{< alternativa >}} [10, 99, 20, 30] {{< /alternativa >}}
{{< alternativa >}} [10, 20, 99] {{< /alternativa >}}
{{< solucao letra="C" >}}
O valor 99 é inserido na posição 1 e os elementos são deslocados para a direita.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece após remover um elemento do meio da lista?
{{< alternativa >}} Os elementos à direita são deslocados para a esquerda {{< /alternativa >}}
{{< alternativa >}} A lista cresce automaticamente {{< /alternativa >}}
{{< alternativa >}} O elemento permanece marcado como nulo {{< /alternativa >}}
{{< alternativa >}} A lista perde sua estrutura interna {{< /alternativa >}}
{{< solucao letra="A" >}}
Após remoção, os elementos à direita são deslocados para manter a continuidade da lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Após executar o código abaixo, qual será o conteúdo final da lista?

{{< code >}}
Lista: [5, 10, 15, 20]
remover(2)
{{< /code >}}

{{< alternativa >}} [5, 10, 20] {{< /alternativa >}}
{{< alternativa >}} [5, 15, 20] {{< /alternativa >}}
{{< alternativa >}} [10, 15, 20] {{< /alternativa >}}
{{< alternativa >}} [5, 10, 15, 20] {{< /alternativa >}}
{{< solucao letra="A" >}}
O elemento na posição 2 (15) é removido e os demais são deslocados.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que a variável "tamanho" representa em uma lista baseada em arranjo?
{{< alternativa >}} A capacidade total do array {{< /alternativa >}}
{{< alternativa >}} O número de elementos realmente armazenados {{< /alternativa >}}
{{< alternativa >}} O número de operações realizadas {{< /alternativa >}}
{{< alternativa >}} O índice máximo possível {{< /alternativa >}}
{{< solucao letra="B" >}}
A variável tamanho indica quantos elementos estão realmente armazenados na lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que será impresso após a execução abaixo?

{{< code >}}
Lista: [10, 20, 30]
atualizar(1, 99)
obter(1)
{{< /code >}}

{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 99 {{< /alternativa >}}
{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
O elemento na posição 1 é atualizado para 99, então esse valor é retornado.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual operação é mais eficiente em uma lista baseada em arranjo?
{{< alternativa >}} Inserção no meio {{< /alternativa >}}
{{< alternativa >}} Remoção no início {{< /alternativa >}}
{{< alternativa >}} Acesso por índice {{< /alternativa >}}
{{< alternativa >}} Redimensionamento {{< /alternativa >}}
{{< solucao letra="C" >}}
O acesso por índice é O(1), sendo a operação mais eficiente.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é o custo do redimensionamento da lista?
{{< alternativa >}} O(1) {{< /alternativa >}}
{{< alternativa >}} O(log n) {{< /alternativa >}}
{{< alternativa >}} O(n) {{< /alternativa >}}
{{< alternativa >}} O(n²) {{< /alternativa >}}
{{< solucao letra="C" >}}
O redimensionamento exige copiar todos os elementos, resultando em O(n).
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece com os elementos após a operação abaixo?

{{< code >}}
Lista: [10, 20, 30, 40]
inserir(2, 99)
{{< /code >}}

{{< alternativa >}} [10, 20, 99, 30, 40] {{< /alternativa >}}
{{< alternativa >}} [10, 99, 20, 30, 40] {{< /alternativa >}}
{{< alternativa >}} [99, 10, 20, 30, 40] {{< /alternativa >}}
{{< alternativa >}} [10, 20, 30, 40] {{< /alternativa >}}
{{< solucao letra="A" >}}
O valor 99 é inserido na posição 2 e os elementos são deslocados para a direita.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Em uma lista baseada em arranjo, qual é a diferença entre "capacidade" e "tamanho"?
{{< alternativa >}} Capacidade é o número de elementos usados e tamanho é o limite máximo {{< /alternativa >}}
{{< alternativa >}} Capacidade é o limite máximo do array e tamanho é a quantidade de elementos armazenados {{< /alternativa >}}
{{< alternativa >}} Capacidade e tamanho sempre representam a mesma coisa {{< /alternativa >}}
{{< alternativa >}} Capacidade é dinâmica e tamanho é fixo {{< /alternativa >}}
{{< solucao letra="B" >}}
Capacidade é o limite máximo que o array interno suporta, enquanto o tamanho indica quantos elementos estão realmente armazenados na lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece quando o tamanho de uma lista baseada em arranjo atinge sua capacidade?
{{< alternativa >}} A lista impede novas inserções permanentemente {{< /alternativa >}}
{{< alternativa >}} O tamanho diminui automaticamente {{< /alternativa >}}
{{< alternativa >}} O array interno é redimensionado para um maior {{< /alternativa >}}
{{< alternativa >}} O último elemento é removido automaticamente {{< /alternativa >}}
{{< solucao letra="C" >}}
Quando o tamanho atinge a capacidade, a lista precisa ser redimensionada criando um novo array maior.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Se uma lista tem capacidade 10 e tamanho 6, o que isso significa?
{{< alternativa >}} Existem 10 elementos armazenados e 6 espaços livres {{< /alternativa >}}
{{< alternativa >}} Existem 6 elementos armazenados e 4 espaços livres {{< /alternativa >}}
{{< alternativa >}} A lista está cheia {{< /alternativa >}}
{{< alternativa >}} A lista está vazia {{< /alternativa >}}
{{< solucao letra="B" >}}
Capacidade 10 significa espaço total de 10 posições, e tamanho 6 indica 6 elementos armazenados, restando 4 vagas livres.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Após a operação abaixo, qual é o tamanho da lista?

{{< code >}}
Lista capacidade: 5
Adicionar: 10, 20, 30
{{< /code >}}

{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 0 {{< /alternativa >}}
{{< solucao letra="C" >}}
Foram adicionados 3 elementos, então o tamanho da lista é 3.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual afirmação é correta sobre tamanho em uma lista baseada em arranjo?
{{< alternativa >}} Representa sempre a capacidade total do array {{< /alternativa >}}
{{< alternativa >}} Indica quantos elementos válidos estão armazenados {{< /alternativa >}}
{{< alternativa >}} É sempre igual ao número de posições livres {{< /alternativa >}}
{{< alternativa >}} Não pode ser alterado após criação {{< /alternativa >}}
{{< solucao letra="B" >}}
O tamanho indica quantos elementos reais estão armazenados na estrutura.
{{< /solucao >}}
{{< /questao >}}

---
title: "Questões sobre Lista Encadeada Circular"
description: "Estrutura de dados linear onde o último nó aponta novamente para o primeiro, formando um ciclo"
slug: lista-encadeada-circular-questoes
tags: estruturas-de-dados, questões, java, circular-linked-list
---

{{< questao >}}
Qual é a principal característica de uma lista encadeada circular?
{{< alternativa >}} O último nó aponta para null {{< /alternativa >}}
{{< alternativa >}} O último nó aponta para o primeiro nó {{< /alternativa >}}
{{< alternativa >}} Os nós são armazenados em array contínuo {{< /alternativa >}}
{{< alternativa >}} Não possui ponteiros entre os nós {{< /alternativa >}}
{{< solucao letra="B" >}}
Na lista circular, o último nó aponta novamente para o primeiro, formando um ciclo contínuo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece se não houver controle de parada ao percorrer uma lista circular?
{{< alternativa >}} A lista termina automaticamente {{< /alternativa >}}
{{< alternativa >}} O programa entra em loop infinito {{< /alternativa >}}
{{< alternativa >}} Os elementos são apagados {{< /alternativa >}}
{{< alternativa >}} A lista vira um array {{< /alternativa >}}
{{< solucao letra="B" >}}
Como não existe null no final, sem controle de parada o percurso se repete indefinidamente.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual condição é usada corretamente para parar o percurso em uma lista circular?
{{< alternativa >}} parar quando atual == null {{< /alternativa >}}
{{< alternativa >}} parar quando atual == fim {{< /alternativa >}}
{{< alternativa >}} parar quando atual == inicio novamente {{< /alternativa >}}
{{< alternativa >}} parar quando tamanho == 0 {{< /alternativa >}}
{{< solucao letra="C" >}}
O percurso deve parar quando o nó atual retorna ao início.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Após executar o código abaixo, qual é a estrutura formada?

{{< code >}}
adicionarFim(10)
adicionarFim(20)
adicionarFim(30)
{{< /code >}}

{{< alternativa >}} 10 -> 20 -> 30 -> null {{< /alternativa >}}
{{< alternativa >}} 10 -> 20 -> 30 -> 10 (ciclo) {{< /alternativa >}}
{{< alternativa >}} 30 -> 20 -> 10 -> null {{< /alternativa >}}
{{< alternativa >}} 10 -> null -> 20 -> 30 {{< /alternativa >}}
{{< solucao letra="B" >}}
Na lista circular, o último elemento aponta novamente para o primeiro.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece ao adicionar um elemento em uma lista circular vazia?
{{< alternativa >}} O elemento aponta para null {{< /alternativa >}}
{{< alternativa >}} O elemento aponta para ele mesmo {{< /alternativa >}}
{{< alternativa >}} O elemento é descartado {{< /alternativa >}}
{{< alternativa >}} A lista não aceita inserção {{< /alternativa >}}
{{< solucao letra="B" >}}
Em uma lista circular com um único elemento, ele aponta para si mesmo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual operação pode ser mais custosa em uma lista circular simplesmente encadeada?
{{< alternativa >}} adicionarInicio {{< /alternativa >}}
{{< alternativa >}} obterInicio {{< /alternativa >}}
{{< alternativa >}} removerFim {{< /alternativa >}}
{{< alternativa >}} percorrer até o início {{< /alternativa >}}
{{< solucao letra="C" >}}
Remover o fim exige percorrer a lista para encontrar o penúltimo nó.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é o principal cuidado ao implementar percorrer() em lista circular?
{{< alternativa >}} Evitar usar ponteiros {{< /alternativa >}}
{{< alternativa >}} Não acessar o primeiro elemento {{< /alternativa >}}
{{< alternativa >}} Evitar loop infinito {{< /alternativa >}}
{{< alternativa >}} Converter para array antes {{< /alternativa >}}
{{< solucao letra="C" >}}
É necessário controlar a parada para evitar loop infinito.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual estrutura permite melhor suporte a repetição contínua de elementos?
{{< alternativa >}} Array simples {{< /alternativa >}}
{{< alternativa >}} Lista simplesmente encadeada {{< /alternativa >}}
{{< alternativa >}} Lista circular {{< /alternativa >}}
{{< alternativa >}} Pilha {{< /alternativa >}}
{{< solucao letra="C" >}}
A lista circular permite navegação contínua sem fim.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece com o ponteiro fim em uma lista circular?
{{< alternativa >}} Ele aponta para null {{< /alternativa >}}
{{< alternativa >}} Ele aponta para o início {{< /alternativa >}}
{{< alternativa >}} Ele não existe {{< /alternativa >}}
{{< alternativa >}} Ele aponta para o elemento anterior ao início {{< /alternativa >}}
{{< solucao letra="B" >}}
O fim sempre aponta de volta para o início, fechando o ciclo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a vantagem de uma lista circular em relação a uma lista simplesmente encadeada?
{{< alternativa >}} Menor uso de memória sempre {{< /alternativa >}}
{{< alternativa >}} Elimina necessidade de ponteiro inicio {{< /alternativa >}}
{{< alternativa >}} Permite navegação contínua dos elementos {{< /alternativa >}}
{{< alternativa >}} Não precisa de nós {{< /alternativa >}}
{{< solucao letra="C" >}}
A principal vantagem é permitir navegação contínua sem fim definido.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que ocorre quando percorremos uma lista circular e encontramos novamente o inicio?
{{< alternativa >}} A lista termina automaticamente {{< /alternativa >}}
{{< alternativa >}} O percurso deve ser interrompido {{< /alternativa >}}
{{< alternativa >}} Os elementos são duplicados {{< /alternativa >}}
{{< alternativa >}} A lista se transforma em lista linear {{< /alternativa >}}
{{< solucao letra="B" >}}
Quando volta ao início, o percurso deve ser interrompido para evitar repetição infinita.
{{< /solucao >}}
{{< /questao >}}

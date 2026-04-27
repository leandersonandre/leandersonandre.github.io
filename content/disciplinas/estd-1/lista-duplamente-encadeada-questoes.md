---
title: "Questões sobre Lista Duplamente Encadeada"
description: "Estrutura de dados linear formada por nós conectados sequencialmente com ponteiros para próximo e anterior"
slug: lista-duplamente-encadeada-questoes
tags: estruturas-de-dados,  questões, java, doubly-linked-list
---

{{< questao >}}
O que caracteriza uma lista duplamente encadeada?
{{< alternativa >}} Cada nó aponta apenas para o próximo elemento {{< /alternativa >}}
{{< alternativa >}} Cada nó aponta para o próximo e para o anterior {{< /alternativa >}}
{{< alternativa >}} Os elementos são armazenados em array contínuo {{< /alternativa >}}
{{< alternativa >}} Os nós não possuem conexões entre si {{< /alternativa >}}
{{< solucao letra="B" >}}
Na lista duplamente encadeada, cada nó possui referências para o próximo e o anterior, permitindo navegação em ambos os sentidos.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a principal vantagem da lista duplamente encadeada em relação à simplesmente encadeada?
{{< alternativa >}} Menor uso de memória {{< /alternativa >}}
{{< alternativa >}} Não utiliza ponteiros {{< /alternativa >}}
{{< alternativa >}} Permite navegação em ambos os sentidos {{< /alternativa >}}
{{< alternativa >}} Não precisa de nós {{< /alternativa >}}
{{< solucao letra="C" >}}
A principal vantagem é permitir navegação bidirecional (para frente e para trás).
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece ao remover o último elemento usando o ponteiro "fim"?
{{< alternativa >}} É necessário percorrer toda a lista {{< /alternativa >}}
{{< alternativa >}} O ponteiro anterior do fim é usado para atualização direta {{< /alternativa >}}
{{< alternativa >}} O elemento não pode ser removido {{< /alternativa >}}
{{< alternativa >}} A lista é convertida em array {{< /alternativa >}}
{{< solucao letra="B" >}}
O ponteiro anterior do último nó permite atualizar o fim diretamente, sem percorrer a lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Após executar a operação abaixo, qual será o estado da lista?

{{< code >}}
Lista: 10 <-> 20 <-> 30
adicionarInicio(5)
{{< /code >}}

{{< alternativa >}} 10 <-> 20 <-> 30 <-> 5 {{< /alternativa >}}
{{< alternativa >}} 5 <-> 10 <-> 20 <-> 30 {{< /alternativa >}}
{{< alternativa >}} 20 <-> 30 <-> 5 <-> 10 {{< /alternativa >}}
{{< alternativa >}} 5 <-> 30 <-> 20 <-> 10 {{< /alternativa >}}
{{< solucao letra="B" >}}
O elemento 5 é inserido no início da lista, tornando-se o primeiro nó.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece com os ponteiros ao inserir um elemento no meio da lista?
{{< alternativa >}} Apenas o ponteiro proximo é alterado {{< /alternativa >}}
{{< alternativa >}} Apenas o ponteiro anterior é alterado {{< /alternativa >}}
{{< alternativa >}} Ambos os ponteiros (proximo e anterior) são ajustados {{< /alternativa >}}
{{< alternativa >}} Nenhum ponteiro é alterado {{< /alternativa >}}
{{< solucao letra="C" >}}
Na inserção no meio, tanto o ponteiro proximo quanto o anterior são ajustados para manter a ligação correta.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Após a operação abaixo, qual será o resultado?

{{< code >}}
Lista: 10 <-> 20 <-> 30 <-> 40
remover(2)
{{< /code >}}

{{< alternativa >}} 10 <-> 20 <-> 30 <-> 40 {{< /alternativa >}}
{{< alternativa >}} 10 <-> 30 <-> 40 {{< /alternativa >}}
{{< alternativa >}} 10 <-> 20 <-> 40 {{< /alternativa >}}
{{< alternativa >}} 20 <-> 30 <-> 40 {{< /alternativa >}}
{{< solucao letra="C" >}}
O elemento da posição 2 (30) é removido e os ponteiros dos vizinhos são ajustados.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual operação é O(1) em uma lista duplamente encadeada?
{{< alternativa >}} obter(indice) {{< /alternativa >}}
{{< alternativa >}} inserir no meio {{< /alternativa >}}
{{< alternativa >}} removerFim {{< /alternativa >}}
{{< alternativa >}} percorrer {{< /alternativa >}}
{{< solucao letra="C" >}}
Com o ponteiro fim e anterior, removerFim é O(1) na lista duplamente encadeada.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece ao percorrer uma lista duplamente encadeada usando apenas proximo?
{{< alternativa >}} A lista perde elementos {{< /alternativa >}}
{{< alternativa >}} O percurso ocorre normalmente do início ao fim {{< /alternativa >}}
{{< alternativa >}} O percurso falha sempre {{< /alternativa >}}
{{< alternativa >}} A lista se torna ordenada automaticamente {{< /alternativa >}}
{{< solucao letra="B" >}}
Usando apenas o ponteiro proximo, a lista é percorrida normalmente do início ao fim.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual estrutura de nó é usada em uma lista duplamente encadeada?
{{< alternativa >}} Apenas valor e índice {{< /alternativa >}}
{{< alternativa >}} Valor, próximo e anterior {{< /alternativa >}}
{{< alternativa >}} Apenas valor e próximo {{< /alternativa >}}
{{< alternativa >}} Apenas ponteiro para início {{< /alternativa >}}
{{< solucao letra="B" >}}
O nó contém valor, referência para o próximo e para o anterior.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Após executar o código abaixo, qual será o elemento na posição 1?

{{< code >}}
Lista: 10 <-> 20 <-> 30
inserir(1, 99)
{{< /code >}}

{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 99 {{< /alternativa >}}
{{< alternativa >}} 30 {{< /alternativa >}}
{{< solucao letra="C" >}}
O valor 99 é inserido na posição 1, deslocando os demais elementos.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é o impacto do ponteiro anterior na lista duplamente encadeada?
{{< alternativa >}} Aumenta a complexidade de todas as operações para O(n²) {{< /alternativa >}}
{{< alternativa >}} Permite remoção eficiente sem percorrer toda a lista {{< /alternativa >}}
{{< alternativa >}} Elimina a necessidade de ponteiro inicio {{< /alternativa >}}
{{< alternativa >}} Impede inserções no meio da lista {{< /alternativa >}}
{{< solucao letra="B" >}}
O ponteiro anterior permite remover nós sem necessidade de percorrer toda a lista.
{{< /solucao >}}
{{< /questao >}}

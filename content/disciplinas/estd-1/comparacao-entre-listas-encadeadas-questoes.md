---
title: "Questões sobre a diferença entre Listas Encadeadas Simples, Duplas e Circulares"
description: "Comparação entre Listas Encadeadas Simples, Duplas e Circulares"
slug: comparacao-entre-listas-encadeadas-questoes
tags:
  - estruturas-de-dados
  - questões
  - linked-list
---


{{< questao >}}
Qual é a principal diferença entre uma lista simplesmente encadeada e uma lista duplamente encadeada?
{{< alternativa >}} A simplesmente encadeada usa array e a duplamente usa ponteiros {{< /alternativa >}}
{{< alternativa >}} A simplesmente encadeada possui apenas referência para o próximo nó, enquanto a duplamente possui próximo e anterior {{< /alternativa >}}
{{< alternativa >}} A duplamente encadeada não permite remoção {{< /alternativa >}}
{{< alternativa >}} A simplesmente encadeada não possui nós {{< /alternativa >}}
{{< solucao letra="B" >}}
A lista simplesmente encadeada possui apenas ponteiro para o próximo nó, enquanto a duplamente encadeada também possui ponteiro para o nó anterior.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual estrutura permite navegação em ambos os sentidos (ida e volta)?
{{< alternativa >}} Lista simplesmente encadeada {{< /alternativa >}}
{{< alternativa >}} Lista circular simplesmente encadeada {{< /alternativa >}}
{{< alternativa >}} Lista duplamente encadeada {{< /alternativa >}}
{{< alternativa >}} Array estático {{< /alternativa >}}
{{< solucao letra="C" >}}
A lista duplamente encadeada permite navegação nos dois sentidos graças ao ponteiro anterior.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a principal característica da lista encadeada circular?
{{< alternativa >}} O último nó aponta para null {{< /alternativa >}}
{{< alternativa >}} O último nó aponta para o primeiro nó {{< /alternativa >}}
{{< alternativa >}} Os nós são armazenados em memória contínua {{< /alternativa >}}
{{< alternativa >}} Não possui ponteiros entre os nós {{< /alternativa >}}
{{< solucao letra="B" >}}
Na lista circular, o último nó aponta novamente para o primeiro, formando um ciclo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual estrutura NÃO possui um fim “null”?
{{< alternativa >}} Lista simplesmente encadeada {{< /alternativa >}}
{{< alternativa >}} Lista duplamente encadeada {{< /alternativa >}}
{{< alternativa >}} Lista circular {{< /alternativa >}}
{{< alternativa >}} Array {{< /alternativa >}}
{{< solucao letra="C" >}}
A lista circular não possui fim nulo, pois o último nó aponta para o início.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual lista permite remover o último elemento em O(1), assumindo ponteiro anterior?
{{< alternativa >}} Lista simplesmente encadeada {{< /alternativa >}}
{{< alternativa >}} Lista duplamente encadeada {{< /alternativa >}}
{{< alternativa >}} Lista circular simplesmente encadeada {{< /alternativa >}}
{{< alternativa >}} Array estático {{< /alternativa >}}
{{< solucao letra="B" >}}
A lista duplamente encadeada permite acesso direto ao anterior do último nó, tornando a remoção O(1).
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual estrutura exige percorrer a lista para remover o último elemento?
{{< alternativa >}} Lista duplamente encadeada {{< /alternativa >}}
{{< alternativa >}} Lista circular duplamente encadeada {{< /alternativa >}}
{{< alternativa >}} Lista simplesmente encadeada {{< /alternativa >}}
{{< alternativa >}} Array dinâmico {{< /alternativa >}}
{{< solucao letra="C" >}}
Na lista simplesmente encadeada, não há referência ao nó anterior, então é necessário percorrer até o penúltimo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual estrutura é mais eficiente para navegação sequencial simples (apenas para frente)?
{{< alternativa >}} Lista duplamente encadeada {{< /alternativa >}}
{{< alternativa >}} Lista simplesmente encadeada {{< /alternativa >}}
{{< alternativa >}} Lista circular duplamente encadeada {{< /alternativa >}}
{{< alternativa >}} Hash table {{< /alternativa >}}
{{< solucao letra="B" >}}
A lista simplesmente encadeada é suficiente e mais leve para navegação apenas para frente.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual estrutura exige mais memória por nó?
{{< alternativa >}} Lista simplesmente encadeada {{< /alternativa >}}
{{< alternativa >}} Lista duplamente encadeada {{< /alternativa >}}
{{< alternativa >}} Lista circular simplesmente encadeada {{< /alternativa >}}
{{< alternativa >}} Array estático {{< /alternativa >}}
{{< solucao letra="B" >}}
A lista duplamente encadeada usa dois ponteiros (próximo e anterior), consumindo mais memória.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual estrutura pode causar loop infinito se não houver controle de parada?
{{< alternativa >}} Lista simplesmente encadeada {{< /alternativa >}}
{{< alternativa >}} Lista duplamente encadeada {{< /alternativa >}}
{{< alternativa >}} Lista circular {{< /alternativa >}}
{{< alternativa >}} Array estático {{< /alternativa >}}
{{< solucao letra="C" >}}
A lista circular pode gerar loop infinito por não possuir fim nulo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual alternativa descreve corretamente a principal diferença entre lista circular e lista simplesmente encadeada?
{{< alternativa >}} A circular não usa nós {{< /alternativa >}}
{{< alternativa >}} A simplesmente encadeada não usa ponteiros {{< /alternativa >}}
{{< alternativa >}} A circular não possui null no final {{< /alternativa >}}
{{< alternativa >}} A simplesmente encadeada é bidirecional {{< /alternativa >}}
{{< solucao letra="C" >}}
Na lista circular, o último nó aponta para o primeiro, eliminando o null no final.
{{< /solucao >}}
{{< /questao >}}

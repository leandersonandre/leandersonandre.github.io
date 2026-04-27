---
title: "Questões sobre Arranjo Ordenado"
description: "Questões sobre Arranjo Ordenado"
slug: arranjo-ordenado-questoes
tags:

- estruturas-de-dados
- arrays
- ordenação
- questões

---


{{< questao >}}
O que caracteriza um arranjo ordenado?
{{< alternativa >}} Elementos armazenados em ordem aleatória {{< /alternativa >}}
{{< alternativa >}} Elementos sempre armazenados em ordem crescente ou decrescente {{< /alternativa >}}
{{< alternativa >}} Elementos armazenados em diferentes tipos de dados {{< /alternativa >}}
{{< alternativa >}} Elementos sem necessidade de organização {{< /alternativa >}}
{{< solucao letra="B" >}}
Um arranjo ordenado mantém seus elementos sempre organizados, geralmente em ordem crescente ou decrescente.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a principal vantagem de um arranjo ordenado?
{{< alternativa >}} Inserção mais rápida {{< /alternativa >}}
{{< alternativa >}} Uso menor de memória {{< /alternativa >}}
{{< alternativa >}} Busca mais eficiente, podendo usar busca binária {{< /alternativa >}}
{{< alternativa >}} Permite tipos diferentes de dados {{< /alternativa >}}
{{< solucao letra="C" >}}
A principal vantagem é a eficiência nas buscas, permitindo o uso de busca binária.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece com os elementos após inserir um valor em um arranjo ordenado?
{{< alternativa >}} Eles permanecem na mesma posição sempre {{< /alternativa >}}
{{< alternativa >}} O arranjo perde a ordenação {{< /alternativa >}}
{{< alternativa >}} Elementos maiores podem ser deslocados para manter a ordem {{< /alternativa >}}
{{< alternativa >}} O array é recriado do zero {{< /alternativa >}}
{{< solucao letra="C" >}}
Ao inserir, elementos maiores são deslocados para manter a ordenação correta.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Após inserir o valor 25 no arranjo abaixo, qual será o estado final?

{{< code >}}
Antes: [10, 20, 30, _, _]
Inserir: 25
{{< /code >}}

{{< alternativa >}} [10, 20, 25, 30, _] {{< /alternativa >}}
{{< alternativa >}} [25, 10, 20, 30, _] {{< /alternativa >}}
{{< alternativa >}} [10, 20, 30, 25, _] {{< /alternativa >}}
{{< alternativa >}} [10, 25, 20, 30, _] {{< /alternativa >}}
{{< solucao letra="A" >}}
O valor 25 é inserido na posição correta mantendo a ordem crescente.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Após remover o valor 20 do arranjo abaixo, qual será o resultado?

{{< code >}}
Antes: [10, 20, 30, 40]
Remover: 20
{{< /code >}}

{{< alternativa >}} [10, 30, 40] {{< /alternativa >}}
{{< alternativa >}} [10, 20, 30] {{< /alternativa >}}
{{< alternativa >}} [10, 30, 40, 20] {{< /alternativa >}}
{{< alternativa >}} [10, 40, 30] {{< /alternativa >}}
{{< solucao letra="A" >}}
O elemento 20 é removido e os demais são deslocados para manter a sequência.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece com os elementos após a remoção em um arranjo ordenado?
{{< alternativa >}} Os elementos são apagados sem ajuste {{< /alternativa >}}
{{< alternativa >}} Os elementos à direita são deslocados para a esquerda {{< /alternativa >}}
{{< alternativa >}} O arranjo perde a ordenação {{< /alternativa >}}
{{< alternativa >}} O arranjo dobra de tamanho {{< /alternativa >}}
{{< solucao letra="B" >}}
Após a remoção, os elementos são deslocados para manter a continuidade do arranjo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Após inserir os valores 50 e 20 em um arranjo ordenado inicialmente vazio, qual será o estado final?

{{< code >}}
Inserir: 50, depois 20
{{< /code >}}

{{< alternativa >}} [50, 20] {{< /alternativa >}}
{{< alternativa >}} [20, 50] {{< /alternativa >}}
{{< alternativa >}} [50] {{< /alternativa >}}
{{< alternativa >}} [20] {{< /alternativa >}}
{{< solucao letra="B" >}}
Mesmo inserindo 50 primeiro, ao inserir 20 o arranjo é reorganizado para manter a ordem crescente.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que ocorre se um valor maior que todos os elementos for inserido em um arranjo ordenado crescente?
{{< alternativa >}} Ele é inserido no início {{< /alternativa >}}
{{< alternativa >}} Ele substitui o maior elemento {{< /alternativa >}}
{{< alternativa >}} Ele é inserido no final sem deslocamentos {{< /alternativa >}}
{{< alternativa >}} Ocorre erro de execução {{< /alternativa >}}
{{< solucao letra="C" >}}
Quando o valor é maior que todos os existentes, ele é inserido no final do arranjo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual operação é necessária para manter a ordem ao inserir um elemento em um arranjo ordenado?
{{< alternativa >}} Troca de variáveis simples {{< /alternativa >}}
{{< alternativa >}} Deslocamento de elementos {{< /alternativa >}}
{{< alternativa >}} Recriação do array {{< /alternativa >}}
{{< alternativa >}} Ordenação por seleção após inserção {{< /alternativa >}}
{{< solucao letra="B" >}}
Para manter a ordem, é necessário deslocar os elementos maiores para abrir espaço.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Sobre o estado do arranjo após a operação abaixo, o que é correto afirmar?

{{< code >}}
[5, 10, 20, 30]
remover(10)
{{< /code >}}

{{< alternativa >}} O arranjo vira [5, 20, 30] e mantém ordem {{< /alternativa >}}
{{< alternativa >}} O arranjo vira [5, 30, 20] {{< /alternativa >}}
{{< alternativa >}} O elemento 10 continua no array {{< /alternativa >}}
{{< alternativa >}} O arranjo fica desordenado {{< /alternativa >}}
{{< solucao letra="A" >}}
Após remover 10, os elementos são deslocados e a ordem é mantida.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Em um arranjo ordenado, o método de busca abaixo retorna o índice de um elemento encontrado. Se o valor existir mais de uma vez no arranjo, o que ele retorna?

{{< code >}}
[10, 20, 20, 20, 30]
buscar(20)
{{< /code >}}

{{< alternativa >}} Retorna todos os índices onde o valor aparece {{< /alternativa >}}
{{< alternativa >}} Retorna sempre o último índice do valor {{< /alternativa >}}
{{< alternativa >}} Retorna sempre o primeiro índice encontrado {{< /alternativa >}}
{{< alternativa >}} Retorna -1, pois há repetição {{< /alternativa >}}
{{< solucao letra="C" >}}
A busca padrão (como a binária ou linear simples mostrada) retorna apenas a primeira ocorrência encontrada do valor. Para retornar todas as ocorrências seria necessário um algoritmo específico de varredura completa.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que será retornado ao buscar o valor 25 no arranjo abaixo usando busca binária?

{{< code >}}
[10, 15, 20, 30, 40]
buscar(25)
{{< /code >}}

{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} -1 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< solucao letra="C" >}}
O valor 25 não existe no arranjo, então a busca retorna -1 indicando “não encontrado”.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
No arranjo abaixo, qual índice será retornado ao buscar o valor 20 usando busca binária?

{{< code >}}
[10, 20, 20, 20, 30]
buscar(20)
{{< /code >}}

{{< alternativa >}} Pode retornar 1 {{< /alternativa >}}
{{< alternativa >}} Sempre retorna 3 {{< /alternativa >}}
{{< alternativa >}} Sempre retorna 2 {{< /alternativa >}}
{{< alternativa >}} Sempre retorna -1 {{< /alternativa >}}
{{< solucao letra="A" >}}
A busca binária retorna um índice onde o valor foi encontrado. Dependendo da implementação, pode retornar qualquer ocorrência, mas neste caso típico retorna a primeira encontrada durante a execução, como o índice 1.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece se o valor procurado for menor que o primeiro elemento em um arranjo ordenado?

{{< code >}}
[10, 20, 30, 40]
buscar(5)
{{< /code >}}

{{< alternativa >}} Retorna 0 {{< /alternativa >}}
{{< alternativa >}} Retorna o último índice {{< /alternativa >}}
{{< alternativa >}} Retorna -1 imediatamente ou após poucas comparações {{< /alternativa >}}
{{< alternativa >}} O arranjo é reorganizado {{< /alternativa >}}
{{< solucao letra="C" >}}
Como o arranjo é ordenado, a busca percebe rapidamente que o valor não pode existir e retorna -1.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a principal diferença ao buscar em um arranjo com valores repetidos?

{{< alternativa >}} A busca sempre falha {{< /alternativa >}}
{{< alternativa >}} A busca retorna todos os índices automaticamente {{< /alternativa >}}
{{< alternativa >}} A busca retorna apenas uma ocorrência do valor {{< /alternativa >}}
{{< alternativa >}} A busca deixa de funcionar corretamente {{< /alternativa >}}
{{< solucao letra="C" >}}
As buscas padrão retornam apenas uma ocorrência do valor, mesmo que existam duplicatas no arranjo.
{{< /solucao >}}
{{< /questao >}}



{{< questao >}}
Qual é a complexidade da busca binária em um arranjo ordenado?
{{< alternativa >}} O(1) {{< /alternativa >}}
{{< alternativa >}} O(n) {{< /alternativa >}}
{{< alternativa >}} O(log n) {{< /alternativa >}}
{{< alternativa >}} O(n²) {{< /alternativa >}}
{{< solucao letra="C" >}}
A busca binária tem complexidade O(log n), pois reduz o espaço de busca pela metade a cada iteração.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a complexidade da busca linear em um arranjo ordenado no pior caso?
{{< alternativa >}} O(1) {{< /alternativa >}}
{{< alternativa >}} O(log n) {{< /alternativa >}}
{{< alternativa >}} O(n) {{< /alternativa >}}
{{< alternativa >}} O(n²) {{< /alternativa >}}
{{< solucao letra="C" >}}
Mesmo com a otimização de parada antecipada, no pior caso a busca linear percorre todos os elementos, resultando em O(n).
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a complexidade da inserção em um arranjo ordenado no pior caso?
{{< alternativa >}} O(1) {{< /alternativa >}}
{{< alternativa >}} O(log n) {{< /alternativa >}}
{{< alternativa >}} O(n) {{< /alternativa >}}
{{< alternativa >}} O(n²) {{< /alternativa >}}
{{< solucao letra="C" >}}
A inserção pode exigir deslocamento de todos os elementos, resultando em O(n).
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a complexidade da remoção em um arranjo ordenado no pior caso?
{{< alternativa >}} O(1) {{< /alternativa >}}
{{< alternativa >}} O(log n) {{< /alternativa >}}
{{< alternativa >}} O(n) {{< /alternativa >}}
{{< alternativa >}} O(n²) {{< /alternativa >}}
{{< solucao letra="C" >}}
A remoção exige deslocamento dos elementos à direita ou à esquerda, resultando em O(n).
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual operação tem melhor desempenho em um arranjo ordenado quando o objetivo é apenas consulta?
{{< alternativa >}} Inserção {{< /alternativa >}}
{{< alternativa >}} Remoção {{< /alternativa >}}
{{< alternativa >}} Busca binária {{< /alternativa >}}
{{< alternativa >}} Deslocamento de elementos {{< /alternativa >}}
{{< solucao letra="C" >}}
A busca binária é a operação mais eficiente para consultas, com complexidade O(log n).
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a complexidade do percurso (percorrer) em um arranjo ordenado?
{{< alternativa >}} O(1) {{< /alternativa >}}
{{< alternativa >}} O(log n) {{< /alternativa >}}
{{< alternativa >}} O(n) {{< /alternativa >}}
{{< alternativa >}} O(n²) {{< /alternativa >}}
{{< solucao letra="C" >}}
Percorrer todos os elementos exige visitar cada posição do arranjo, resultando em O(n).
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Por que a inserção em arranjo ordenado não é O(1)?
{{< alternativa >}} Porque sempre usa busca binária {{< /alternativa >}}
{{< alternativa >}} Porque não existe inserção em arrays {{< /alternativa >}}
{{< alternativa >}} Porque pode ser necessário deslocar vários elementos {{< /alternativa >}}
{{< alternativa >}} Porque o Java não permite arrays ordenados {{< /alternativa >}}
{{< solucao letra="C" >}}
Mesmo encontrando a posição rapidamente, é necessário deslocar elementos, o que pode levar O(n).
{{< /solucao >}}
{{< /questao >}}

---
title: "Questões sobre Notação Big-O: como analisar a complexidade de algoritmos"
description: "Entenda Big-O, como identificar a complexidade, por que usamos apenas o termo dominante e como interpretar crescimento"
slug: big-o-questoes
tags:
  - algoritmos
  - big-o
  - complexidade
  - estruturas-de-dados
  - questões
---

{{< questao >}}
Qual é o principal objetivo da notação Big-O?
{{< alternativa >}} Medir o tempo exato de execução em segundos {{< /alternativa >}}
{{< alternativa >}} Descrever o crescimento do custo de um algoritmo conforme o tamanho da entrada aumenta {{< /alternativa >}}
{{< alternativa >}} Contar o número de linhas do código {{< /alternativa >}}
{{< alternativa >}} Melhorar a sintaxe do código {{< /alternativa >}}
{{< solucao letra="B" >}}
A notação Big-O descreve como o custo de um algoritmo cresce conforme o tamanho da entrada aumenta, focando no comportamento assintótico.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Por que não usamos tempo real na análise de algoritmos?
{{< alternativa >}} Porque Big-O só funciona em Java {{< /alternativa >}}
{{< alternativa >}} Porque o tempo real depende de hardware, sistema operacional e linguagem {{< /alternativa >}}
{{< alternativa >}} Porque tempo real não existe {{< /alternativa >}}
{{< alternativa >}} Porque todos os algoritmos executam no mesmo tempo {{< /alternativa >}}
{{< solucao letra="B" >}}
O tempo real varia conforme o ambiente de execução, tornando a comparação inconsistente.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que significa o termo “assintótico” na análise de complexidade?
{{< alternativa >}} Análise do código em tempo de compilação {{< /alternativa >}}
{{< alternativa >}} Comportamento quando n é muito pequeno {{< /alternativa >}}
{{< alternativa >}} Comportamento do algoritmo quando n tende a valores grandes {{< /alternativa >}}
{{< alternativa >}} Número de variáveis do algoritmo {{< /alternativa >}}
{{< solucao letra="C" >}}
Análise assintótica foca no comportamento do algoritmo quando n cresce muito.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a forma correta simplificada de f(n) = 3n² + 10n + 7 em Big-O?
{{< alternativa >}} O(n) {{< /alternativa >}}
{{< alternativa >}} O(n²) {{< /alternativa >}}
{{< alternativa >}} O(3n² + 10n + 7) {{< /alternativa >}}
{{< alternativa >}} O(log n) {{< /alternativa >}}
{{< solucao letra="B" >}}
Em Big-O, consideramos apenas o termo dominante, que é n².
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Por que ignoramos constantes na notação Big-O?
{{< alternativa >}} Porque constantes não existem na matemática {{< /alternativa >}}
{{< alternativa >}} Porque elas não influenciam o crescimento para grandes valores de n {{< /alternativa >}}
{{< alternativa >}} Porque deixam o código mais lento {{< /alternativa >}}
{{< alternativa >}} Porque são sempre zero {{< /alternativa >}}
{{< solucao letra="B" >}}
Constantes não afetam o comportamento assintótico quando n é grande.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual classe cresce mais rapidamente?
{{< alternativa >}} O(n) {{< /alternativa >}}
{{< alternativa >}} O(n log n) {{< /alternativa >}}
{{< alternativa >}} O(n²) {{< /alternativa >}}
{{< alternativa >}} O(2ⁿ) {{< /alternativa >}}
{{< solucao letra="D" >}}
O(2ⁿ) é exponencial e cresce muito mais rápido que as demais classes.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual das alternativas representa crescimento constante?
{{< alternativa >}} O(n) {{< /alternativa >}}
{{< alternativa >}} O(log n) {{< /alternativa >}}
{{< alternativa >}} O(1) {{< /alternativa >}}
{{< alternativa >}} O(n²) {{< /alternativa >}}
{{< solucao letra="C" >}}
O(1) indica que o custo não depende do tamanho da entrada.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual algoritmo geralmente tem complexidade O(log n)?
{{< alternativa >}} Busca linear {{< /alternativa >}}
{{< alternativa >}} Busca binária {{< /alternativa >}}
{{< alternativa >}} Dois loops aninhados {{< /alternativa >}}
{{< alternativa >}} Percorrer array inteiro {{< /alternativa >}}
{{< solucao letra="B" >}}
A busca binária reduz o problema pela metade a cada passo, resultando em O(log n).
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que significa dizer que O(n²) é pior que O(n)?
{{< alternativa >}} Significa que usa menos memória {{< /alternativa >}}
{{< alternativa >}} Significa que cresce mais lentamente {{< /alternativa >}}
{{< alternativa >}} Significa que o custo cresce mais rapidamente com o aumento de n {{< /alternativa >}}
{{< alternativa >}} Significa que sempre executa mais rápido {{< /alternativa >}}
{{< solucao letra="C" >}}
O(n²) cresce mais rapidamente que O(n), tornando-se mais custoso para entradas grandes.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a ordem correta de crescimento (do melhor para o pior)?
{{< alternativa >}} O(n²), O(n), O(1), O(log n) {{< /alternativa >}}
{{< alternativa >}} O(1), O(log n), O(n), O(n²) {{< /alternativa >}}
{{< alternativa >}} O(log n), O(1), O(n²), O(n) {{< /alternativa >}}
{{< alternativa >}} O(n), O(1), O(n²), O(log n) {{< /alternativa >}}
{{< solucao letra="B" >}}
A ordem correta é: O(1) < O(log n) < O(n) < O(n²).
{{< /solucao >}}
{{< /questao >}}

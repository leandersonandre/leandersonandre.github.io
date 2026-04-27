---
title: "Questões sobre Complexidade de Algoritmos e Análise de Custo"
description: "Como analisar algoritmos e encontrar a função de custo a partir do código"
slug: complexidade-de-algoritmos-questoes
tags:
  - algoritmos
  - estruturas-de-dados
  - análise-de-custo
  - desempenho
---

{{< questao >}}
O que representa o valor n na análise de complexidade de algoritmos?
{{< alternativa >}} O tempo de execução em segundos {{< /alternativa >}}
{{< alternativa >}} O tamanho da entrada do algoritmo {{< /alternativa >}}
{{< alternativa >}} A quantidade de memória RAM usada {{< /alternativa >}}
{{< alternativa >}} O número de linhas do código {{< /alternativa >}}
{{< solucao letra="B" >}}
Na análise de complexidade, n representa o tamanho da entrada do algoritmo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é o principal objetivo da análise de algoritmos?
{{< alternativa >}} Medir o tempo exato em segundos de execução {{< /alternativa >}}
{{< alternativa >}} Comparar linguagens de programação {{< /alternativa >}}
{{< alternativa >}} Entender o custo de execução em função do tamanho da entrada {{< /alternativa >}}
{{< alternativa >}} Melhorar a interface do usuário {{< /alternativa >}}
{{< solucao letra="C" >}}
A análise de algoritmos busca entender como o custo cresce conforme o tamanho da entrada aumenta.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a ideia principal ao calcular a função de custo f(n)?
{{< alternativa >}} Contar o número de variáveis usadas {{< /alternativa >}}
{{< alternativa >}} Somar o número de linhas do código {{< /alternativa >}}
{{< alternativa >}} Contar quantas vezes cada operação é executada em função de n {{< /alternativa >}}
{{< alternativa >}} Medir o tamanho do programa em bytes {{< /alternativa >}}
{{< solucao letra="C" >}}
A função de custo é obtida somando quantas vezes cada instrução é executada em função de n.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a função de custo simplificada da busca linear apresentada?

{{< code >}}
public int buscaLinear(int[] vetor, int alvo) {
    for (int i = 0; i < vetor.length; i++) {
        if (vetor[i] == alvo) {
            return i;
        }
    }
    return -1;
}
{{< /code >}}

{{< alternativa >}} f(n) = log n + 1 {{< /alternativa >}}
{{< alternativa >}} f(n) = n² + n {{< /alternativa >}}
{{< alternativa >}} f(n) = 3n + 4 {{< /alternativa >}}
{{< alternativa >}} f(n) = 2ⁿ {{< /alternativa >}}
{{< solucao letra="C" >}}
A análise do algoritmo resulta em f(n) = 3n + 4.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece com o custo da busca linear quando o tamanho do arranjo dobra?
{{< alternativa >}} O custo diminui pela metade {{< /alternativa >}}
{{< alternativa >}} O custo permanece constante {{< /alternativa >}}
{{< alternativa >}} O custo aproximadamente dobra {{< /alternativa >}}
{{< alternativa >}} O custo vira logarítmico {{< /alternativa >}}
{{< solucao letra="C" >}}
Na busca linear, o custo cresce proporcionalmente ao tamanho da entrada.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual caso da busca linear representa o melhor desempenho?
{{< alternativa >}} Elemento na última posição {{< /alternativa >}}
{{< alternativa >}} Elemento não existe {{< /alternativa >}}
{{< alternativa >}} Elemento na primeira posição {{< /alternativa >}}
{{< alternativa >}} Lista vazia sempre {{< /alternativa >}}
{{< solucao letra="C" >}}
No melhor caso, o elemento está na primeira posição e é encontrado imediatamente.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual caso representa o pior caso da busca linear?
{{< alternativa >}} Elemento na primeira posição {{< /alternativa >}}
{{< alternativa >}} Elemento no meio {{< /alternativa >}}
{{< alternativa >}} Elemento na última posição ou inexistente {{< /alternativa >}}
{{< alternativa >}} Lista ordenada {{< /alternativa >}}
{{< solucao letra="C" >}}
O pior caso ocorre quando o elemento está no final ou não existe.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual tipo de crescimento a busca linear apresenta?

{{< code >}}
public int buscaLinear(int[] vetor, int alvo) {
    for (int i = 0; i < vetor.length; i++) {
        if (vetor[i] == alvo) {
            return i;
        }
    }
    return -1;
}
{{< /code >}}

{{< alternativa >}} Constante O(1) {{< /alternativa >}}
{{< alternativa >}} Logarítmico O(log n) {{< /alternativa >}}
{{< alternativa >}} Linear O(n) {{< /alternativa >}}
{{< alternativa >}} Quadrático O(n²) {{< /alternativa >}}
{{< solucao letra="C" >}}
A busca linear cresce de forma linear em relação ao tamanho da entrada.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual operação geralmente possui custo constante O(1)?
{{< alternativa >}} Percorrer um array inteiro {{< /alternativa >}}
{{< alternativa >}} Dois loops aninhados {{< /alternativa >}}
{{< alternativa >}} Acesso direto a um elemento por índice {{< /alternativa >}}
{{< alternativa >}} Busca linear {{< /alternativa >}}
{{< solucao letra="C" >}}
O acesso direto por índice é uma operação de custo constante O(1).
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual tipo de algoritmo geralmente possui crescimento O(n²)?
{{< alternativa >}} Busca binária {{< /alternativa >}}
{{< alternativa >}} Percurso simples {{< /alternativa >}}
{{< alternativa >}} Dois loops aninhados {{< /alternativa >}}
{{< alternativa >}} Acesso direto {{< /alternativa >}}
{{< solucao letra="C" >}}
Algoritmos com dois loops aninhados geralmente têm complexidade quadrática O(n²).
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Por que a análise de algoritmos ignora hardware e sistema operacional?
{{< alternativa >}} Porque não influenciam o desempenho {{< /alternativa >}}
{{< alternativa >}} Porque só funcionam em Java {{< /alternativa >}}
{{< alternativa >}} Para focar no comportamento matemático do algoritmo {{< /alternativa >}}
{{< alternativa >}} Porque são sempre iguais em todos os computadores {{< /alternativa >}}
{{< solucao letra="C" >}}
A análise foca no comportamento teórico do algoritmo, independente do ambiente físico.
{{< /solucao >}}
{{< /questao >}}

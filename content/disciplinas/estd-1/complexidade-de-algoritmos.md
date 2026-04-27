---
title: "Complexidade de Algoritmos e Análise de Custo"
description: "Como analisar algoritmos e encontrar a função de custo a partir do código"
slug: complexidade-de-algoritmos
tags:
  - algoritmos
  - estruturas-de-dados
  - análise-de-custo
  - desempenho
---

## Introdução

A análise de algoritmos tem como objetivo entender quanto “custa” executar um algoritmo em função do tamanho da entrada, normalmente representado por **n**.

Esse custo pode ser interpretado como tempo de execução ou uso de memória. Para simplificar a análise, não consideramos detalhes de hardware, sistema operacional ou linguagem, mas sim a quantidade de operações realizadas.

A forma mais comum de estudar esse comportamento é transformar o código em uma **função de custo f(n)**.

## Como encontrar a função de custo

A ideia central é simples: cada linha de um algoritmo possui um custo básico de execução. Esse custo é somado de acordo com o número de vezes que a linha é executada.

Uma forma prática de análise é:

1. Identificar as instruções básicas
2. Contar quantas vezes cada instrução é executada em função de n
3. Somar os custos
4. Simplificar a função resultante

Esse processo permite transformar código em uma expressão matemática.

## Exemplo completo: busca linear

A busca linear percorre um arranjo elemento por elemento até encontrar o valor desejado ou até o final da estrutura.

```java
public int buscaLinear(int[] vetor, int alvo) {
    for (int i = 0; i < vetor.length; i++) {
        if (vetor[i] == alvo) {
            return i;
        }
    }
    return -1;
}
````

## Análise de custo por linha

Podemos decompor o algoritmo da seguinte forma:

| Linha | Operação                | Execuções | Custo total |
| ----- | ----------------------- | --------- | ----------- |
| 1     | inicialização do método | 1         | 1           |
| 2     | inicialização do for    | 1         | 1           |
| 3     | comparação i < n        | n + 1     | n + 1       |
| 3     | incremento i++          | n         | n           |
| 4     | comparação vetor[i]     | n         | n           |
| 5     | return i (melhor caso)  | 1         | 1           |
| 7     | return -1               | 1         | 1           |

## Função de custo

Somando os custos:

```text
f(n) = (n + 1) + n + n + 3
```

Simplificando:

```text
f(n) = 3n + 4
```

## Interpretação do resultado

A função mostra que o número de operações cresce proporcionalmente ao tamanho do arranjo.

Isso significa que, se o tamanho do arranjo dobra, o número de operações também dobra aproximadamente.

Esse comportamento é típico de algoritmos que percorrem todos os elementos de forma sequencial.

## Melhor caso e pior caso

Na busca linear, o custo depende da posição do elemento.

Se o elemento estiver na primeira posição, o algoritmo termina imediatamente.

Se estiver na última posição ou não existir, o algoritmo percorre todo o arranjo.

Isso faz com que a análise de custo seja fortemente influenciada pela posição do dado.

## Exemplo intuitivo de crescimento

A tabela abaixo mostra como o número de comparações cresce com o tamanho do arranjo:

| n (tamanho) | Comparações no pior caso |
| ----------- | ------------------------ |
| 10          | 10                       |
| 100         | 100                      |
| 1.000       | 1.000                    |
| 10.000      | 10.000                   |

O crescimento é direto e proporcional.

## Comparação com outros comportamentos

Algoritmos podem ter comportamentos diferentes dependendo da estrutura:

| Tipo de acesso       | Crescimento do custo |
| -------------------- | -------------------- |
| Acesso direto        | constante            |
| Percurso sequencial  | linear               |
| Dois loops aninhados | quadrático           |

A busca linear pertence ao grupo de crescimento linear, pois depende diretamente do tamanho da entrada.

## Conclusão

A análise de algoritmos por custo de execução permite entender como o código se comporta antes mesmo de ser executado.

No caso da busca linear, a simplicidade do algoritmo também implica em crescimento proporcional ao tamanho da entrada, o que pode se tornar custoso em estruturas muito grandes.

Esse tipo de análise é essencial para comparar diferentes soluções e escolher a estrutura de dados mais adequada para cada problema.

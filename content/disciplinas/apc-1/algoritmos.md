---
title: "Algoritmos"
slug: "algoritmos"
description: "Algoritmos"
tags:
- algoritmos
- fluxograma
---

## O que são algoritmos?

Algoritmos são sequências finitas e bem definidas de passos utilizados para resolver um problema ou executar uma tarefa. Eles funcionam como uma “receita”, onde cada instrução deve ser seguida em ordem para chegar ao resultado esperado.

Na computação, algoritmos são a base de todos os programas, desde operações simples até sistemas complexos.


## Características de um algoritmo

Um algoritmo eficiente deve possuir:

- **Finitude**: deve terminar após um número finito de passos  
- **Precisão**: cada instrução deve ser clara e sem ambiguidades  
- **Entrada (input)**: pode receber dados iniciais  
- **Saída (output)**: deve produzir um resultado  
- **Eficiência**: deve resolver o problema de forma adequada  


## Formas de representar algoritmos

### Linguagem natural

Descrição passo a passo usando texto simples.

**Exemplo:**
1. Pegue dois números  
2. Some os dois  
3. Mostre o resultado  


### Pseudocódigo

Uma forma intermediária entre linguagem natural e código de programação.

```text
início
  leia A
  leia B
  soma ← A + B
  escreva soma
fim
````


### Fluxograma

Representação gráfica do algoritmo usando símbolos:

* Oval → início/fim
* Retângulo → processo
* Paralelogramo → entrada/saída
* Losango → decisão

{{< plantuml >}}
start

:Leia o número N;

if (N mod 2 == 0?) then (sim)
  :Exibir "Par";
else (não)
  :Exibir "Ímpar";
endif

stop
{{< /plantuml>}}

## Tipos de algoritmos

* **Sequenciais**: executam passos em ordem fixa
* **Condicionais**: tomam decisões (if/else)
* **Repetitivos**: usam laços (for, while)
* **Recursivos**: chamam a si mesmos


## Exemplo de algoritmo: número par ou ímpar

```text
início
  leia N
  se N mod 2 = 0 então
     escreva "Par"
  senão
     escreva "Ímpar"
fim
```


## Importância dos algoritmos

Os algoritmos são essenciais porque:

* Permitem resolver problemas de forma lógica
* São a base da programação
* Ajudam a otimizar processos
* Podem ser aplicados em diversas áreas


## Conclusão

Aprender algoritmos é o primeiro passo para desenvolver lógica de programação. Um bom algoritmo torna qualquer solução mais eficiente e organizada.

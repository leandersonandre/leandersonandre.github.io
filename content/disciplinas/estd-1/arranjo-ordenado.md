---
title: "Arranjo Ordenado"
description: "Estrutura de dados baseada em arrays com elementos mantidos em ordem"
slug: arranjo-ordenado
tags:

- estruturas-de-dados
- arrays
- ordenação
- busca

---

Um arranjo ordenado é uma estrutura de dados baseada em arrays na qual os elementos são mantidos sempre em ordem, geralmente crescente ou decrescente.

A principal vantagem de manter os dados ordenados está na eficiência das operações de busca. Quando os elementos estão organizados, é possível utilizar algoritmos mais rápidos, como a busca binária, reduzindo significativamente o número de comparações necessárias.

## Estrutura

Um arranjo ordenado pode ser representado por três atributos principais:

```java id="k2m9qx"
private int[] arranjo;
private int capacidade;
private int tamanho;
```

{{< plantuml >}}
class ArranjoOrdenado {
  - arranjo: int[] 
  - capacidade: int 
  - tamanho: int 

  + ArranjoOrdenado(capacidade: int )
  + inserir(valor: int )
  + deletar(valor: int )
  + buscar(valor: int ): int
  +  percorrer()
}
{{< /plantuml >}}



O array armazena os elementos. A capacidade define o limite máximo de armazenamento. O tamanho indica quantos elementos estão efetivamente armazenados.

## Inserção

A inserção em um arranjo ordenado exige que a ordem seja mantida. Para isso, não basta inserir o elemento no final.

O processo consiste em encontrar a posição correta do novo elemento e deslocar os elementos maiores uma posição à direita.

Exemplo:

```text id="q8t1mz"
Antes: [3, 5, _, _, _]
Inserir: 4
Depois: [3, 4, 5, _, _]
```

Passos envolvidos:

Primeiro, verifica-se se o arranjo possui espaço disponível. Em seguida, encontra-se a posição onde o elemento deve ser inserido. Depois disso, todos os elementos à direita dessa posição são deslocados. Por fim, o novo valor é inserido e o tamanho é incrementado.

```java id="9d3kq1"
public void inserir(int valor) {
    if (tamanho == capacidade) {
        throw new RuntimeException("Arranjo cheio");
    }

    int i;
    for (i = tamanho - 1; i >= 0 && arranjo[i] > valor; i--) {
        arranjo[i + 1] = arranjo[i];
    }

    arranjo[i + 1] = valor;
    tamanho++;
}
```

## Remoção

A remoção também precisa manter a ordem do arranjo. Após localizar o elemento, os elementos à direita devem ser deslocados para a esquerda.

```java id="1x7npa"
public void deletar(int valor) {
    int pos = buscar(valor);

    if (pos == -1) {
        throw new RuntimeException("Elemento não encontrado");
    }

    for (int i = pos; i < tamanho - 1; i++) {
        arranjo[i] = arranjo[i + 1];
    }

    tamanho--;
}
```

Quando o elemento removido está no final, basta reduzir o tamanho. Caso esteja no meio, o deslocamento é necessário.

## Busca

A busca pode ser realizada atráves da busca linear ou busca binária.

### Busca linear

Em um arranjo ordenado, a busca linear pode ser otimizada aproveitando o fato de que os elementos estão em ordem crescente. Isso significa que, ao percorrer o arranjo, se encontrarmos um valor maior que o valor procurado, podemos interromper a busca antecipadamente, pois o elemento não estará nas posições seguintes.

```java id="buscaord1"
public int buscar(int valor) {
    for (int i = 0; i < tamanho; i++) {
        if (arranjo[i] == valor) {
            return i; // encontrado
        }

        // como o array é ordenado, pode parar antes
        if (arranjo[i] > valor) {
            break;
        }
    }
    return -1; // não encontrado
}
```

### Busca binária

A busca pode ser feita de forma mais eficiente devido à ordenação. Embora seja possível usar busca sequencial, o ideal é utilizar busca binária.

```java id="m7z2qp"
public int buscar(int valor) {
    int inicio = 0;
    int fim = tamanho - 1;

    while (inicio <= fim) {
        int meio = (inicio + fim) / 2;

        if (arranjo[meio] == valor) {
            return meio;
        } else if (arranjo[meio] < valor) {
            inicio = meio + 1;
        } else {
            fim = meio - 1;
        }
    }

    return -1;
}
```

## Percorrer

O percurso deve considerar apenas os elementos válidos do arranjo, ou seja, até o tamanho.

```java id="z4c8yr"
public void percorrer() {
    for (int i = 0; i < tamanho; i++) {
        System.out.println(arranjo[i]);
    }
}
```

## Vantagens e desvantagens

A principal vantagem do arranjo ordenado está na eficiência da busca, que pode ser realizada em tempo logarítmico com busca binária.

Por outro lado, operações de inserção e remoção podem ser custosas, pois exigem deslocamento de elementos, resultando em tempo linear.

## Complexidade de Tempo (Big O)

A análise de complexidade Big O descreve o desempenho dos algoritmos em função do tamanho da entrada (n). Em arranjos ordenados, o principal ganho está na eficiência das operações de busca.

A **busca linear** percorre os elementos de forma sequencial. Em arranjos ordenados, é possível interromper a execução antes do final caso o valor atual ultrapasse o valor procurado. Ainda assim, no pior caso, o custo permanece linear.

A **busca binária**, por sua vez, utiliza a ordenação do arranjo para reduzir o espaço de busca pela metade a cada iteração. Essa estratégia torna o algoritmo significativamente mais eficiente, principalmente para grandes conjuntos de dados.

As operações de **inserção** e **remoção** apresentam maior custo, pois, mesmo quando a posição correta é encontrada rapidamente, é necessário deslocar os elementos subsequentes para manter a ordenação do arranjo.

A tabela a seguir resume as complexidades das principais operações:

| Operação      | Melhor Caso | Caso Médio | Pior Caso |
| ------------- | ----------- | ---------- | --------- |
| Busca Linear  | O(1)        | O(n)       | O(n)      |
| Busca Binária | O(1)        | O(log n)   | O(log n)  |
| Inserir       | O(1)        | O(n)       | O(n)      |
| Remover       | O(1)        | O(n)       | O(n)      |
| Percorrer     | O(n)        | O(n)       | O(n)      |

Na prática, a **busca binária** é a abordagem mais adequada para arranjos ordenados quando há predominância de operações de consulta, pois reduz drasticamente o número de comparações.

A **busca linear**, embora menos eficiente em termos assintóticos, pode ser adequada em cenários com poucos elementos ou quando se busca simplicidade de implementação.

Por outro lado, inserções e remoções continuam sendo operações custosas. Mesmo com a localização eficiente da posição correta, o deslocamento de elementos mantém o custo linear. Dessa forma, arranjos ordenados são mais indicados para cenários com muitas buscas e poucas modificações estruturais.

## Exemplo de uso

A seguir é apresentada uma implementação completa de um arranjo ordenado em Java. Nesse exemplo, os elementos são mantidos em ordem crescente, utilizando **busca binária** para localizar posições e **deslocamento de elementos** para inserção e remoção.

```java
public class ArranjoOrdenado {
    private int[] elementos;
    private int tamanho;

    public ArranjoOrdenado(int capacidade) {
        elementos = new int[capacidade];
        tamanho = 0;
    }

    // Busca binária
    public int buscar(int valor) {
        int inicio = 0;
        int fim = tamanho - 1;

        while (inicio <= fim) {
            int meio = (inicio + fim) / 2;

            if (elementos[meio] == valor) {
                return meio;
            } else if (elementos[meio] < valor) {
                inicio = meio + 1;
            } else {
                fim = meio - 1;
            }
        }

        return -1; // não encontrado
    }

    // Inserção mantendo ordenação
    public void inserir(int valor) {
        if (tamanho == elementos.length) {
            System.out.println("Arranjo cheio");
            return;
        }

        int i;

        // encontra a posição correta
        for (i = tamanho - 1; i >= 0 && elementos[i] > valor; i--) {
            elementos[i + 1] = elementos[i]; // desloca para a direita
        }

        elementos[i + 1] = valor;
        tamanho++;
    }

    // Remoção de elemento
    public boolean remover(int valor) {
        int indice = buscar(valor);

        if (indice == -1) {
            return false;
        }

        // desloca elementos para a esquerda
        for (int i = indice; i < tamanho - 1; i++) {
            elementos[i] = elementos[i + 1];
        }

        tamanho--;
        return true;
    }

    // Impressão do arranjo
    public void imprimir() {
        for (int i = 0; i < tamanho; i++) {
            System.out.print(elementos[i] + " ");
        }
        System.out.println();
    }

    public static void main(String[] args) {
        ArranjoOrdenado arr = new ArranjoOrdenado(10);

        arr.inserir(30);
        arr.inserir(10);
        arr.inserir(20);
        arr.inserir(40);

        System.out.print("Arranjo: ");
        arr.imprimir();

        System.out.println("Buscar 20: índice = " + arr.buscar(20));

        arr.remover(20);
        System.out.print("Após remover 20: ");
        arr.imprimir();
    }
}
```

Nesse exemplo:

O método `inserir` garante que os elementos permaneçam ordenados, deslocando os valores maiores para abrir espaço.

O método `buscar` utiliza **busca binária**, aproveitando a ordenação para melhorar o desempenho.

O método `remover` elimina um elemento e reorganiza o arranjo para manter a sequência contínua.

Essa implementação evidencia bem o comportamento do arranjo ordenado: buscas eficientes, porém com custo maior em inserções e remoções devido ao deslocamento de elementos.


## Conclusão

O arranjo ordenado é uma estrutura simples, mas poderosa, especialmente quando há muitas operações de busca e poucas inserções e remoções. Ele exemplifica bem o trade-off entre custo de manutenção da ordem e ganho de desempenho nas consultas.

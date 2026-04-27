---
title: "Lista Baseada em Arranjo"
description: "Estrutura de dados dinâmica baseada em arrays com crescimento e operações sequenciais"
slug: lista-baseada-em-arranjos
tags:
  - estruturas-de-dados
  - arrays
  - listas
  - java
  - arraylist
---

Uma lista baseada em arranjo é uma estrutura de dados linear que utiliza um array como estrutura interna para armazenar elementos de forma sequencial.

Ela é dinâmica na prática porque permite crescimento automático quando a capacidade do array é atingida, simulando o comportamento de uma lista flexível mesmo sendo baseada em uma estrutura estática.

## Estrutura

A estrutura interna de uma lista baseada em arranjo é simples, normalmente composta por um array e uma variável que controla o número de elementos inseridos. Essa combinação permite controlar tanto o armazenamento quanto o uso efetivo da lista.

```java
private int[] elementos;
private int tamanho;
```

{{< plantuml >}}
class ListaBaseadaEmArranjo {

* elementos: int[]
* tamanho: int

- adicionar(valor: int)
- inserir(posicao: int, valor: int)
- remover(posicao: int)
- obter(posicao: int): int
- atualizar(posicao: int): int
- percorrer()
  }
{{< /plantuml >}}

O array é responsável pelo armazenamento dos dados, enquanto o tamanho indica quantos elementos válidos existem atualmente na lista. Essa separação permite distinguir entre capacidade total e uso real.

## Ideia principal

A ideia central dessa estrutura é simular uma lista dinâmica utilizando um array fixo internamente. Quando o espaço se esgota, um novo array maior é criado e os elementos são copiados.

Esse comportamento permite que a estrutura cresça sob demanda, mantendo a simplicidade do array original.

## Adição de elementos

Adicionar elementos no final da lista é a operação mais simples e eficiente. Ela consiste apenas em inserir o valor na próxima posição livre e incrementar o tamanho.

```java 
public void adicionar(int valor) {
    if (tamanho == elementos.length) {
        redimensionar();
    }

    elementos[tamanho] = valor;
    tamanho++;
}
```

Essa operação é geralmente rápida, pois não exige movimentação de outros elementos, exceto quando ocorre o redimensionamento.

## Redimensionamento

O redimensionamento ocorre quando o array interno atinge sua capacidade máxima. Nesse caso, é criado um novo array maior e todos os elementos são copiados para ele.

```java id="r8m2cc"
private void redimensionar() {
    int novaCapacidade = elementos.length * 2;
    int[] novoArray = new int[novaCapacidade];

    for (int i = 0; i < elementos.length; i++) {
        novoArray[i] = elementos[i];
    }

    elementos = novoArray;
}
```

Esse processo garante que a lista possa continuar crescendo, embora tenha um custo computacional de O(n) no momento da cópia.

## Inserção em posição específica

Inserir em uma posição intermediária exige deslocar os elementos à direita para abrir espaço. Isso torna essa operação mais custosa.

```java id="i4k7dd"
public void inserir(int posicao, int valor) {
    if (posicao < 0 || posicao > tamanho) {
        throw new IndexOutOfBoundsException();
    }

    if (tamanho == elementos.length) {
        redimensionar();
    }

    for (int i = tamanho - 1; i >= posicao; i--) {
        elementos[i + 1] = elementos[i];
    }

    elementos[posicao] = valor;
    tamanho++;
}
```

Esse deslocamento garante que a ordem dos elementos seja preservada após a inserção.

## Remoção de elementos

A remoção também exige reorganização da estrutura, pois os elementos à direita precisam ser deslocados para preencher o espaço vazio.

```java id="d1n9ee"
public void remover(int posicao) {
    if (posicao < 0 || posicao >= tamanho) {
        throw new IndexOutOfBoundsException();
    }

    for (int i = posicao; i < tamanho - 1; i++) {
        elementos[i] = elementos[i + 1];
    }

    tamanho--;
}
```

Essa operação mantém a continuidade da lista, garantindo que não existam “buracos” no array.

## Acesso a elementos

O acesso a elementos em uma lista baseada em arranjo é direto, o que torna essa operação extremamente eficiente.

```java id="g6t8ff"
public int obter(int posicao) {
    if (posicao < 0 || posicao >= tamanho) {
        throw new IndexOutOfBoundsException();
    }

    return elementos[posicao];
}
```

Esse acesso direto é uma das principais vantagens dessa estrutura.

## Atualização de elementos

A atualização de elementos em uma lista baseada em arranjo consiste em substituir um valor já existente em uma posição específica da estrutura. Essa operação não altera o tamanho da lista, apenas modifica o conteúdo armazenado.

Por ser uma estrutura que permite acesso direto por índice, a atualização é simples e eficiente, desde que a posição seja válida.

```java
public int atualizar(int posicao, int valor) {
    if (posicao < 0 || posicao >= tamanho) {
        throw new IndexOutOfBoundsException();
    }

    int substituido = elementos[posicao];
    elementos[posicao] = valor;
    return substituido;
}
```

Essa operação é bastante eficiente, pois ocorre em tempo constante O(1), já que não há necessidade de deslocamento de elementos nem redimensionamento do array.


## Percorrer a lista

Percorrer a lista significa visitar cada elemento válido armazenado, respeitando o tamanho atual da estrutura.

```java id="p2k5gg"
public void percorrer() {
    for (int i = 0; i < tamanho; i++) {
        System.out.println(elementos[i]);
    }
}
```

Esse tipo de iteração é comum em operações de leitura e processamento de dados.

## Complexidade de tempo (Big O)

A análise de complexidade mostra o comportamento da estrutura em diferentes operações. O acesso direto é muito eficiente, enquanto inserções e remoções podem exigir deslocamento de elementos.

| Operação            | Melhor Caso | Caso Médio | Pior Caso |
|---------------------|------------|------------|-----------|
| Acesso por índice   | O(1)       | O(1)       | O(1)      |
| Adicionar no fim    | O(1)       | O(1)*      | O(n)      |
| Inserir no meio     | O(1)       | O(n)       | O(n)      |
| Remover             | O(1)       | O(n)       | O(n)      |
| Atualizar           | O(1)       | O(1)       | O(1)      |
| Percorrer           | O(n)       | O(n)       | O(n)      |

O custo amortizado de adicionar no final continua sendo baixo na prática, mesmo com eventuais redimensionamentos.

## Vantagens e desvantagens

As listas baseadas em arranjo possuem um bom equilíbrio entre desempenho e simplicidade, mas apresentam limitações em operações estruturais.

### Vantagens

* Acesso direto muito rápido (O(1))
* Boa performance para inserção no final
* Estrutura simples e eficiente
* Boa localidade de memória

### Desvantagens

* Inserção no meio é custosa
* Remoção exige deslocamento
* Redimensionamento pode impactar desempenho

## Exemplo de uso

A seguir é apresentada uma implementação completa de uma lista baseada em arranjo, incluindo operações de adição, inserção, remoção, atualização e acesso. O método de atualização foi implementado de forma que retorna o elemento antigo que foi substituído, permitindo maior controle sobre as alterações realizadas na estrutura.

```java id="l9m2ex"
public class ListaBaseadaEmArranjo {

    private int[] elementos;
    private int tamanho;

    public ListaBaseadaEmArranjo(int capacidade) {
        elementos = new int[capacidade];
        tamanho = 0;
    }

    public void adicionar(int valor) {
        if (tamanho == elementos.length) {
            redimensionar();
        }

        elementos[tamanho] = valor;
        tamanho++;
    }

    public void inserir(int posicao, int valor) {
        if (posicao < 0 || posicao > tamanho) {
            throw new IndexOutOfBoundsException();
        }

        if (tamanho == elementos.length) {
            redimensionar();
        }

        for (int i = tamanho - 1; i >= posicao; i--) {
            elementos[i + 1] = elementos[i];
        }

        elementos[posicao] = valor;
        tamanho++;
    }

    public int remover(int posicao) {
        if (posicao < 0 || posicao >= tamanho) {
            throw new IndexOutOfBoundsException();
        }

        int removido = elementos[posicao];

        for (int i = posicao; i < tamanho - 1; i++) {
            elementos[i] = elementos[i + 1];
        }

        tamanho--;
        return removido;
    }

    public int atualizar(int posicao, int valor) {
        if (posicao < 0 || posicao >= tamanho) {
            throw new IndexOutOfBoundsException();
        }

        int antigo = elementos[posicao];
        elementos[posicao] = valor;

        return antigo;
    }

    public int obter(int posicao) {
        if (posicao < 0 || posicao >= tamanho) {
            throw new IndexOutOfBoundsException();
        }

        return elementos[posicao];
    }

    public void percorrer() {
        for (int i = 0; i < tamanho; i++) {
            System.out.println(elementos[i]);
        }
    }

    private void redimensionar() {
        int novaCapacidade = elementos.length * 2;
        int[] novoArray = new int[novaCapacidade];

        for (int i = 0; i < elementos.length; i++) {
            novoArray[i] = elementos[i];
        }

        elementos = novoArray;
    }

    public static void main(String[] args) {
        ListaBaseadaEmArranjo lista = new ListaBaseadaEmArranjo(3);

        lista.adicionar(10);
        lista.adicionar(20);
        lista.adicionar(30);

        System.out.println("Lista inicial:");
        lista.percorrer();

        lista.inserir(1, 15);

        System.out.println("Após inserção:");
        lista.percorrer();

        int removido = lista.remover(2);
        System.out.println("Removido: " + removido);

        System.out.println("Após remoção:");
        lista.percorrer();

        int antigo = lista.atualizar(1, 99);
        System.out.println("Valor substituído: " + antigo);

        System.out.println("Após atualização:");
        lista.percorrer();
    }
}
```


## Implementação na biblioteca Java

Na linguagem Java, essa estrutura já está pronta na biblioteca padrão através da implementação dinâmica de listas baseada em arrays.

java.util.ArrayList

Ela faz parte do Java Collections Framework e encapsula toda a lógica de redimensionamento e manipulação interna.

### Exemplo de uso

```java id="j8m3hh"
import java.util.ArrayList;

public class Exemplo {
    public static void main(String[] args) {
        ArrayList<String> lista = new ArrayList<>();

        lista.add("A");
        lista.add("B");
        lista.add("C");

        lista.add(1, "X");

        lista.remove("B");

        for (String item : lista) {
            System.out.println(item);
        }
    }
}
```

Internamente, essa implementação utiliza um array que cresce dinamicamente conforme necessário, mantendo a lógica de deslocamento quando há inserções ou remoções no meio.

## Conclusão

A lista baseada em arranjo é uma das estruturas mais importantes da ciência da computação por equilibrar simplicidade e eficiência. Ela é amplamente utilizada em sistemas reais, principalmente quando há necessidade de acesso rápido aos dados e predominância de operações de leitura.

---
title: "Fila"
description: "Estrutura de dados FIFO"
slug: fila
tags:

- estruturas-de-dados
- fila
- queue
---

Uma fila é uma estrutura de dados linear que segue o princípio **FIFO (First In, First Out)**, onde o primeiro elemento a entrar é o primeiro a sair.
Diferente de um arranjo ordenado, a fila **não mantém ordenação**, mas sim a ordem de chegada dos elementos.
Quando implementada com **lista encadeada**, a fila se torna dinâmica, não necessitando de tamanho fixo.

## Estrutura

Uma fila com lista encadeada pode ser representada por:

```java 
private Node head;
private Node tail;
private int size;
```

Cada nó contém um valor e uma referência para o próximo:

```java 
class Node {
    int value;
    Node next;

    public Node(int value) {
        this.value = value;
        this.next = null;
    }
}
```

{{< plantuml >}}
class Queue {
-head: Node
-tail: Node
-size: int
+queue(value: int)
+dequeue(): int
+peek(): int
+isEmpty(): boolean
}
{{< /plantuml >}}


## Inserção (enqueue)

A inserção ocorre sempre no **final da fila (tail)**.

Exemplo:

```java
public void enqueue(int value) {
    Node newNode = new Node(value);

    if (isEmpty()) {
        head = tail = newNode;
    } else {
        tail.next = newNode;
        tail = newNode;
    }

    size++;
}
```


## Remoção (dequeue)

A remoção ocorre sempre no **início da fila (head)**.

```java
public int dequeue() {
    if (isEmpty()) {
        throw new RuntimeException("Fila vazia");
    }

    int value = head.value;
    head = head.next;

    if (head == null) {
        tail = null;
    }

    size--;
    return value;
}
```


## Consulta (peek)

Retorna o primeiro elemento sem remover.

```java
public int peek() {
    if (isEmpty()) {
        throw new RuntimeException("Fila vazia");
    }

    return head.value;
}
```


## Vantagens e desvantagens

A principal vantagem da fila está na eficiência de inserção e remoção dos elementos, que pode ser realizada em tempo constante.

Por outro lado, a fila não permite acesso direto a elementos intermediários e apenas o primeiro elemento pode ser removido.

## Complexidade de Tempo (Big O)



A tabela a seguir resume as complexidades das principais operações:

| Operação      | Complexidade | 
| ------------- | ----------- | 
| Enqueue  | O(1)        | 
| Dequeue | O(1)        | 
| Peek       | O(1)        | 


## Exemplo de uso

A seguir é apresentada uma implementação completa de uma fila em Java.

```java
public class Queue {
    private Node head;
    private Node tail;
    private int size;

    private class Node {
        int value;
        Node next;

        Node(int value) {
            this.value = value;
        }
    }

    public void enqueue(int value) {
        Node newNode = new Node(value);

        if (isEmpty()) {
            head = tail = newNode;
        } else {
            tail.next = newNode;
            tail = newNode;
        }

        size++;
    }

    public int dequeue() {
        if (isEmpty()) {
            throw new RuntimeException("Fila vazia");
        }

        int value = head.value;
        head = head.next;

        if (head == null) {
            tail = null;
        }

        size--;
        return value;
    }

    public int peek() {
        if (isEmpty()) {
            throw new RuntimeException("Fila vazia");
        }

        return head.value;
    }

    public boolean isEmpty() {
        return size == 0;
    }

    public void imprimir() {
        Node current = head;

        while (current != null) {
            System.out.print(current.value + " ");
            current = current.next;
        }

        System.out.println();
    }

    public static void main(String[] args) {
        Queue fila = new Queue();

        fila.enqueue(10);
        fila.enqueue(20);
        fila.enqueue(30);

        fila.imprimir(); // 10 20 30

        System.out.println("Removido: " + fila.dequeue()); // 10

        fila.imprimir(); // 20 30

        System.out.println("Primeiro: " + fila.peek()); // 20
    }
}
```


## Exemplo de uso da Fila da plataforma Java

A classe LinkedList do Java também pode ser utilizada como uma fila (FIFO), pois implementa a interface Queue.
Isso permite inserir elementos no final e remover do início de forma eficiente.

```java
import java.util.LinkedList;
import java.util.Queue;

public class ExemploFila {

    public static void main(String[] args) {

        Queue<Integer> fila = new LinkedList<>();

        // enqueue (inserção no final)
        fila.add(10);
        fila.add(20);
        fila.add(30);
        fila.add(40);

        System.out.println("Fila: " + fila);

        // peek (consulta o primeiro)
        System.out.println("Primeiro elemento: " + fila.peek());

        // dequeue (remove do início)
        System.out.println("Removido: " + fila.poll());

        System.out.println("Fila após remoção: " + fila);

        // percorrer
        for (Integer valor : fila) {
            System.out.println(valor);
        }
    }
}
```

Em Java, além da LinkedList, também é possível utilizar a classe ArrayDeque como implementação de fila. Ela é baseada em um array circular, oferecendo inserções e remoções eficientes nas extremidades com custo O(1) na prática. Por não possuir a sobrecarga de nós encadeados, costuma apresentar melhor desempenho e menor consumo de memória em comparação com a LinkedList. Por isso, ArrayDeque é geralmente a opção mais recomendada para filas em aplicações reais, desde que não seja necessário trabalhar com valores null ou cenários concorrentes.

```java
import java.util.ArrayDeque;

Queue<Integer> fila = new ArrayDeque<>();
```

## Conclusão

A fila é uma estrutura baseada no príncipio FIFO, sendo amplamento utilizada em processamento de tarefas, sistemas de filas, algoritmos de busca em largura (BFS). Sua implementação com lista encadeada garante eficiência e flexibilidade, com operações principais em tempo constante.

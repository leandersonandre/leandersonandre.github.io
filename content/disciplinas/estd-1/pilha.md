---
title: "Pilha"
description: "Estrutura de dados LIFO"
slug: pilha
tags:

- estruturas-de-dados
- pilha
- stack
---

Uma pilha é uma estrutura de dados linear que segue o princípio **LIFO (Last In, First Out)**, onde o último elemento a entrar é o primeiro a sair.
Diferente de uma fila, a pilha opera apenas em **uma extremidade**, chamada de topo (top).
Quando implementada com **lista encadeada**, a pilha se torna dinâmica, não necessitando de tamanho fixo.

## Estrutura

Uma pilha com lista encadeada pode ser representada por:

```java 
private Node top;
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
class Stack {
-top: Node
-size: int
+push(value: int)
+pop(): int
+peek(): int
+isEmpty(): boolean
}
{{< /plantuml >}}


## Inserção (push)

A inserção ocorre sempre no **no topo da pilha (top)**.

Exemplo:

```java
public void push(int value) {
    Node newNode = new Node(value);

    newNode.next = top;
    top = newNode;

    size++;
}
```


## Remoção (pop)

A remoção ocorre sempre no **topo da pilha (top)**.

```java
public int pop() {
    if (isEmpty()) {
        throw new RuntimeException("Pilha vazia");
    }

    int value = top.value;
    top = top.next;

    size--;
    return value;
}
```


## Consulta (peek)

Retorna o  elemento do topo sem remover.

```java
public int peek() {
    if (isEmpty()) {
        throw new RuntimeException("Pilha vazia");
    }

    return top.value;
}
```


## Vantagens e desvantagens

A principal vantagem da pilha está na simplicidade e eficiência das operações, que ocorrem sempre no topo e em tempo constante.

Por outro lado, a pilha não permite acesso direto a elementos intermediários, limitando o acesso ao último elemento inserido.

## Complexidade de Tempo (Big O)



A tabela a seguir resume as complexidades das principais operações:

| Operação      | Complexidade | 
| ------------- | ----------- | 
| Push  | O(1)        | 
| Pop | O(1)        | 
| Peek       | O(1)        | 


## Exemplo de uso

A seguir é apresentada uma implementação completa de uma pilha em Java.

```java
public class Stack {
    private Node top;
    private int size;

    private class Node {
        int value;
        Node next;

        Node(int value) {
            this.value = value;
        }
    }

    public void push(int value) {
        Node newNode = new Node(value);

        newNode.next = top;
        top = newNode;

        size++;
    }

    public int pop() {
        if (isEmpty()) {
            throw new RuntimeException("Pilha vazia");
        }

        int value = top.value;
        top = top.next;

        size--;
        return value;
    }

    public int peek() {
        if (isEmpty()) {
            throw new RuntimeException("Pilha vazia");
        }

        return top.value;
    }

    public boolean isEmpty() {
        return size == 0;
    }

    public void imprimir() {
        Node current = top;

        while (current != null) {
            System.out.print(current.value + " ");
            current = current.next;
        }

        System.out.println();
    }

    public static void main(String[] args) {
        Stack pilha = new Stack();

        pilha.push(10);
        pilha.push(20);
        pilha.push(30);

        pilha.imprimir(); // 30 20 10

        System.out.println("Removido: " + pilha.pop()); // 30

        pilha.imprimir(); // 20 10

        System.out.println("Topo: " + pilha.peek()); // 20
    }
}
```


## Exemplo de uso da Fila da plataforma Java

A classe Stack do Java implementa a estrutura de dados Pilha.

```java
import java.util.Stack;

public class ExemploPilha {

    public static void main(String[] args) {

        Stack<Integer> pilha = new Stack<>();

        pilha.push(10);
        pilha.push(20);
        pilha.push(30);

        System.out.println("Pilha: " + pilha);

        System.out.println("Topo: " + pilha.peek());

        System.out.println("Removido: " + pilha.pop());

        System.out.println("Pilha após remoção: " + pilha);
    }
}
```


## Conclusão

A pilha é uma estrutura baseada no princípio LIFO, sendo amplamente utilizada em chamadas de funções (recursão), avaliação de expressões e algoritmos como DFS. Sua implementação com lista encadeada garante eficiência e simplicidade, com operações principais em tempo constante.

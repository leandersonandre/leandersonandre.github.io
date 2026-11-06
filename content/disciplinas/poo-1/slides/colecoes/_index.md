---
title : "Coleções"
slug: "colecoes"
outputs : ["Reveal"]
reveal_hugo:
  theme: "serif"
  custom_css: "css/univille.css"
---

{{% slide-capa titulo="Coleções" subtitulo="Programação Orientada a Objetos I" %}}

___

# Coleções

{{% block titulo="Definição" %}}
Estruturas de dados utilizadas para armazenar e manipular grupos de elementos. O **Java Collections Framework** fornece interfaces e implementações para representar listas, conjuntos, filas e mapas, oferecendo operações como inserção, remoção, busca e iteração.

{{% /block %}}

___

# Java Collections Framework

{{< plantuml >}}
scale 0.8

interface Iterable
interface Collection
interface List
interface Set
interface Queue
interface Deque

abstract class AbstractCollection
abstract class AbstractList
abstract class AbstractSequentialList
abstract class AbstractSet
abstract class AbstractQueue

class ArrayList
class LinkedList
class Vector
class Stack

class HashSet
class LinkedHashSet
class TreeSet
class EnumSet

class PriorityQueue
class ArrayDeque

Iterable <|-- Collection

Collection <|-- List
Collection <|-- Set
Collection <|-- Queue

Queue <|-- Deque

Collection <|-- AbstractCollection

AbstractCollection <|-- AbstractList
AbstractCollection <|-- AbstractSet
AbstractCollection <|-- AbstractQueue

AbstractList <|-- AbstractSequentialList

List <|.. AbstractList
Set <|.. AbstractSet
Queue <|.. AbstractQueue

AbstractList <|-- ArrayList
AbstractSequentialList <|-- LinkedList
AbstractList <|-- Vector
Vector <|-- Stack

AbstractSet <|-- HashSet
HashSet <|-- LinkedHashSet
AbstractSet <|-- TreeSet
AbstractSet <|-- EnumSet

AbstractQueue <|-- PriorityQueue
AbstractQueue <|-- ArrayDeque
Deque <|.. ArrayDeque
Deque <|.. LinkedList


{{< /plantuml >}}


___

# Java Collections Framework



{{< plantuml >}}

interface Map
abstract class AbstractMap

class HashMap
class LinkedHashMap
class TreeMap
class WeakHashMap
class IdentityHashMap
class EnumMap
class Hashtable


Map <|.. AbstractMap

AbstractMap <|-- HashMap
HashMap <|-- LinkedHashMap
AbstractMap <|-- TreeMap
AbstractMap <|-- WeakHashMap
AbstractMap <|-- IdentityHashMap
AbstractMap <|-- EnumMap
AbstractMap <|-- Hashtable

{{< /plantuml >}}

___

# Listas

{{% block titulo="Definição" %}}
Estruturas de dados que representam sequências de elementos, nas quais a ordem é preservada, elementos podem se repetir e cada elemento possui uma posição.
{{% /block %}}

___

# Listas

Listas representam computacionalmente o **conceito matemático de sequência**.
<br>
<br>
<div style="display: flex; justify-content: center;">
<div style="display: flex; flex-direction: column; align-items: flex-start;">

  <div style="display: flex; gap: 0;">
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">10</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">25</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">30</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">45</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">60</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">30</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">-5</div>
  </div>

  <div style="width: 65px; text-align: center; font-size: 14px; padding-top: 6px;">
    Índice 0
  </div>

</div>
</div>

___

# Listas

A api de listas é definida na interface `java.util.List`.

{{< plantuml >}}

scale 1.2

interface List<E> {
    + add(element: E): boolean
    + add(index: int, element: E): void
    + get(index: int): E
    + set(index: int, element: E): E
    + remove(index: int): E
    + remove(element: Object): boolean
    + size(): int
    + isEmpty(): boolean
    + contains(element: Object): boolean
    + clear(): void
    + indexOf(element: Object): int
    + lastIndexOf(element: Object): int
    + iterator(): Iterator<E>
    + toArray(): Object[]
}

{{< /plantuml >}}


___

# Implementações de Listas

<table>
  <thead>
    <tr>
      <th>Implementação</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>ArrayList</code></td>
      <td>Armazena os elementos em um arranjo dinâmico, simulando um arranjo de tamanho variável.</td>
    </tr>
    <tr>
      <td><code>LinkedList</code></td>
      <td>Armazena os elementos em nós duplamente encadeados, facilitando o acesso ao primeiro e ao último elemento.</td>
    </tr>
  </tbody>
</table>

___

# ArrayList

Prefira utilizar a interface `List` para declarar variáveis, parâmetros e atributos, deixando a implementação (`ArrayList`) como detalhe da instanciação.

```java
import java.util.List;
import java.util.ArrayList;

// Criação de uma lista
List<Integer> lista = new ArrayList<>();

// Cria uma lista com capacidade inicial para 200 elementos.
List<Integer> lista2 = new ArrayList<Integer>(200);

// Inferência de tipos (variável do tipo ArrayList)
var lista3 = new ArrayList<Integer>();

```

___

# Adicionar elementos na lista

O método `add(elemento)`  adiciona o elemento ao final da lista.

```java
List<Integer> lista = new ArrayList<>();

lista.add(1);
lista.add(2);
lista.add(3);

```

<div style="display: flex; justify-content: center;">
<div style="display: flex; flex-direction: column; align-items: flex-start;">

  <div style="display: flex; gap: 0;">
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">1</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">2</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">3</div>
  </div>

</div>
</div>

___

# Adicionar elementos na lista

O método `add(index,elemento)`  adiciona o elemento em uma posição específica da lista, deslocando os elementos seguintes.


<div style="display: flex; justify-content: center;">
<div style="display: flex; flex-direction: column; align-items: flex-start;">

  <div style="display: flex; gap: 0;">
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">1</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">2</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">3</div>
  </div>

</div>
</div>

```java
List<Integer> lista = new ArrayList<>(List.of(1, 2, 3));

lista.add(1,99);
```

<div style="display: flex; justify-content: center;">
<div style="display: flex; flex-direction: column; align-items: flex-start;">

  <div style="display: flex; gap: 0;">
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">1</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #FF7F7F; display: flex; align-items: center; justify-content: center;">99</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">2</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">3</div>
  </div>

</div>
</div>

___

# Obter um elemento pela posição

O método `get(index)` retorna o elemento na posição `index`.

```java
List<Integer> lista = new ArrayList<>(List.of(1, 2, 3));

var elemento = lista.get(1);
System.out.println(elemento); // 2
```
___

# Atualizar um elemento pela posição

O método `set(index,elemento)` substitui o elemento na posição `index`. O método retorna o elemento substituído.

<div style="display: flex; justify-content: center;">
<div style="display: flex; flex-direction: column; align-items: flex-start;">

  <div style="display: flex; gap: 0;">
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">1</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">2</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">3</div>
  </div>

</div>
</div>

```java
List<Integer> lista = new ArrayList<>(List.of(1, 2, 3));

var substituido = lista.set(1,99);

System.out.println(substituido); // 2
System.out.println(lista.get(1)); // 99
```

<div style="display: flex; justify-content: center;">
<div style="display: flex; flex-direction: column; align-items: flex-start;">

  <div style="display: flex; gap: 0;">
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">1</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #FF7F7F; display: flex; align-items: center; justify-content: center;">99</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">3</div>
  </div>

</div>
</div>

___

# Remover um elemento pela posição

O método `remove(index)` remove o elemento na posição `index` e retorna o elemento removido. Os elementos seguintes são deslocados uma posição à esquerda.

<div style="display: flex; justify-content: center;">
<div style="display: flex; flex-direction: column; align-items: flex-start;">

  <div style="display: flex; gap: 0;">
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">1</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">2</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">3</div>
  </div>

</div>
</div>

```java
List<Integer> lista = new ArrayList<>(List.of(1, 2, 3));

var removido = lista.remove(1);

System.out.println(removido); // 2
System.out.println(lista.get(1)); // 3
```

<div style="display: flex; justify-content: center;">
<div style="display: flex; flex-direction: column; align-items: flex-start;">

  <div style="display: flex; gap: 0;">
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">1</div>
    <div style="width: 65px; height: 55px; border: 1px solid #36834A; background: #F3F8F3; display: flex; align-items: center; justify-content: center;">3</div>
  </div>

</div>
</div>


___

# Remoção por elemento

O método `remove(elemento)` remove a primeira ocorrência do elemento na lista e retorna `true` se a remoção for realizada. Os elementos seguintes são deslocados uma posição à esquerda.

```java
List<Integer> lista = new ArrayList<>(List.of(1, 2, 3));

lista.remove(1);                  // remove pela posição
lista.remove(Integer.valueOf(1)); // remove pelo valor

```
___

# Métodos úteis

```java
var lista = new ArrayList<Integer>();

// Verifica se a lista contém o elemento
// Retorna true ou false
var contem = lista.contains(99);

// Retorna o índice da primeira ocorrência
// Retorna -1 caso não encontre o elemento
var indice = lista.indexOf(99);
```
___

# Métodos úteis

```java
// Retorna o índice da última ocorrência
var indice = lista.lastIndexOf(99);

// Retorna a quantidade de elementos
var tamanho = lista.size();

// Verifica se a lista está vazia
boolean vazio = lista.isEmpty();

// Remove todos os elementos da lista
lista.clear();
```

___

# Percorrer a lista



A lista pode ser percorrida utilizando a estrutura de repetição `for` com índices, permitindo acessar cada elemento pela sua posição.

```java
var lista = new ArrayList<Integer>();

for(var i = 0; i < lista.size(); i++){
  System.out.println(lista.get(i));
}

```

___

# Percorrer a lista


A estrutura `for-each` permite percorrer todos os elementos da lista, do primeiro ao último, sem a necessidade de utilizar índices.

```java
var lista = new ArrayList<Integer>();

for(var elemento : lista){
  System.out.println(elemento);
}

```

___
# Acesso a posições inválidas

O acesso a uma posição inexistente da lista provoca a exceção `IndexOutOfBoundsException`.

Um índice válido deve estar entre `0` e `size() - 1`.

```java
List<Integer> lista = new ArrayList<>(List.of(10, 20, 30));

// Índice negativo
lista.get(-1); // IndexOutOfBoundsException

// Índice igual ao tamanho da lista
lista.get(3);  // IndexOutOfBoundsException

// Índice maior que o tamanho da lista
lista.get(10); // IndexOutOfBoundsException
```



___ 

{{% slide-contracapa %}}

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

# Conjuntos

{{% block titulo="Definição" %}}
Estruturas de dados que armazenam elementos distintos, sem estabelecer uma ordem entre eles.
{{% /block %}}

___

# Conjuntos

Conjuntos representam computacionalmente o **conceito matemático de conjunto**.

<br>

<div style="display: flex; justify-content: center;">
  <div style="
    width: 260px;
    height: 260px;
    border: 2px solid #36834A;
    border-radius: 50%;
    background: #F3F8F3;
    position: relative;
  ">
    <span style="position:absolute; top:25px; left:75px;">10</span>
    <span style="position:absolute; top:55px; right:55px;">25</span>
    <span style="position:absolute; top:115px; left:115px;">30</span>
    <span style="position:absolute; bottom:55px; left:65px;">45</span>
    <span style="position:absolute; bottom:35px; right:55px;">60</span>
    <span style="position:absolute; top:-12px; left:35px; color:#36834A; font-size:20px;"></span>
  </div>
</div>

___

# Conjuntos

A api de conjuntos é definida na interface `java.util.Set`.

{{< plantuml >}}

scale 1.2

interface Set<E> {
    + add(element: E): boolean
    + remove(element: Object): boolean
    + contains(element: Object): boolean
    + size(): int
    + isEmpty(): boolean
    + clear(): void
    + iterator(): Iterator<E>
    + toArray(): Object[]
}

{{< /plantuml >}}

___

# Implementações de Conjuntos


<table>
  <thead>
    <tr>
      <th>Implementação</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>HashSet</code></td>
      <td>Armazena elementos utilizando uma tabela hash, sem garantir a ordem dos elementos.</td>
    </tr>
    <tr>
      <td><code>LinkedHashSet</code></td>
      <td>Armazena elementos utilizando uma tabela hash, preservando a ordem de inserção.</td>
    </tr>
    <tr>
      <td><code>TreeSet</code></td>
      <td>Armazena elementos em uma árvore, mantendo-os ordenados.</td>
    </tr>
  </tbody>
</table>

___

# HashSet

Prefira utilizar a interface `Hash` para declarar variáveis, parâmetros e atributos, deixando a implementação (`HashSet`) como detalhe da instanciação.

```java
import java.util.Set;
import java.util.HashSet;

// Criação de um conjunto
Set<Integer> conjunto = new HashSet<>();

// Inferência de tipos (variável do tipo HashSet)
var conjunto2 = new HashSet<Integer>();

```

___

# Adicionar elementos no conjunto

O método `add(elemento)`  adiciona o elemento no conjunto.

```java
Set<Integer> conjunto = new HashSet<>();

conjunto.add(1);
conjunto.add(2);
conjunto.add(3);

```
<div style="display: flex; justify-content: center;">
  <div style="
    width: 190px;
    height: 190px;
    border: 2px solid #36834A;
    border-radius: 50%;
    background: #F3F8F3;
    position: relative;
  ">
    <div style="position: absolute; top: 40px; left: 45px;">1</div>
    <div style="position: absolute; top: 75px; right: 40px;">2</div>
    <div style="position: absolute; bottom: 40px; left: 85px;">3</div>
  </div>
</div>

___

# Verificar se um elemento existe

O método `contains(elemento)` retorna `true` se o conjunto contiver o elemento informado e `false` caso contrário.

```java
Set<Integer> conjunto = new HashSet<>(Set.of(1, 2, 3));

var resultado1 = conjunto.contains(1);  // true
var resultado2 = conjunto.contains(10); // false

```
<div style="display: flex; justify-content: center;">
  <div style="
    width: 190px;
    height: 190px;
    border: 2px solid #36834A;
    border-radius: 50%;
    background: #F3F8F3;
    position: relative;
  ">
    <div style="position: absolute; top: 40px; left: 45px;">1</div>
    <div style="position: absolute; top: 75px; right: 40px;">2</div>
    <div style="position: absolute; bottom: 40px; left: 85px;">3</div>
  </div>
</div>

___

# Remoção por elemento

O método `remove(elemento)` remove o elemento do conjunto e retorna `true` se ele existir e for removido, ou `false` caso contrário.

```java
Set<Integer> conjunto = new HashSet<>(Set.of(1, 2, 3));

var removido = lista.remove(1);

```
___

# Métodos úteis

```java

// Retorna a quantidade de elementos
var tamanho = conjunto.size();

// Verifica se a conjunto está vazia
boolean vazio = conjunto.isEmpty();

// Remove todos os elementos da conjunto
conjunto.clear();
```
___

# Percorrer o conjunto


A estrutura `for-each` permite percorrer todos os elementos do conjunto,  sem garantir uma ordem específica.

```java
Set<Integer> conjunto = new HashSet<>(Set.of(1, 2, 3));

for(var elemento : conjunto){
  System.out.println(elemento);
}

```

___

# Mapas

{{% block titulo="Definição" %}}
Os mapas são estruturas de dados que armazenam pares de elementos (chave, valor). Cada chave é única e utilizada para associar um determinado valor. Os valores podem se repetir.
{{% /block %}}

___

# Mapas

Conjuntos representam computacionalmente o **conceito matemático de funções**.

<br>

<div style="display: flex; justify-content: center; align-items: center; gap: 55px;">

  <!-- Chaves -->
  <div style="text-align: center;">
    <div style="color: #36834A; margin-bottom: 12px;">Chaves</div>
    <div style="width: 110px; height: 250px; border: 2px solid #36834A; border-radius: 50%; background: #F3F8F3; position: relative;">
      <span style="position:absolute; top:25px; left:48px;">1</span>
      <span style="position:absolute; top:95px; left:48px;">2</span>
      <span style="position:absolute; bottom:25px; left:48px;">3</span>
    </div>
  </div>

  <!-- Associações -->
  <div style="height: 250px; display: flex; flex-direction: column; justify-content: space-around; color: #36834A; font-size: 25px;">
    <span>⟶</span>
    <span>⟶</span>
    <span>⟶</span>
  </div>

  <!-- Valores -->
  <div style="text-align: center;">
    <div style="color: #36834A; margin-bottom: 12px;">Valores</div>
    <div style="width: 170px; height: 250px; border: 2px solid #36834A; border-radius: 50%; background: #F3F8F3; position: relative;">
      <span style="position:absolute; top:25px; left:35px;">Ana</span>
      <span style="position:absolute; top:95px; left:35px;">João</span>
      <span style="position:absolute; bottom:25px; left:35px;">Maria</span>
    </div>
  </div>

</div>

___

# Mapas

A api de mapas é definida na interface `java.util.Map`.

{{< plantuml >}}

scale 1.2

interface Map<K, V> {
    + put(key: K, value: V): V
    + get(key: Object): V
    + remove(key: Object): V
    + containsKey(key: Object): boolean
    + containsValue(value: Object): boolean
    + size(): int
    + isEmpty(): boolean
    + clear(): void
    + keySet(): Set<K>
    + values(): Collection<V>
    + entrySet(): Set<Map.Entry<K,V>>
}

{{< /plantuml >}}

___

# Implementações de Mapas


<table style="font-size: 0.8em;">
  <thead>
    <tr>
      <th>Implementação</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>HashMap</code></td>
      <td>Utiliza uma tabela hash, sem garantir a ordem dos elementos.</td>
    </tr>
    <tr>
      <td><code>LinkedHashMap</code></td>
      <td>Utiliza uma tabela hash, preservando a ordem de inserção.</td>
    </tr>
    <tr>
      <td><code>TreeMap</code></td>
      <td>Utiliza uma árvore, mantendo as chaves ordenadas.</td>
    </tr>
  </tbody>
</table>

___
# HashMap

Prefira utilizar a interface `Map` para declarar variáveis, parâmetros e atributos, deixando a implementação (`HashMap`) como detalhe da instanciação.

```java
import java.util.Map;
import java.util.HashMap;

// Criação de uma mapa
// Integer representa o tipo de dados da chave
// String representa o tipo de dados do valor
Map<Integer,String> mapa = new HashMap<>();

// Inferência de tipos (variável do tipo HashMap)
var mapa2 = new HashMap<Integer,String>();

```
___

# Adicionar pares no mapa

O método `add(chave,valor)`  adiciona o elemento no conjunto.

```java
Map<Integer,String> conjunto = new HashMap<>();

conjunto.add(1,"Argentina");
conjunto.add(2,"Brasil");
conjunto.add(3,"Chile");

```
<table style="margin: auto; font-size: 20px; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="color: #36834A;">Chaves</th>
      <th></th>
      <th style="color: #36834A;">Valores</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center; padding: 8px;">
        <div style="border: 2px solid #36834A; background: #F3F8F3; padding: 8px 18px;">1</div>
      </td>
      <td style="color: #36834A; text-align: center; padding: 8px 25px;">⟶</td>
      <td style="padding: 8px;">Argentina</td>
    </tr>
    <tr>
      <td style="text-align: center; padding: 8px;">
        <div style="border: 2px solid #36834A; background: #F3F8F3; padding: 8px 18px;">2</div>
      </td>
      <td style="color: #36834A; text-align: center; padding: 8px 25px;">⟶</td>
      <td style="padding: 8px;">Brasil</td>
    </tr>
    <tr>
      <td style="text-align: center; padding: 8px;">
        <div style="border: 2px solid #36834A; background: #F3F8F3; padding: 8px 18px;">3</div>
      </td>
      <td style="color: #36834A; text-align: center; padding: 8px 25px;">⟶</td>
      <td style="padding: 8px;">Chile</td>
    </tr>
  </tbody>
</table>

___

# Adicionar pares no mapa

O mapa não permite duplicar a chave. Ao adicionar uma chave existente, seu valor é substituído.

```java
Map<Integer,String> conjunto = new HashMap<>();

conjunto.add(1,"Argentina");
conjunto.add(1,"Brasil");
conjunto.add(1,"Chile"); 

```
<table style="margin: auto; font-size: 20px; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="color: #36834A;">Chaves</th>
      <th></th>
      <th style="color: #36834A;">Valores</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align: center; padding: 8px;">
        <div style="border: 2px solid #36834A; background: #F3F8F3; padding: 8px 18px;">1</div>
      </td>
      <td style="color: #36834A; text-align: center; padding: 8px 25px;">⟶</td>
      <td style="padding: 8px;">Chile</td>
    </tr>
  </tbody>
</table>

___

# Obter o valor pela sua chave

O método `get(chave)` retorna o valor associado a chave.  Caso a chave não exista no mapa, o método retorna `null`.

```java
Map<Integer, String> mapa = new HashMap<>(
    Map.of(
        1, "Argentina",
        2, "Brasil",
        3, "Chile"
    )
);

var valor = mapa.get(2); // Brasil
var valor2 = mapa.get(99); // null

```

___

# Obter o valor pela sua chave

O método `getOrDefault(chave,default)` retorna o valor associado à chave. Caso ela não exista no mapa, retorna o valor padrão informado.

```java
Map<Integer, String> mapa = new HashMap<>(
    Map.of(
        1, "Argentina",
        2, "Brasil",
        3, "Chile"
    )
);

var valor = mapa.getOrDefault(99,"País desconhecido"); 
// País desconhecido
System.out.println(valor);
```

___

# Verificar se existe uma chave

O método `containsKey(chave)` verifica se a chave existe no mapa. Retorna `true` caso existir. Caso contrário retorna `false`.


```java
Map<Integer, String> mapa = new HashMap<>(
    Map.of(
        1, "Argentina",
        2, "Brasil",
        3, "Chile"
    )
);

var valor1 = mapa.containsKey(1); // true
var valor2 = mapa.containsKey(2); // false
```

___

# Verificar se existe um valor

O método `containsValue(valor)` verifica se o valor existe no mapa. Retorna `true` caso existir. Caso contrário retorna `false`.


```java
Map<Integer, String> mapa = new HashMap<>(
    Map.of(
        1, "Argentina",
        2, "Brasil",
        3, "Chile"
    )
);

var valor1 = mapa.containsValue("Brasil");    // true
var valor2 = mapa.containsValue("Dinamarca"); // false
```

___

# Remover uma chave

O método `remove(chave)` remove a chave do mapa e retorna o valor associado.


```java
Map<Integer, String> mapa = new HashMap<>(
    Map.of(
        1, "Argentina",
        2, "Brasil",
        3, "Chile"
    )
);

var valor1 = mapa.remove(2);    // Brasil
```

___

# Métodos úteis

```java

// Retorna a quantidade de elementos
var tamanho = mapa.size();

// Verifica se a conjunto está vazia
boolean vazio = mapa.isEmpty();

// Remove todos os elementos do mapa
mapa.clear();
```
___

# Percorrer o mapa


A estrutura `for-each` permite percorrer todos os pares(chave,valor) do mapa,  sem garantir uma ordem específica.

```java
Map<Integer, String> mapa = new HashMap<>(
    Map.of(
        1, "Argentina",
        2, "Brasil",
        3, "Chile"
    )
);

// Percorre os pares
for(var par : mapa.entrySet()){
  System.out.println(par.getKey());
  System.out.println(par.getValue());
}

```

___

# Percorrer o mapa

```java

// Percorre as chaves
for(var chave : mapa.keySet()){
  System.out.println(chave);
}

// Percorre os valores
for(var valor : mapa.values()){
  System.out.println(valor);
}

```

___

# Comparação entre Lista, Conjunto e Mapa


<table style="font-size: 0.7em;">
  <thead>
    <tr>
      <th>Característica</th>
      <th>List</th>
      <th>Set</th>
      <th>Map</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Elementos repetidos</td>
      <td>Sim</td>
      <td>Não</td>
      <td>Chaves não</td>
    </tr>
    <tr>
      <td>Acesso por índice</td>
      <td>Sim</td>
      <td>Não</td>
      <td>Não</td>
    </tr>
    <tr>
      <td>Associação chave-valor</td>
      <td>Não</td>
      <td>Não</td>
      <td>Sim</td>
    </tr>
    <tr>
      <td>Ordem dos elementos</td>
      <td>Preservada</td>
      <td>Depende da implementação</td>
      <td>Depende da implementação</td>
    </tr>
  </tbody>
</table>

___ 

{{% slide-contracapa %}}

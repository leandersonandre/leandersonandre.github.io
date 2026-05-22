---
title: "Coleções"
slug: "colecoes"
description: "colecoes"
tags:
- colecoes
- arraylist
- hashset
- hashmap
---


## Definição

Coleções são estruturas de dados utilizadas para armazenar e manipular grupos de objetos. O framework Collections do Java fornece interfaces e implementações prontas para representar listas, conjuntos e mapas, oferecendo operações como inserção, remoção, busca e iteração. As principais coleções da biblioteca padrão estão disponíveis no pacote `java.util`.

Diagrama da API de coleções da linguagem Java.

{{< plantuml >}}
scale 0.7

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

## Listas

As listas são coleções de objetos onde é possível adicionar elementos repetidos e a ordem importa. A lista corresponde ao conceito matemático de sequência.
O Java possui a interface `List` para definir a estrutura de dados das listas e possui implementações de alguns tipos de listas, entre eles o `ArrayList`, `LinkedList` e `Vector`.

O `ArrayList` é a estrutura mais comum onde os elementos são armazenados dentro de um arranjo.

#### Criação da Lista

A lista pode ser definida através de uma variável do tipo `List`. As coleções do Java utilizam tipos genéricos, portanto é preciso indicar qual o tipo de dados que será armazenado na lista. Para este fim, se utiliza o operador diamante `<>` para indicar o tipo de dados. 

{{< tabs items="Diagrama,PlantUML" >}}
{{< tab >}}
{{< plantuml >}}

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

class ArrayList<E> {
    - elementData: Object[]
    - size: int

    + ArrayList()
    + ArrayList(initialCapacity: int)

    + ensureCapacity(minCapacity: int): void
    + trimToSize(): void
    + iterator(): Iterator<E>
}

List <|.r. ArrayList

{{< /plantuml >}}

{{< /tab >}}

{{< tab >}} Como criar o diagrama utilizando PlantUML

```
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

class ArrayList<E> {
    - elementData: Object[]
    - size: int

    + ArrayList()
    + ArrayList(initialCapacity: int)

    + ensureCapacity(minCapacity: int): void
    + trimToSize(): void
    + iterator(): Iterator<E>
}

List <|.r. ArrayList
```

{{< /tab >}}

{{< /tabs >}}

A instanciação da `List` deve ser feita através do tipo concreto, ou seja, a classe `ArrayList`.  

```java
// Criação de uma lista
List<Integer> lista = new ArrayList<Integer>();

// Cria um ArrayList com capacidade inicial para 200 elementos.
List<Integer> lista = new ArrayList<Integer>(200);

// Pode ser utilizado a inferência de tipos,
// porém o tipo de dados da variável é ArrayList
var lista = new ArrayList<Integer>();

```


#### Adicionar elementos

O método `add(elemento)` sempre adiciona no final da lista.

```java
var lista = new ArrayList<Integer>();

lista.add(1);
lista.add(2);
lista.add(3);

```

O método `add(index,elemento)` adiciona o elemento na posição `index`. Caso a posição não exista, uma exceção é lançada.

```java
var lista = new ArrayList<Integer>();
lista.add(1);
lista.add(2);
lista.add(3);

lista.add(1,99);

```

#### Obter um elemento pela posição

O método `get(index)` retorna o elemento na posição `index`. Caso a posição não exista, uma exceção é lançada.

```java
var lista = new ArrayList<Integer>();
lista.add(1);
lista.add(2);
lista.add(3);

lista.get(1);

```

#### Atualizar um elemento pela posição

O método `set(index,elemento)` substitui o elemento na posição `index`. O método retorna o elemento substituído. Caso a posição não exista, uma exceção é lançada.

```java
var lista = new ArrayList<Integer>();
lista.add(1);
lista.add(2);
lista.add(3);

var substituido = lista.set(1,99);

```


#### Remover elementos

O método `remove(index)` remove o elemento na posição `index`. O método retorna o elemento removido. Caso a posição não exista, uma exceção é lançada.

```java
var lista = new ArrayList<Integer>();
lista.add(1);
lista.add(2);
lista.add(3);

var removido = lista.remove(2);
```

#### Métodos úteis

O `List` fornece uma gama de métodos uteis, tais como size, clear, contains entre outros.

```java
var lista = new ArrayList<Integer>();


// Verifica se possui um elemento -
// true -> se possuir o elemento
// false -> se não possuir o elemento
var contem = lista.contains(99);

// Localiza o índice do elemento
// Retorna -1 caso não encontrar o elemento na lista
var indice = lista.indexOf(99);

// Retorna o índice do último elemento 99
var indice = lista.lastIndexOf(99);

// tamanho da lista
var tamanho = lista.size();

// Verificar se a lista está vazia
boolean vazio = lista.isEmpty();

// Limpar a lista / remover todos os elementos
lista.clear();
```

#### Percorrer a lista

A lista pode ser percorrida através da estrutura de repetição clássica com índices.

```java
var lista = new ArrayList<Integer>();

for(var i = 0; i < lista.size(); i++){
  System.out.println(lista.get(i));
}

```

A estrutura `for-each` pode ser utilizada para percorrer a lista. Esta estrutura sempre percorre do primeiro elemento até o último. Neste tipo de repetição, o índice não é conhecido.

```java
var lista = new ArrayList<Integer>();

for(var e : lista){
  System.out.println(e);
}

```

## Conjuntos

Os conjuntos são coleções de objetos em que não é permitido adicionar elementos repetidos e a ordem dos elementos não é garantida. A coleção conjunto funciona de forma semelhante aos conjuntos da matemática. 

O Java possui a interface Set para definir a estrutura de dados dos conjuntos e possui implementações de alguns tipos de conjuntos, entre eles o `HashSet`, `EnumSet`, `LinkedHashSet` e `TreeSet`.


O `HashSet` é a implementação mais comum da interface `Set`. Internamente, seus elementos são armazenados utilizando uma tabela hash.

#### Criação de um conjunto

Um conjunto pode ser definido por meio de uma variável do tipo `Set`.  A instanciação do conjunto deve ser feita através do tipo concreto, ou seja, a classe `HashSet`.


{{< tabs items="Diagrama,PlantUML" >}}
{{< tab >}}
{{< plantuml >}}


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

class HashSet<E> {
    - map: HashMap<E, Object>

    + HashSet()

}

Set <|.r. HashSet
{{< /plantuml >}}

{{< /tab >}}

{{< tab >}} Como criar o diagrama utilizando PlantUML

```


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

class HashSet<E> {
    - map: HashMap<E, Object>

    + HashSet()

}

Set <|.r. HashSet
```
{{< /tab >}}

{{< /tabs >}}


```java
Set<Integer> conjunto = new HashSet<Integer>();

var conjunto = new HashSet<Integer>();

```




#### Adicionar elementos

O método `add(elemento)`  adiciona o elemento no conjunto. O elemento é descartado caso já existir no conjunto.

```java

var conjunto = new HashSet<Integer>();
conjunto.add(1);
conjunto.add(2);
conjunto.add(3);

```

#### Verificar se um elemento existe

O método `contains(elemento)`  verifica se o elemento existe no conjunto. Caso existir, retorna `true`. Caso contrário, retorna `false`.

```java

var conjunto = new HashSet<Integer>();
var existe = conjunto.contains(1);

```

#### Remover elementos

O método `remove(elemento)`  remove o elemento no conjunto. O método retorna  `true` se o elemento existia no conjunto e foi removido. Caso contrário, retorna `false`.

```java

var conjunto = new HashSet<Integer>();
var foiRemovido = conjunto.remove(1);

```

#### Métodos úteis

O conjunto fornece uma gama de métodos uteis, tais como size, clear entre outros.

```java

var conjunto = new HashSet<Integer>();

// Verificar o tamanho
conjunto.size();

// Verificar se está vazio
var estaVazio = conjunto.isEmpty();

// Remover todos os elementos
conjunto.clear();

```

#### Percorrer o conjunto

O conjunto não possui o conceito de posições ou sequência dos elementos. Para percorrer os elementos de um conjunto, utiliza-se um `Iterator`.


```java

var conjunto = new HashSet<Integer>();
conjunto.add(1);
conjunto.add(10);
conjunto.add(100);

for(var e : conjunto){
  System.out.println(e);
}

```

## Mapas

Os mapas são coleções de objetos em que uma chave é utilizada para associar um determinado valor. A coleção mapa funciona de forma semelhante aos dicionários.
O Java possui a interface `Map` para definir a estrutura de dados dos mapas e disponibiliza implementações de diferentes tipos de mapas, entre elas `HashMap`, `LinkedHashMap` e `TreeMap`.
O `HashMap` é a implementação mais comum, em que os elementos são armazenados em uma estrutura baseada em tabela hash.

#### Criação de um mapa


{{< tabs items="Diagrama,PlantUML" >}}
{{< tab >}}
{{< plantuml >}}


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

class HashMap<K, V> {
    - table: Node<K,V>[]
    - size: int
    - loadFactor: float

    + HashMap()

}

Map <|.r. HashMap


{{< /plantuml >}}

{{< /tab >}}

{{< tab >}} Como criar o diagrama utilizando PlantUML

```


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

class HashMap<K, V> {
    - table: Node<K,V>[]
    - size: int
    - loadFactor: float

    + HashMap()

}

Map <|.r. HashMap


```
{{< /tab >}}

{{< /tabs >}}

O mapa possui dois tipos genéricos. O `K` representa o tipos de dado da chave e o `V` representa o tipo de dado do valor.

```java
// Map<K,V>
Map<Integer,String> mapa = new HashMap<Integer,String>();

var mapa = new HashMap<Integer,String>();

```

#### Adicionando um par de elementos

O método `put(chave,valor)`  adiciona o par (chave, valor) no mapa. Caso a chave já exista no mapa, o valor é substituído.

```java

var mapa = new HashMap<Integer,String>();

mapa.put(1,"Brasil");
mapa.put(2,"Argentina");

```

#### Obter o elemento pela sua chave

O método `get(chave)`  retorna o valor associado a chave. Caso a chave não exista no mapa, o método retorna `null`.

```java

var mapa = new HashMap<Integer,String>();

mapa.put(1,"Brasil");
var valor = mapa.get(1);

valor = mapa.get(99);

```

O método `getOrDefault(chave,default)`  retorna o valor associado a chave. Caso a chave não exista no mapa, o método retorna `default`.

```java

var mapa = new HashMap<Integer,String>();
var valor = mapa.getOrDefault(1,"Não encontrado");

```

#### Verificar se existe uma chave

O método `containsKey(chave)`  verifica se a chave existe no mapa. Retorna `true` caso existir. Caso contrário retorna `false`.

```java

var mapa = new HashMap<Integer,String>();
var chaveExiste = mapa.containsKey(1);

```


#### Verificar se existe um elemento (valor)

O método `containsValue(valor)`  verifica se um elemento existe no mapa. Retorna `true` caso existir. Caso contrário retorna `false`.

```java

var mapa = new HashMap<Integer,String>();
var elementoExiste = mapa.containsValue("Brasil");

```

#### Remover uma chave

O método `remove(chave)`  remove a chave do mapa e retorna o valor associado.

```java

var mapa = new HashMap<Integer,String>();
var valor = mapa.remove(1);

```

#### Métodos úteis

O mapa fornece uma gama de métodos uteis, tais como size, clear entre outros.

```java

var mapa = new HashMap<Integer,String>();

// Verificar o tamanho
mapa.size();

// Verificar se está vazio
var estaVazio = mapa.isEmpty();

// Remover todos os elementos
mapa.clear();

```

#### Percorrendo um mapa


O mapa não possui o conceito de posições ou sequência dos elementos. Para percorrer os elementos de um mapa, utiliza-se um `Iterator`.

O mapa permite percorrer o conjunto de chaves, valores e os pares (chave,valor).

```java

var mapa = new HashMap<Integer,String>();

// Percorrer as chaves
for(var chave : mapa.keySet()){
  System.out.println(chave);
}

// Percorrer os valores
for(var valor : mapa.values()){
  System.out.println(valor);
}

// Percorrer os pares (chave,valor)
for(var par : mapa.entrySet()){
  System.out.println(par.getKey());
  System.out.println(par.getValue());
}

```

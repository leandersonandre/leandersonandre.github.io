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



## Listas

As listas são coleções de objetos onde é possível adicionar elementos repetidos e a ordem importa. A lista é relacionado com a sequência da matemática.
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

A instanciação da `List` deve ser feito através do tipo concreto, ou seja, a classe `ArrayList`.  

```java
// Criação de uma lista
List<Integer> lista = new ArrayList<Integer>();

// Cria um arraylist com um arranjo de tamanho 200 para guardar os elementos.
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

lista.add(1,99);

```

#### Obter um elemento pela posição

O método `get(index)` retorna o elemento na posição `index`. Caso a posição não exista, uma exceção é lançada.

```java
var lista = new ArrayList<Integer>();

lista.get(1);

```

#### Atualizar um elemento pela posição

O método `set(index,elemento)` substitui o elemento na posição `index`. O método retorna o elemento substituído. Caso a posição não exista, uma exceção é lançada.

```java
var lista = new ArrayList<Integer>();

var substituido = lista.set(1,99);

```


#### Remover elementos

O método `remove(index)` remove o elemento na posição `index`. O método retorna o elemento removido. Caso a posição não exista, uma exceção é lançada.

```java
var lista = new ArrayList<Integer>();

var removido = lista.remove(99);
```

#### Métodos úteis

O `List` fornece uma gama de métodos uteis, tais como size, clear, contains entre outros.

```java
var lista = new ArrayList<Integer>();


// Verifica se possui um elemento -
// true -> se possuir o elemento
// false -> se não possuir o elemento
var contem = list.contains(99);

// Localiza o índice do elemento
// Retorna -1 caso não encontrar o elemento na lista
var indice = list.indexOf(99);

// Retorna o índice do último elemento 99
var indice = list.lastIndexOf(99);

// tamanho da lista
var tamanho = list.size();

// Verificar se a lista está vazia
boolean vazio = list.isEmpty();

// Limpar a lista / remover todos os elementos
list.clear();
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

Os conjuntos são coleções de objetos onde não é possível adicionar elementos repetidos e a ordem não importa. A coleção conjunto funciona da mesma maneira que os conjuntos na matemática.

O Java possui a interface Set para definir a estrutura de dados dos conjuntos e possui implementações de alguns tipos de conjuntos, entre eles o `HashSet`, `EnumSet`, `LinkedSet` e `TreeSet`.

O `HashSet` é a estrutura mais comum onde os elementos são armazenados dentro de um mapa.

#### Criação de um conjunto

O conjunto pode ser definida através de uma variável do tipo `Set`.  A instanciação do conjunto deve ser feito através do tipo concreto, ou seja, a classe `HashSet`.


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

O conjunto não possui o conceito de posições ou sequência. Para percorrer um conjunto, é utilizado o `Iterator`.


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

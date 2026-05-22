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


### Definição



### Listas

As listas são coleções de objetos onde é possível adicionar elementos repetidos e a ordem importa. A lista é relacionado com a sequência da matemática.
O Java possui a interface `List` para definir a estrutura de dados das listas e possui implementações de alguns tipos de listas, entre eles o `ArrayList`, `LinkedList` e `Vector`.

O `ArrayList` é a estrutura mais comum onde os elementos são armazenados dentro de um arranjo.

#### Criação da Lista

A lista pode ser definida através de uma variável do tipo `List`. As coleções do Java utilizam tipos genéricos, portanto é preciso indicar qual o tipo de dados que será armazenado na lista. Para este fim, se utiliza o operador diamante `<>` para indicar o tipo de dados. 

A instanciação da `List` deve ser feito através do tipo concreto, ou seja, a classe `ArrayList`.  

```java
// Criação de uma lista
List<Integer> lista = new ArrayList<Integer>();

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

#### Métodos uteis

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

### Conjuntos

### Mapas

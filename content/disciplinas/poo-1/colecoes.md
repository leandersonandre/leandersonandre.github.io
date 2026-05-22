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

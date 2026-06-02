---
title: "Enumerações"
slug: "enums"
description: "Tipo Enum"
tags:
- enum
---


## Definição

*Enumerações* são um tipo especial de classe que define um conjunto finito de objetos imutáveis nomeados, chamado de enumeradores.


## Implementação de enumerações no Java

A palavra reservada `enum` define o tipo de dados enumeração. Os enumeradores são identificados com todas as letras em caixa alta.

```java
public enum Prioridade{
  BAIXA,
  MEDIA,
  ALTA,
  URGENTE
}
```

Cada enumerador possui como tipo a própria enumeração. Assim, o tipo do enumerador `BAIXA` é `Prioridade`. Ao ser convertido para texto, o enumerador produz seu próprio nome.

```java
Prioridade p = Prioridade.BAIXA;

// BAIXA
System.out.println(p);
```

Um enumerador não pode ser instanciado com o operador `new`. O valor de uma variável deve ser definida a partir do objeto constante na enumeração. Como cada enumerador possui uma única instância, é seguro compará-los com o operador  `==`.

```java
Prioridade p = Prioridade.ALTA;

if(p == Prioridade.ALTA){
  System.out.println("A prioridade é alta");
}
```

### Método values

O método `values`  retorna um arranjo contendo todos os enumeradores definidos na enumeração.

```java
for(var enumerador : Prioridade.values()){
  System.out.println(enumerador);
}
```

### Método valueOf

O método `valueOf`  retorna o enumerador cujo nome corresponde à `String` informada por parâmetro.

```java
var prioridade = Prioridade.valueOf("ALTA");
System.out.println(prioridade);
```

Caso não existir uma enumeração que corresponde à `String` informada por parâmetro, uma exceção será lançada.

### Construtores, atributos e métodos

As enumerações podem possuir construtores, atributos e métodos assim como as outras classes. Os construtores de uma enumeração são privados e não podem ser invocados diretamente com o operador `new`. Quando a enumeração define um construtor com parâmetros, é necessário informar os valores correspondentes para cada enumerador.

```java
public enum Prioridade{
  BAIXA(0),
  MEDIA(1),
  ALTA(2),
  URGENTE(3);

  private int valor;

  private Prioridade(int valor){
    this.valor = valor;
  }
  
  public int valor(){
    return valor;
  }
}
```

Os construtores de enumerações são privados e não podem ser invocados diretamente com o operador `new`. Cada enumerador é criado durante a inicialização da enumeração e recebe os valores definidos em sua declaração.

```java
// Imprime 2
System.out.println(Prioridade.ALTA.valor());
```

### Uso em estruturas `switch`

Enumerações podem ser utilizadas em estruturas `switch`, permitindo executar comportamentos diferentes para cada enumerador.

```java
Prioridade prioridade = Prioridade.ALTA;

switch (prioridade) {
  case BAIXA:
    System.out.println("Prioridade baixa");
    break;

  case MEDIA:
    System.out.println("Prioridade média");
    break;

  case ALTA:
    System.out.println("Prioridade alta");
    break;

  case URGENTE:
    System.out.println("Prioridade urgente");
    break;
}
```

Ao utilizar uma enumeração em um `switch`, os rótulos `case` devem utilizar apenas o nome dos enumeradores, sem o prefixo do tipo.

```java
// Correto
case ALTA:

// Incorreto
case Prioridade.ALTA:
```

## Representação de Enumerações na UML

Nos diagramas de classe da UML, as enumerações são representadas pelo estereótipo `enumeration`. Por convenção, os enumeradores são escritos em caixa alta.

{{< tabs items="Diagrama,PlantUML" >}}
{{< tab >}}
{{< plantuml >}}
enum Prioridade <<enumeration>> {
  BAIXA
  MEDIA
  ALTA
  URGENTE
}
{{< /plantuml >}}
{{< /tab >}}
{{< tab >}}
Como criar o diagrama utilizando PlantUML.
```plantuml
enum Prioridade <<enumeration>> {
  BAIXA
  MEDIA
  ALTA
  URGENTE
}
```
{{< /tab >}}

{{< /tabs >}}

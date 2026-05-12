---
title: "Classes Abstratas"
slug: "classes-abstratas"
description: "Classes Abstratas"
tags:
- classes-abstrata
---


### Definição

Uma classe abstrata é um tipo de classe que não pode ser instanciada diretamente e que permite definir métodos abstratos (sem implementação) e métodos concretos (com implementação).

Os métodos abstratos devem obrigatoriamente ser implementados pelas classes que herdam dessa classe.

### Objetivos

A classe abstrata permite:

* Abstração de código
* Permitir  o uso  do polimorfismo
* Desacoplamento entre as classes


#### Representação em diagrama de classes da UML.

{{< tabs items="Diagrama,PlantUML" >}}



{{< tab >}}
Observe que o nome da classe abstrata está em itálico.
O método ```area()```  é um método abstrato, portanto está em itálico.

{{< plantuml>}}
abstract class Shape  {
  {abstract} +area() : double
  +getName(): String
}
{{< /plantuml>}}

{{< /tab >}}

{{< tab >}}
Como criar o diagrama utilizando PlantUML
```
abstract class Shape  {
  {abstract} +area() : double
  +getName(): String
}
```
{{< /tab >}}

{{< /tabs >}}

#### Código Java

A classe abstrata é definida com a palavra-reservada ```abstract```.
Os métodos abstratos devem ser indicados com esta palavra chave.

```java
public abstract class Shape{
  public abstract double area();
}

```

A classe abstrata pode possuir atributos e métodos como uma classe regular.

```java
public abstract class Shape{
  private String name;
  public abstract double area();
  public String getName(){
    return name;
  }
}

```

### Implementação

A classe abstrata não pode ser instanciada, portanto, deve ser realizada herança. Na classe filha, os métodos abstratos devem ser implementados.

#### Passo 1

Indicar na classe a herança de classe abstrata. Após o nome da classe utilize a palavra-chave **extends**.

```java
class Rect extends Shape{
  
}

```

#### Passo 2

A classe obrigatoriamente deve implementar todos os métodos abstratos da classe abstrata. Recomenda-se sempre utilizar a anotação **@Override** nos métodos implementados.

```java
class Rect extends Shape{
   @Override
   public double area(){
     return 0;
   }
}

```

### Instanciação

Um objeto não pode ser criado a partir de uma classe abstrata. Deve ser sempre instanciado um objeto da classe que estenda a  classe abstrata.

```java
// ERRADO
Shape s = new Shape();

// CERTO
Rect r = new Rect();
```

### Polimorfismo

Um objeto de uma classe que extende uma classe abstrata pode ser referenciado por uma variável do tipo da classe abstrata. O uso de classes abstratas facilita a aplicação do polimorfismo.

```java
Shape s = new Rect();

// Retornar ao objeto original,
// deve ser utilizado o operador de casting

Rect r = (Rect) s;
```

O casting só é seguro quando o objeto realmente é do tipo convertido.
A conversão do objeto para um tipo que ele não pertença causará o erro de **ClassCastException**.


### Múltiplas heranças de classe abstrata

A linguagem java não permite a herança de múltiplas classes.

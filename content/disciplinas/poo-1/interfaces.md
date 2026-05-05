---
title: "Interfaces"
slug: "interfaces"
description: "Interfaces"
tags:
- interface
---


### Definição

Um contrato que define um conjunto de métodos que uma classe deve implementar, sem fornecer a implementação desses métodos.

Diferente da herança, interfaces definem contratos que podem ser implementados por diferentes classes, permitindo maior flexibilidade e desacoplamento.

### Objetivos

A interface permite:

* Abstração de código
* Ativar o mecanismo de polimorfismo
* Desacoplamento entre as classes


#### Representação em diagrama de classes da UML.

{{< plantuml>}}
interface Printable  <<interface>> {
  +print()
}

{{< /plantuml>}}

#### Código Java

Por padrão, os métodos em uma interface são públicos e abstratos, ou seja, não possuem um corpo(implementação).
No entanto, a partir do Java 8, interfaces também podem possuir métodos default e static com implementação.

```java
public interface Printable{
  void print();
}

```

A interface pode possuir atributos, porém são sempre públicos, estáticos (escopo de classe) e finais (constantes).

```java
public interface Constants{
  double PI = 3.1415;
}

```

### Implementação

Os métodos devem ser implementados/realizados em uma classe concreta.

#### Passo 1

Indicar na classe a implementação/realização de interface. Após o nome da classe utilize a palavra-chave **implements**.

```java
class Person implements Printable{
  private String name;
  // getters e setters ocultos
}

```

#### Passo 2

A classe obrigatoriamente deve implementar todos os métodos da interface. Recomenda-se sempre utilizar a anotação **@Override** nos métodos implementados.

```java
class Person implements Printable{

  private String name;

  @Override
  public void print(){
    System.out.println("Name: " + name);
  }
}

```

### Instanciação

Um objeto não pode ser criado a partir de uma interface. Deve ser sempre instanciado um objeto que implementa a interface.

```java
// ERRADO
Printable c = new Printable();

// CERTO
Person p = new Person();
```

### Polimorfismo

Um objeto que implementa uma interface pode ser referenciado por uma variável do tipo da interface. O polimorfismo é um dos objetivos de se utilizar interfaces.

```java
Printable c = new Person();

// Retornar ao objeto original,
// deve ser utilizado o operador de casting

Person p = (Person) c;
```

O casting só é seguro quando o objeto realmente é do tipo convertido.
A conversão do objeto para um tipo que ele não pertença causará o erro de **ClassCastException**.


### Múltiplas realizações de interface

Uma classe pode realizar a implementação de múltiplas interfaces.

{{< plantuml>}}
interface Printable  <<interface>> {
  +print()
}

interface Cloneable  <<interface>> {
  
}

class Person{
}

Printable <|.. Person
Cloneable <|.. Person

{{< /plantuml>}}

Os nomes das interfaces implementadas são separadas pela vírgula.

```java
class Person implements Printable, Cloneable{

  private String name;

  @Override
  public void print(){
    
  }
}

```

Interfaces podem definir métodos com a mesma assinatura. 
Quando esses métodos possuem implementação (default), podem ocorrer conflitos que devem ser resolvidos pela classe. Esse problema é conhecido como "diamond problem" (problema do diamante).


```java
interface A {
  default void print() {
    System.out.println("A");
  }
}

interface B {
  default void print() {
    System.out.println("B");
  }
}

class Person implements A, B {
  @Override
  public void print() {
    A.super.print(); // resolve conflito
  }
}
```

### Herança de interfaces

As interfaces podem realizar uma ou múltiplas heranças de outras interfaces.

{{< plantuml>}}
interface Printable  <<interface>> {
  +print()
}

interface Cloneable  <<interface>> {
  
}
Cloneable <|-- Printable

{{< /plantuml>}}

Na implementação, se utiliza a palavra-chave **extends** para indicar herança de interfaces. 

```java
interface Cloneable{

}

interface Printable extends Cloneable{
  void print();
}

```


### Interface na linguagem Java

A linguagem Java fornece recursos extras na criação de interfaces.

#### Método default

O método default permite adicionar uma implementação padrão em um método da interface. Caso a classe que implementa a interface não sobrescreva o método, será utilizado o método default da interface.

```java
public interface Printable{
  default void print(){
     System.out.println("Hello print");
  }
}

public class Person implements Printable{

  // Não é obrigatório implementar o método print
}

```

#### Método static
Interfaces também podem possuir métodos estáticos. Esses métodos pertencem à própria interface e não às classes que a implementam.
Diferente dos métodos **default**, métodos **static** não são herdados pelas classes que implementam a interface.

```java
public interface Printable{

  static void printMessage(){
    System.out.println("Printing...");
  }
}
```

**Utilização:**  O método estático deve ser acessado diretamente pela interface:
```java
Printable.printMessage();
```
Não é possível acessar o método estático a partir de uma instância da classe:
```java
Printable p = new Person();

// ERRADO
p.printMessage();
```

**Observação:** Métodos estáticos em interfaces são geralmente utilizados para:

* métodos utilitários relacionados à interface
* métodos auxiliares
* criação de objetos (factory methods, em alguns casos)

---
title: "Imutabilidade"
slug: "imutabilidade"
description: "imutabilidade"
tags:
- imutabilidade
- record
---


## Definição

A **imutabilidade** é uma técnica de desenvolvimento de software na qual um objeto não pode ter seu estado alterado após sua criação. A imutabilidade é um dos conceitos fundamentais da programação funcional.


### Objeto mutável

Um objeto comum na orientação a objetos pode ter seu estado interno alterado ao longo do tempo, geralmente por meio de métodos `setters`. Essa é uma característica frequentemente desejável em sistemas que precisam atualizar informações durante sua execução.

```java
class Person{
  private String name;
  public void setName(String name){
    this.name = name;
  }
  public String getName(){
    return name;
  }
}

Person person = new Person();
person.setName("Tom Cruise");

// Tom Cruise
System.out.println(person.getName());

person.setName("Daniel Craig");
// Daniel Craig
System.out.println(person.getName());
```

Nesse exemplo, o objeto `person` é mutável, pois seu atributo `name` pode ser alterado várias vezes após a criação do objeto.


### Objeto imutável

Em um objeto imutável, o estado é definido no momento da criação e não pode ser modificado posteriormente.

```java
class Person {
    private final String name;

    public Person(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }
}

Person person = new Person("Tom Cruise");

// Tom Cruise
System.out.println(person.getName());

```

Como não existe um método `setName()` e o atributo é `final`, o nome não pode ser alterado após a criação do objeto. Para ter uma pessoa com outro nome, seria necessário criar uma nova instância:

```java
Person anotherPerson = new Person("Daniel Craig");
```

Assim, a imutabilidade garante que o estado do objeto permaneça consistente durante toda a sua existência.


## Imutabilidade na linguagem Java


A linguagem Java oferece diversos recursos que facilitam a criação de objetos imutáveis. A ideia principal é garantir que os atributos de uma classe sejam definidos durante a construção do objeto e não possam ser modificados posteriormente.


### Palavra reservada final

A palavra reservada `final`  é um dos principais recursos utilizados para implementar imutabilidade em Java. Quando aplicada a um atributo, ela garante que sua referência ou valor só possa ser atribuído uma única vez.


Após a inicialização, qualquer tentativa de reatribuição resultará em erro de compilação.

```java
class Person {
    private final String name;

    public Person(String name) {
        this.name = name;
    }

    public String getName() {
        return name;
    }
}
```

No exemplo acima, o atributo `name` deve receber um valor durante a construção do objeto e não poderá ser alterado posteriormente.

```java
Person person = new Person("Tom Cruise");

// Erro de compilação
person.name = "Daniel Craig";
```

É importante destacar que o final impede apenas a reatribuição da variável. Quando o atributo referencia um objeto mutável, o estado interno desse objeto ainda pode ser alterado.


```java
class Team {
    private final List<String> members = new ArrayList<>();

    public List<String> getMembers() {
        return members;
    }
}

Team team = new Team();

team.getMembers().add("Tom Cruise");
```

Nesse caso, a referência `members` não pode apontar para outra lista, mas os elementos da lista ainda podem ser modificados. Por isso, o uso de `final` sozinho não garante a imutabilidade completa de uma classe.


Para construir objetos verdadeiramente imutáveis, é comum combinar `final` com outras práticas, como a ausência de métodos setters e o uso de cópias defensivas para atributos mutáveis.

### Práticas comuns para garantir a imutabilidade

Uma classe imutável deve garantir que seus atributos não possam ser modificados, para isto, a classe deve:

* Declarar os atributos como `private` e `final`.
* Inicializar todos os atributos no construtor.
* Não fornecer métodos modificadores (*setters*).
* Em atributos mutáveis (como listas, arrays e datas), realizar cópias defensivas para evitar alterações externas.


Uma classe imutável pode omitir o prefixo `get` dos métodos de acesso (*getters*), adotando uma nomenclatura mais concisa. Essa abordagem é comum em APIs modernas e foi popularizada pelos **records**  do Java.

```java
class Person {
    private final String name;

    public Person(String name) {
        this.name = name;
    }

    public String name() {
        return name;
    }
}

Person person = new Person("Tom Cruise");
System.out.println(person.name());
```

O método `name()` apenas retorna o valor do atributo, sem sugerir que ele possa ser modificado. Como a classe é imutável, não há necessidade de expor métodos *setters*.


## Representação da imutabilidade na UML

Nos diagramas de classe da UML, a imutabilidade é representada pela propriedade `readOnly`.

{{< tabs items="Diagrama,PlantUML" >}}
{{< tab >}}
{{< plantuml >}}
class Person {
     -name : String {readOnly}
    + Person(name : String)
    + name() : String
}
{{< /plantuml >}}
{{< /tab >}}
{{< tab >}}
Como criar o diagrama utilizando PlantUML.
```plantuml
class Person {
    -name : String {readOnly} 
    + Person(name : String)
    + name() : String
}
```
{{< /tab >}}

{{< /tabs >}}


## Modificação de objetos imutáveis

Os objetos imutáveis não sofrem alterações em suas operações. Quando é necessário realizar alguma modificação em um objeto imutável, a operação cria uma nova instância contendo o estado atualizado, preservando o objeto original.

```java
class Person {
    private final String firstName;
    private final String lastName;

    public Person(String firstName, String lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }

    public String firstName() {
        return firstName;
    }

    public String lastName() {
        return lastName;
    }

    public Person withLastName(String lastName) {
        return new Person(this.firstName, lastName);
    }
}

Person person = new Person("Tom", "Cruise");

Person updatedPerson = person.withLastName("Hanks");

System.out.println(
    person.firstName() + " " + person.lastName()
);
// Tom Cruise

System.out.println(
    updatedPerson.firstName() + " " + updatedPerson.lastName()
);
// Tom Hanks
```

Observe que o objeto original permanece inalterado. A operação cria uma nova instância com o sobrenome modificado, preservando a imutabilidade da classe.

Esse padrão, conhecido como **copy-on-write** ou **with methods**, é amplamente utilizado em classes imutáveis, pois permite realizar alterações sem comprometer a integridade do objeto original.


## Tipo records

A linguagem Java fornece o tipo especial `record` para representar objetos cujo principal objetivo é armazenar dados. Os *records* reduzem significativamente a quantidade de código necessária para criar classes imutáveis.


Considere a seguinte classe imutável:


```java
class Person {
    private final String firstName;
    private final String lastName;

    public Person(String firstName, String lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }

    public String firstName() {
        return firstName;
    }

    public String lastName() {
        return lastName;
    }
}
```

A mesma classe pode ser escrita utilizando um `record`:

```java
public record Person(String firstName, String lastName) {
}
```

Ao declarar um `record`, o compilador gera automaticamente:

* Os atributos privados e finais.
* Um construtor com todos os atributos.
* Métodos de acesso para cada atributo.
* Os métodos `equals()`, `hashCode()` e `toString()`.


Os componentes de um `record` são implicitamente `final`, o que significa que seus valores não podem ser alterados após a criação da instância.

Caso seja necessário "modificar" um objeto, uma nova instância deve ser criada:

```java
Person person = new Person("Tom", "Cruise");

Person updatedPerson =
    new Person(person.firstName(), "Hanks");

System.out.println(person);
// Person[firstName=Tom, lastName=Cruise]

System.out.println(updatedPerson);
// Person[firstName=Tom, lastName=Hanks]
```

Por sua simplicidade e suporte nativo à imutabilidade, os records são amplamente utilizados para representar objetos de transferência de dados (*DTOs*), parâmetros de entrada, respostas de APIs e outros tipos de objetos cujo estado não deve ser alterado após a criação.


### Representação de records na UML

O tipo record é representado no diagrama de classes da UML com o estereótipo `record`.

{{< tabs items="Diagrama,PlantUML" >}}
{{< tab >}}
{{< plantuml >}}
class Pessoa <<record>> {
    nome : String
    idade : int
}
{{< /plantuml >}}
{{< /tab >}}
{{< tab >}}
Como criar o diagrama utilizando PlantUML.
```plantuml
class Pessoa <<record>> {
    nome : String
    idade : int
}
```
{{< /tab >}}

{{< /tabs >}}


## Tipos imutáveis na plataforma Java

A plataforma Java oferece alguns tipos de dados imutáveis, entre eles estão:

* String
* Tipos relacionados a tempo e data: LocalDate, LocalTime, LocalDateTime, Instant, Duration e Period.
* BigDecimal
* BigInteger
* UUID


## Benefícios da imutabilidade

A utilização de objetos imutáveis traz diversas vantagens:

* Maior previsibilidade do comportamento do sistema.
* Menor risco de alterações acidentais de estado.
* Facilidade de compartilhamento entre múltiplas threads.
* Código mais simples de testar e depurar.
* Melhor encapsulamento dos dados.

Por esses motivos, a imutabilidade é amplamente utilizada em aplicações modernas e é considerada uma boa prática sempre que os objetos não precisarem sofrer alterações após sua criação.

## Imutabilidade e programação funcional

A programação funcional favorece estruturas de dados imutáveis.
Em vez de alterar objetos existentes, operações produzem novos objetos contendo o estado desejado.

Esse modelo reduz efeitos colaterais e facilita o raciocínio sobre o comportamento do sistema.

Muitos recursos modernos do Java, como Stream, Optional, Record e a API java.time, foram influenciados por conceitos da programação funcional e fazem amplo uso da imutabilidade.

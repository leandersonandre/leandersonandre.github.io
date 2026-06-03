---
title: "Questões sobre Interfaces"
slug: "interfaces-questoes"
description: "Questões sobre interfaces"
tags:
- questões
- interfaces
---


{{< lista-questoes >}}

{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
interface Animal {
  emitirSom() : void
}
{{< /plantuml >}}

Qual alternativa está correta?

{{< alternativa >}} Animal é uma classe abstrata. {{< /alternativa >}}
{{< alternativa >}} Animal é uma interface. {{< /alternativa >}}
{{< alternativa >}} emitirSom é um atributo. {{< /alternativa >}}
{{< alternativa >}} Animal é uma classe concreta. {{< /alternativa >}}

{{< solucao letra="B" >}}
O diagrama indica explicitamente uma interface.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
interface Forma {
  calcularArea() : double
}
{{< /plantuml >}}

Qual é o tipo de retorno do método calcularArea?

{{< alternativa >}} int {{< /alternativa >}}
{{< alternativa >}} void {{< /alternativa >}}
{{< alternativa >}} double {{< /alternativa >}}
{{< alternativa >}} String {{< /alternativa >}}

{{< solucao letra="C" >}}
O retorno indicado no diagrama é do tipo <code>double</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
interface Imprimivel {
  imprimir() : void
}

class Relatorio

Imprimivel <|.. Relatorio
{{< /plantuml >}}

Qual alternativa está correta?

{{< alternativa >}} Imprimivel herda de Relatorio. {{< /alternativa >}}
{{< alternativa >}} Relatorio implementa Imprimivel. {{< /alternativa >}}
{{< alternativa >}} Relatorio é uma interface. {{< /alternativa >}}
{{< alternativa >}} imprimir é um atributo. {{< /alternativa >}}

{{< solucao letra="B" >}}
A linha tracejada com triângulo indica implementação de interface.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
interface Autenticavel {
  autenticar(login:String, senha:String) : boolean
}
{{< /plantuml >}}

Quantos parâmetros possui o método autenticar?

{{< alternativa >}} Nenhum {{< /alternativa >}}
{{< alternativa >}} Um {{< /alternativa >}}
{{< alternativa >}} Dois {{< /alternativa >}}
{{< alternativa >}} Três {{< /alternativa >}}

{{< solucao letra="C" >}}
O método possui os parâmetros <code>login</code> e <code>senha</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
interface Persistivel {
  salvar() : void
}

class Usuario
class Produto

Persistivel <|.. Usuario
Persistivel <|.. Produto
{{< /plantuml >}}

Qual alternativa está correta?

{{< alternativa >}} Usuario e Produto implementam Persistivel. {{< /alternativa >}}
{{< alternativa >}} Persistivel herda de Usuario e Produto. {{< /alternativa >}}
{{< alternativa >}} Usuario herda de Produto. {{< /alternativa >}}
{{< alternativa >}} Persistivel é uma classe abstrata. {{< /alternativa >}}

{{< solucao letra="A" >}}
As duas classes implementam a interface Persistivel.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
O que é uma interface em Java?

{{< alternativa >}} Uma classe que não possui métodos. {{< /alternativa >}}
{{< alternativa >}} Um contrato que define operações que outras classes devem implementar. {{< /alternativa >}}
{{< alternativa >}} Uma classe abstrata especial que pode ser instanciada. {{< /alternativa >}}
{{< alternativa >}} Um tipo de atributo utilizado em UML. {{< /alternativa >}}

{{< solucao letra="B" >}}
Uma interface define um conjunto de operações que devem ser implementadas pelas classes que a utilizam.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Qual palavra-chave é utilizada em Java para declarar uma interface?

{{< alternativa >}} abstract {{< /alternativa >}}
{{< alternativa >}} class {{< /alternativa >}}
{{< alternativa >}} interface {{< /alternativa >}}
{{< alternativa >}} implements {{< /alternativa >}}

{{< solucao letra="C" >}}
A palavra-chave utilizada para declarar uma interface é <code>interface</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Uma interface pode ser instanciada diretamente?

{{< alternativa >}} Sim, sempre. {{< /alternativa >}}
{{< alternativa >}} Apenas se não possuir métodos. {{< /alternativa >}}
{{< alternativa >}} Não. {{< /alternativa >}}
{{< alternativa >}} Apenas se for pública. {{< /alternativa >}}

{{< solucao letra="C" >}}
Interfaces não podem ser instanciadas diretamente.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Qual palavra-chave é utilizada para indicar que uma classe implementa uma interface?

{{< alternativa >}} extends {{< /alternativa >}}
{{< alternativa >}} implements {{< /alternativa >}}
{{< alternativa >}} interface {{< /alternativa >}}
{{< alternativa >}} abstract {{< /alternativa >}}

{{< solucao letra="B" >}}
A palavra-chave <code>implements</code> é utilizada para implementar interfaces.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public interface Animal{
  void emitirSom();
}
{{< /code >}}

Qual alternativa está correta?

{{< alternativa >}} Animal é uma classe concreta. {{< /alternativa >}}
{{< alternativa >}} Animal é uma interface. {{< /alternativa >}}
{{< alternativa >}} emitirSom é um atributo. {{< /alternativa >}}
{{< alternativa >}} O código possui erro de compilação. {{< /alternativa >}}

{{< solucao letra="B" >}}
A palavra-chave <code>interface</code> define uma interface.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public interface Animal{
  void emitirSom();
}

public class Cachorro implements Animal{
}
{{< /code >}}

O que acontece?

{{< alternativa >}} O código compila normalmente. {{< /alternativa >}}
{{< alternativa >}} Cachorro deve implementar emitirSom(). {{< /alternativa >}}
{{< alternativa >}} Animal torna-se uma classe abstrata. {{< /alternativa >}}
{{< alternativa >}} emitirSom é herdado automaticamente com implementação. {{< /alternativa >}}

{{< solucao letra="B" >}}
Uma classe concreta que implementa uma interface deve implementar seus métodos.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public interface Animal{
  void emitirSom();
}

public class Cachorro implements Animal{
  public void emitirSom(){
    System.out.println("Au Au");
  }
}
{{< /code >}}

Qual alternativa está correta?

{{< alternativa >}} Cachorro implementa a interface Animal. {{< /alternativa >}}
{{< alternativa >}} Cachorro herda de Animal usando extends. {{< /alternativa >}}
{{< alternativa >}} Animal é uma classe abstrata. {{< /alternativa >}}
{{< alternativa >}} O código possui erro. {{< /alternativa >}}

{{< solucao letra="A" >}}
A classe fornece implementação para o método definido na interface.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Uma classe pode implementar mais de uma interface?

{{< alternativa >}} Sim. {{< /alternativa >}}
{{< alternativa >}} Não. {{< /alternativa >}}
{{< alternativa >}} Apenas duas interfaces. {{< /alternativa >}}
{{< alternativa >}} Apenas se for abstrata. {{< /alternativa >}}

{{< solucao letra="A" >}}
Uma classe pode implementar múltiplas interfaces.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public interface A{
  void executar();
}

public interface B{
  void imprimir();
}

public class Teste implements A, B{
}
{{< /code >}}

Qual alternativa está correta?

{{< alternativa >}} O código possui erro porque uma classe só pode implementar uma interface. {{< /alternativa >}}
{{< alternativa >}} Teste deve implementar executar() e imprimir(). {{< /alternativa >}}
{{< alternativa >}} A e B devem ser classes abstratas. {{< /alternativa >}}
{{< alternativa >}} O código cria duas instâncias automaticamente. {{< /alternativa >}}

{{< solucao letra="B" >}}
A classe deve fornecer implementação para os métodos das duas interfaces.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Qual das alternativas representa corretamente a implementação de uma interface?

{{< alternativa >}}
{{< code >}}
public class Carro extends Veiculo{
}
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
public class Carro interface Veiculo{
}
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
public class Carro implements Veiculo{
}
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
public interface Carro implements Veiculo{
}
{{< /code >}}
{{< /alternativa >}}

{{< solucao letra="C" >}}
Interfaces são implementadas utilizando a palavra-chave <code>implements</code>.
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

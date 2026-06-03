---
title: "Questões sobre Classes Abstratas"
slug: classes-abstratas-questoes
description: "Lista de questões sobre classes abstratas"
tags:
- classes abstratas
- questões
---

{{< lista-questoes >}}
{{< questao >}}
O que é uma classe abstrata?

{{< alternativa >}} Uma classe que não possui atributos. {{< /alternativa >}}
{{< alternativa >}} Uma classe que não pode ser instanciada diretamente. {{< /alternativa >}}
{{< alternativa >}} Uma classe que possui apenas métodos privados. {{< /alternativa >}}
{{< alternativa >}} Uma classe que não pode possuir métodos. {{< /alternativa >}}

{{< solucao letra="B" >}}
Uma classe abstrata serve como modelo para outras classes e não pode ser instanciada diretamente.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Qual palavra-chave é utilizada em Java para declarar uma classe abstrata?

{{< alternativa >}} static {{< /alternativa >}}
{{< alternativa >}} final {{< /alternativa >}}
{{< alternativa >}} abstract {{< /alternativa >}}
{{< alternativa >}} extends {{< /alternativa >}}

{{< solucao letra="C" >}}
A palavra-chave utilizada é <code>abstract</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Uma classe abstrata pode possuir métodos implementados?

{{< alternativa >}} Sim. {{< /alternativa >}}
{{< alternativa >}} Não. {{< /alternativa >}}
{{< alternativa >}} Apenas métodos privados. {{< /alternativa >}}
{{< alternativa >}} Apenas construtores. {{< /alternativa >}}

{{< solucao letra="A" >}}
Uma classe abstrata pode possuir métodos abstratos e métodos já implementados.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
O que caracteriza um método abstrato?

{{< alternativa >}} Possui implementação obrigatória na própria classe. {{< /alternativa >}}
{{< alternativa >}} Não possui corpo (implementação). {{< /alternativa >}}
{{< alternativa >}} Deve ser privado. {{< /alternativa >}}
{{< alternativa >}} Deve retornar void. {{< /alternativa >}}

{{< solucao letra="B" >}}
Métodos abstratos definem apenas a assinatura e não possuem implementação.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public abstract class Animal{
}
{{< /code >}}

Qual alternativa está correta?

{{< alternativa >}} A classe pode ser instanciada normalmente. {{< /alternativa >}}
{{< alternativa >}} A classe é abstrata. {{< /alternativa >}}
{{< alternativa >}} O código possui erro de compilação. {{< /alternativa >}}
{{< alternativa >}} A classe é uma interface. {{< /alternativa >}}

{{< solucao letra="B" >}}
A palavra-chave <code>abstract</code> indica que a classe é abstrata.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public abstract class Animal{
}

public class Main{
  public static void main(String[] args){
    Animal a = new Animal();
  }
}
{{< /code >}}

O que acontece?

{{< alternativa >}} O código imprime o objeto. {{< /alternativa >}}
{{< alternativa >}} O código executa normalmente. {{< /alternativa >}}
{{< alternativa >}} Ocorre erro de compilação. {{< /alternativa >}}
{{< alternativa >}} O objeto recebe valor null. {{< /alternativa >}}

{{< solucao letra="C" >}}
Classes abstratas não podem ser instanciadas diretamente.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public abstract class Animal{
  public abstract void emitirSom();
}
{{< /code >}}

Quantos métodos abstratos existem na classe?

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}

{{< solucao letra="B" >}}
O método <code>emitirSom()</code> é abstrato.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public abstract class Animal{
  public abstract void emitirSom();
}

public class Cachorro extends Animal{
}
{{< /code >}}

O que acontece?

{{< alternativa >}} O código compila normalmente. {{< /alternativa >}}
{{< alternativa >}} Ocorre erro porque Cachorro não implementou emitirSom(). {{< /alternativa >}}
{{< alternativa >}} O método é herdado automaticamente. {{< /alternativa >}}
{{< alternativa >}} Cachorro torna-se uma interface. {{< /alternativa >}}

{{< solucao letra="B" >}}
Uma classe concreta deve implementar todos os métodos abstratos herdados.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public abstract class Animal{
  public abstract void emitirSom();
}

public class Cachorro extends Animal{
  public void emitirSom(){
    System.out.println("Au Au");
  }
}
{{< /code >}}

Qual alternativa está correta?

{{< alternativa >}} Cachorro implementa o método abstrato. {{< /alternativa >}}
{{< alternativa >}} Cachorro continua abstrata. {{< /alternativa >}}
{{< alternativa >}} O código possui erro. {{< /alternativa >}}
{{< alternativa >}} Animal deixa de ser abstrata. {{< /alternativa >}}

{{< solucao letra="A" >}}
A classe Cachorro fornece uma implementação para o método abstrato herdado.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Uma classe abstrata pode possuir construtores?

{{< alternativa >}} Sim. {{< /alternativa >}}
{{< alternativa >}} Não. {{< /alternativa >}}
{{< alternativa >}} Apenas se não tiver métodos abstratos. {{< /alternativa >}}
{{< alternativa >}} Apenas se for final. {{< /alternativa >}}

{{< solucao letra="A" >}}
Classes abstratas podem possuir construtores que serão utilizados pelas subclasses.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
abstract class Forma {
  +calcularArea() : double
}
{{< /plantuml >}}

Qual alternativa está correta?

{{< alternativa >}} Forma é uma interface. {{< /alternativa >}}
{{< alternativa >}} Forma é uma classe abstrata. {{< /alternativa >}}
{{< alternativa >}} calcularArea é um atributo. {{< /alternativa >}}
{{< alternativa >}} calcularArea retorna int. {{< /alternativa >}}

{{< solucao letra="B" >}}
A palavra <code>abstract</code> indica uma classe abstrata.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
abstract class Funcionario {
  +calcularSalario() : double
}
{{< /plantuml >}}

Qual é o tipo de retorno do método calcularSalario?

{{< alternativa >}} void {{< /alternativa >}}
{{< alternativa >}} int {{< /alternativa >}}
{{< alternativa >}} double {{< /alternativa >}}
{{< alternativa >}} String {{< /alternativa >}}

{{< solucao letra="C" >}}
O diagrama indica retorno do tipo <code>double</code>.
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

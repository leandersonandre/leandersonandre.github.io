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

{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
abstract class Animal {
  {abstract} emitirSom() : void
}
{{< /plantuml >}}

Qual alternativa está correta?

{{< alternativa >}} Animal possui um método concreto chamado emitirSom. {{< /alternativa >}}
{{< alternativa >}} emitirSom é um método abstrato. {{< /alternativa >}}
{{< alternativa >}} emitirSom é um atributo. {{< /alternativa >}}
{{< alternativa >}} Animal é uma interface. {{< /alternativa >}}

{{< solucao letra="B" >}}
A notação <code>{abstract}</code> indica que o método é abstrato.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
abstract class Forma {
  {abstract} calcularArea() : double
}
{{< /plantuml >}}

Qual é o tipo de retorno do método calcularArea?

{{< alternativa >}} int {{< /alternativa >}}
{{< alternativa >}} void {{< /alternativa >}}
{{< alternativa >}} String {{< /alternativa >}}
{{< alternativa >}} double {{< /alternativa >}}

{{< solucao letra="D" >}}
O tipo de retorno aparece após os dois pontos.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
abstract class Funcionario {
  nome : String
  {abstract} calcularSalario() : double
}
{{< /plantuml >}}

Quantos métodos abstratos existem na classe?

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}

{{< solucao letra="B" >}}
Apenas o método <code>calcularSalario()</code> está marcado como abstrato.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
abstract class Veiculo {
  {abstract} acelerar() : void
}
{{< /plantuml >}}

Qual código Java corresponde ao método representado?

{{< alternativa >}}
{{< code >}}
public void acelerar(){}
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
public abstract void acelerar();
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
private abstract void acelerar();
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
public int acelerar();
{{< /code >}}
{{< /alternativa >}}

{{< solucao letra="B" >}}
O método é abstrato, público e não possui implementação.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
abstract class Documento {
  {abstract} validar() : boolean
}
{{< /plantuml >}}

Qual alternativa está correta?

{{< alternativa >}} validar retorna String. {{< /alternativa >}}
{{< alternativa >}} validar recebe um parâmetro boolean. {{< /alternativa >}}
{{< alternativa >}} validar é um método abstrato que retorna boolean. {{< /alternativa >}}
{{< alternativa >}} validar é um atributo do tipo boolean. {{< /alternativa >}}

{{< solucao letra="C" >}}
O método está marcado como abstrato e possui retorno boolean.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
abstract class Figura {
  {abstract} desenhar() : void
}

class Circulo {
  +desenhar() : void
}
Figura <|-- Circulo
{{< /plantuml >}}

Qual alternativa está correta?

{{< alternativa >}} Circulo herda de Figura. {{< /alternativa >}}
{{< alternativa >}} Figura herda de Circulo. {{< /alternativa >}}
{{< alternativa >}} desenhar é um atributo. {{< /alternativa >}}
{{< alternativa >}} Circulo é abstrata. {{< /alternativa >}}

{{< solucao letra="A" >}}
A seta de generalização indica que Circulo herda de Figura.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
abstract class Pagamento {
  {abstract} processar(valor : double) : void
}
{{< /plantuml >}}

Quantos parâmetros possui o método processar?

{{< alternativa >}} Nenhum {{< /alternativa >}}
{{< alternativa >}} Um parâmetro do tipo double {{< /alternativa >}}
{{< alternativa >}} Dois parâmetros do tipo double {{< /alternativa >}}
{{< alternativa >}} Um parâmetro do tipo void {{< /alternativa >}}

{{< solucao letra="B" >}}
O método recebe um parâmetro chamado <code>valor</code> do tipo <code>double</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
abstract class Conta {
  {abstract} sacar(valor : double) : boolean
}
{{< /plantuml >}}

Qual alternativa representa corretamente a assinatura do método em Java?

{{< alternativa >}}
{{< code >}}
public abstract boolean sacar(double valor);
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
public boolean sacar(double valor){}
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
public abstract void sacar(double valor);
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
private abstract boolean sacar(double valor);
{{< /code >}}
{{< /alternativa >}}

{{< solucao letra="A" >}}
O método recebe um parâmetro double e retorna boolean.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo e identifique a alternativa incorreta.

{{< plantuml >}}
abstract class Relatorio {
  {abstract} gerar() : String
}
{{< /plantuml >}}

{{< alternativa >}} Relatorio é uma classe abstrata. {{< /alternativa >}}
{{< alternativa >}} gerar retorna String. {{< /alternativa >}}
{{< alternativa >}} gerar é um método abstrato. {{< /alternativa >}}
{{< alternativa >}} gerar possui implementação na classe Relatorio. {{< /alternativa >}}

{{< solucao letra="D" >}}
Métodos abstratos não possuem implementação.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo e identifique a alternativa correta.

{{< plantuml >}}
abstract class Operacao {
  {abstract} executar(a:int, b:int) : int
}
{{< /plantuml >}}

{{< alternativa >}} executar recebe dois parâmetros e retorna int. {{< /alternativa >}}
{{< alternativa >}} executar recebe um parâmetro int. {{< /alternativa >}}
{{< alternativa >}} executar retorna String. {{< /alternativa >}}
{{< alternativa >}} executar é um atributo. {{< /alternativa >}}

{{< solucao letra="A" >}}
O método possui dois parâmetros do tipo int e retorno int.
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

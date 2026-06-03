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
interface  Animal <<interface>> {
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
interface  Forma <<interface>> {
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
interface Imprimivel <<interface>> {
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
interface Autenticavel <<interface>> {
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
interface  Persistivel <<interface>> {
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
public interface Animal <<interface>>{
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
public interface Animal <<interface>>{
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
public interface  A <<interface>>{
  void executar();
}

public interface B <<interface>>{
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

public class Main{
  public static void main(String[] args){
    Animal a = new Cachorro();
  }
}
{{< /code >}}

Qual conceito está sendo demonstrado?

{{< alternativa >}} Encapsulamento. {{< /alternativa >}}
{{< alternativa >}} Polimorfismo. {{< /alternativa >}}
{{< alternativa >}} Sobrecarga. {{< /alternativa >}}
{{< alternativa >}} Composição. {{< /alternativa >}}

{{< solucao letra="B" >}}
Uma variável do tipo da interface referencia um objeto de uma classe que a implementa.
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

public class Main{
  public static void main(String[] args){
    Animal a = new Cachorro();
    a.emitirSom();
  }
}
{{< /code >}}

Qual valor será impresso?

{{< alternativa >}} Animal {{< /alternativa >}}
{{< alternativa >}} Cachorro {{< /alternativa >}}
{{< alternativa >}} Au Au {{< /alternativa >}}
{{< alternativa >}} Nada {{< /alternativa >}}

{{< solucao letra="C" >}}
A chamada é resolvida em tempo de execução para a implementação da classe Cachorro.
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

public class Gato implements Animal{
  public void emitirSom(){
    System.out.println("Miau");
  }
}

public class Main{
  public static void main(String[] args){
    Animal a = new Gato();
    a.emitirSom();
  }
}
{{< /code >}}

Qual será a saída?

{{< alternativa >}} Au Au {{< /alternativa >}}
{{< alternativa >}} Miau {{< /alternativa >}}
{{< alternativa >}} Animal {{< /alternativa >}}
{{< alternativa >}} Erro de compilação {{< /alternativa >}}

{{< solucao letra="B" >}}
Embora a variável seja do tipo Animal, o objeto referenciado é um Gato.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public interface Forma{
  double area();
}

public class Quadrado implements Forma{
  public double area(){
    return 25;
  }
}

public class Main{
  public static void main(String[] args){
    Forma f = new Quadrado();
    System.out.println(f.area());
  }
}
{{< /code >}}

Qual valor será impresso?

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 25 {{< /alternativa >}}
{{< alternativa >}} Erro de compilação {{< /alternativa >}}

{{< solucao letra="C" >}}
A chamada é direcionada para o método implementado em Quadrado.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public interface Veiculo{
  void mover();
}

public class Carro implements Veiculo{
  public void mover(){
    System.out.println("Rodando");
  }
}

public class Barco implements Veiculo{
  public void mover(){
    System.out.println("Navegando");
  }
}
{{< /code >}}

Qual alternativa representa uma utilização polimórfica da interface?

{{< alternativa >}}
{{< code >}}
Veiculo v = new Carro();
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
Carro v = new Veiculo();
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
Veiculo v = new Veiculo();
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
Carro v = new Barco();
{{< /code >}}
{{< /alternativa >}}

{{< solucao letra="A" >}}
Uma referência do tipo da interface pode apontar para qualquer objeto que a implemente.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public interface Impressora{
  void imprimir();
}

public class Pdf implements Impressora{
  public void imprimir(){
    System.out.println("PDF");
  }
}

public class Texto implements Impressora{
  public void imprimir(){
    System.out.println("TXT");
  }
}
{{< /code >}}

Qual é a principal vantagem de utilizar a interface Impressora?

{{< alternativa >}} Impedir a criação de objetos. {{< /alternativa >}}
{{< alternativa >}} Permitir tratar diferentes implementações de forma uniforme. {{< /alternativa >}}
{{< alternativa >}} Tornar todos os métodos privados. {{< /alternativa >}}
{{< alternativa >}} Eliminar a necessidade de classes. {{< /alternativa >}}

{{< solucao letra="B" >}}
O código cliente pode trabalhar com a interface sem conhecer a implementação concreta.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o UML abaixo.

{{< plantuml >}}
interface Animal {
  emitirSom() : void
}

class Cachorro
class Gato

Animal <|.. Cachorro
Animal <|.. Gato
{{< /plantuml >}}

Qual alternativa demonstra polimorfismo?

{{< alternativa >}}
{{< code >}}
Animal a = new Cachorro();
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
Cachorro a = new Animal();
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
Animal a = new Animal();
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
Gato a = new Cachorro();
{{< /code >}}
{{< /alternativa >}}

{{< solucao letra="A" >}}
Uma referência do tipo da interface aponta para um objeto concreto.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public interface Pagamento{
  void pagar();
}

public class Pix implements Pagamento{
  public void pagar(){
    System.out.println("PIX");
  }
}

public class Cartao implements Pagamento{
  public void pagar(){
    System.out.println("CARTAO");
  }
}

public class Main{
  public static void main(String[] args){
    Pagamento p = new Cartao();
    p.pagar();
  }
}
{{< /code >}}

Qual será a saída?

{{< alternativa >}} PIX {{< /alternativa >}}
{{< alternativa >}} CARTAO {{< /alternativa >}}
{{< alternativa >}} Pagamento {{< /alternativa >}}
{{< alternativa >}} Erro de compilação {{< /alternativa >}}

{{< solucao letra="B" >}}
O método executado depende do objeto referenciado, não do tipo da variável.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public interface Forma{
  double area();
}

public class Quadrado implements Forma{
  public double area(){
    return 16;
  }
}

public class Circulo implements Forma{
  public double area(){
    return 12;
  }
}

public class Main{
  public static void imprimir(Forma f){
    System.out.println(f.area());
  }
}
{{< /code >}}

Qual vantagem a utilização da interface Forma proporciona ao método imprimir?

{{< alternativa >}} O método aceita apenas objetos Quadrado. {{< /alternativa >}}
{{< alternativa >}} O método aceita apenas objetos Circulo. {{< /alternativa >}}
{{< alternativa >}} O método pode receber qualquer objeto que implemente Forma. {{< /alternativa >}}
{{< alternativa >}} O método não pode ser reutilizado. {{< /alternativa >}}

{{< solucao letra="C" >}}
O parâmetro é do tipo da interface, permitindo o uso de polimorfismo.
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

public class Gato implements Animal{
  public void emitirSom(){
    System.out.println("Miau");
  }
}

public class Main{
  public static void main(String[] args){
    Animal[] animais = {
      new Cachorro(),
      new Gato()
    };

    for(Animal a : animais){
      a.emitirSom();
    }
  }
}
{{< /code >}}

Qual será a saída?

{{< alternativa >}}
Au Au
Au Au
{{< /alternativa >}}

{{< alternativa >}}
Miau
Miau
{{< /alternativa >}}

{{< alternativa >}}
Au Au
Miau
{{< /alternativa >}}

{{< alternativa >}}
Erro de compilação
{{< /alternativa >}}

{{< solucao letra="C" >}}
Cada elemento do vetor executa sua própria implementação de <code>emitirSom()</code>, caracterizando polimorfismo.
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

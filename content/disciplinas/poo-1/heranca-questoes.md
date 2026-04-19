---
title: "Questões sobre Herança"
slug: heranca-questoes
description: "Lista de questões sobre Herança"
tags:
- herança
- questões
---

{{< lista-questoes >}}


{{< questao >}} 
Identifique a alternativa que melhor descreve o conceito de herança.
{{< alternativa >}} Modificador que permite apenas a própria classe acessar os atributos ou métodos. {{< /alternativa >}}
{{< alternativa >}} Técnica de ocultamento dos detalhes dos objetos. {{< /alternativa >}}
{{< alternativa >}} Uma associação do tipo todo parte onde as partes podem existir independente do todo. {{< /alternativa >}}
{{< alternativa >}} Mecanismo que permite o reaproveitamento de código e organização hierárquica de classes. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="D">}} Herança permite reutilização de código e organização hierárquica entre classes. {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
No Java não é permitido realizar múltipla herança de classes. Ou seja, uma classe não pode estender mais de uma classe ao mesmo tempo.

Diante dessa limitação, qual é o tipo de relacionamento mais utilizado para representar a ideia de “reutilização de comportamentos de múltiplas fontes” em Java?

{{< alternativa >}} Herança múltipla {{< /alternativa >}}
{{< alternativa >}} Associação {{< /alternativa >}}
{{< alternativa >}} Composição (ou agregação) {{< /alternativa >}}
{{< alternativa >}} Dependência circular {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="C">}} Como o Java não permite herança múltipla de classes, utiliza-se principalmente composição (ou agregação) para reutilizar comportamentos e estruturar relações entre objetos, permitindo combinar funcionalidades de diferentes classes sem herança múltipla. {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Identifique o símbolo da UML que representa a visibilidade protegida.
{{< alternativa >}} + {{< /alternativa >}}
{{< alternativa >}} - {{< /alternativa >}}
{{< alternativa >}} # {{< /alternativa >}}
{{< alternativa >}} ~ {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="C">}} Visibilidade protegida em UML é representada por #. {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Identifique o símbolo da UML que representa a visibilidade de pacote (package).

{{< alternativa >}} + {{< /alternativa >}} 
{{< alternativa >}} - {{< /alternativa >}}
{{< alternativa >}} # {{< /alternativa >}}
{{< alternativa >}} ~ {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="D">}} A visibilidade de pacote (package) em UML é representada pelo símbolo ~. {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise o diagrama e identifique a alternativa correta.

{{< plantuml >}} 
ClassB -L-|> ClassA
{{< /plantuml >}} 

{{< alternativa >}} ClasseA representa o objeto "todo" no relacionamento de agregação. {{< /alternativa >}}
{{< alternativa >}} ClasseA representa o objeto "todo" no relacionamento de composição. {{< /alternativa >}}
{{< alternativa >}} ClasseB depende da ClasseA {{< /alternativa >}}
{{< alternativa >}} ClasseB extende a ClasseA {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="D">}}
A linha com triângulo aberto (`--|>`) no diagrama UML representa uma relação de <b>herança (generalização)</b>. Ela indica que uma classe (ClasseB) estende outra classe (ClasseA), formando uma hierarquia entre superclasse e subclasse.
{{< /solucao >}}

{{< /questao >}}

{{< questao >}} 
Analise o diagrama e identifique as classes que estão em um relacionamento de Herança.

{{< plantuml >}}
class ClasseV
class ClasseL
class ClasseF
class ClasseB
class ClasseG
class ClasseA
class ClasseH
class ClasseK

ClasseV o-- ClasseL
ClasseF <|-- ClasseB
ClasseG --> ClasseA
ClasseH *-- ClasseK
{{< /plantuml >}}

{{< alternativa >}} ClasseV e ClasseL {{< /alternativa >}}
{{< alternativa >}} ClasseF e ClasseB {{< /alternativa >}}
{{< alternativa >}} ClasseG e ClasseA {{< /alternativa >}}
{{< alternativa >}} ClasseH e ClasseK {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="B">}} O relacionamento de herança em UML é representado pela seta com triângulo aberto (<|--). No diagrama, isso ocorre entre ClasseF e ClasseB, indicando que ClasseB herda de ClasseF. {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise o código e identifique a mensagem que irá imprimir no terminal.
{{< code >}}
public class A {
  public void metodo(){
    System.out.println("1");
  }
}
public class Main{
  public void metodo(){
    System.out.println("2");
  }
  public static void main(String args[]){
    Main main = new Main();
    main.metodo();
  }
}
{{< /code >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. {{< /alternativa >}}
{{< alternativa >}} Erro de execução. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="B">}} O método chamado é o de Main, imprimindo "2". {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise o código e identifique a mensagem que irá imprimir no terminal.
{{< code >}}
public class A {
  public void metodo(){
    System.out.println("1");
  }
}
public class Main extends A{
  public void metodo(){
    System.out.println("2");
  }
  public static void main(String args[]){
    Main main = new Main();
    main.metodo();
  }
}
{{< /code >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. {{< /alternativa >}}
{{< alternativa >}} Erro de execução. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="B">}} O método sobrescrito em Main imprime "2". {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise o código e identifique a mensagem que irá imprimir no terminal.
{{< code >}}
public class A {
  public void metodo(){
    System.out.println("1");
  }
}
public class Main extends A{
  public void metodo2(){
    System.out.println("2");
  }
  public static void main(String args[]){
    Main main = new Main();
    main.metodo();
  }
}
{{< /code >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. {{< /alternativa >}}
{{< alternativa >}} Erro de execução. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="A">}} O método herdado de A imprime "1". {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise o código e identifique a mensagem que irá imprimir no terminal.
{{< code >}}
public class A extends Main{
  public void metodo(){
    System.out.println("1");
  }
}
public class Main{
  public void metodo(){
    System.out.println("2");
  }
  public static void main(String args[]){
    Main main = new A();
    main.metodo();
  }
}
{{< /code >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. {{< /alternativa >}}
{{< alternativa >}} Erro de execução. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="A">}} Polimorfismo chama método de A, imprimindo "1". {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise o código e identifique a mensagem irá imprimir no terminal.
{{< code >}}
public class A extends Main{
  private int i = 9;
}
public class Main{
  public void metodo(){
    System.out.println("2");
  }
  public static void main(String args[]){
    Main main = new A();
    System.out.println(main.i);
  }
}
{{< /code >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. {{< /alternativa >}}
{{< alternativa >}} Erro de execução. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="C">}} O código apresenta erro de compilação porque a variável de referência é do tipo Main, e essa classe não possui o atributo i. Além disso, mesmo que o atributo estivesse acessível na hierarquia, ele está declarado como private na classe A, o que impede acesso direto fora da própria classe. {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise o código e identifique a mensagem que irá imprimir no terminal.
{{< code >}}
public class A extends Main{
  protected int i = 9;
}
public class Main{
  public void metodo(){
    System.out.println("2");
  }
  public static void main(String args[]){
    Main main = new A();
    System.out.println(main.i);
  }
}
{{< /code >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. {{< /alternativa >}}
{{< alternativa >}} Erro de execução. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="E">}} Acesso inválido ao atributo via referência na classe Main. {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise o código e identifique a mensagem que irá imprimir no terminal.
{{< code >}}
public class A extends Main{
  public int i = 9;
}
public class Main{
  public void metodo(){
    System.out.println("2");
  }
  public static void main(String args[]){
    Main main = new Main();
    System.out.println(main.i);
  }
}
{{< /code >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. {{< /alternativa >}}
{{< alternativa >}} Erro de execução. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="E">}} A classe Main não possui atributo i. {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise o código e identifique o problema que existe no código.
{{< code >}}
public class A {
  public A(int a){}
}
public class Main extends A{
  public Main(){ }
  public static void main(String args[]){
    Main main = new Main();
  }
}
{{< /code >}}
{{< alternativa >}} Erro de execução. Erro de conversão de tipos. {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. Interface não implementada. {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. Construtor da super classe deve ser invocado. {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. Classe final não pode ser herdada. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="C">}} Superclasse não possui construtor padrão. {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise o código e identifique o problema que existe no código.
{{< code >}}
public final class A {
  public A(){}
}
public class Main extends A{
  public Main(){ }
  public static void main(String args[]){
    Main main = new Main();
  }
}
{{< /code >}}
{{< alternativa >}} Erro de execução. {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. Interface não implementada. {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. Construtor da super classe deve ser invocado. {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. Classe final não pode ser herdada. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="D">}} Classe final não pode ser estendida. {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise o código e identifique o problema que existe no código.
{{< code >}}
public class A {
  public A(int a){}
}
public class Main extends A{
  public Main(){ super(0); }
  public static void main(String args[]){
    Main main = new Main();
  }
}
{{< /code >}}
{{< alternativa >}} Erro de execução. {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. Interface não implementada. {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. Construtor da super classe deve ser invocado. {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. Classe final não pode ser herdada. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="E">}} Código está correto. {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise o código e identifique o problema que existe no código.
{{< code >}}
public class A {
  public A(int a){}
}
public class Main extends A{
  public Main(){ }
  public static void main(String args[]){
    Main main = new A(1);
  }
}
{{< /code >}}
{{< alternativa >}} Erro de execução. {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. Interface não implementada. {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. Construtor da super classe deve ser invocado. {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. Classe final não pode ser herdada. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="C">}} O código apresenta erro de compilação, pois a classe Main não invoca corretamente o construtor da superclasse A (que exige parâmetro), e também há incompatibilidade de tipos ao tentar atribuir um objeto do tipo A a uma variável do tipo Main. {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise e identifique o problema que existe no código.
{{< code >}}
public class A {
  public A(int a){}
}
public class Main{
  public Main(){ }
  public static void main(String args[]){
    Main main = new A(1);
  }
}
{{< /code >}}
{{< alternativa >}} Erro de execução. {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. Interface não implementada. {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. Construtor da super classe deve ser invocado. {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. Classe final não pode ser herdada. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="E">}} Atribuição incompatível de tipos. {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise o código e identifique o resultado da execução.

{{< code >}}
public class A {
  public final void metodo(){
    System.out.println("A");
  }
}

public class B extends A {
  public void metodo(){
    System.out.println("B");
  }

  public static void main(String args[]){
    B b = new B();
    b.metodo();
  }
}
{{< /code >}}

{{< alternativa >}} A {{< /alternativa >}}
{{< alternativa >}} B {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. O método não pode ser sobrescrito. {{< /alternativa >}}
{{< alternativa >}} Erro de execução. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="C">}} O método `metodo()` na classe A é declarado como `final`, portanto não pode ser sobrescrito na classe B. Isso gera erro de compilação. {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise o código e identifique o problema existente.

{{< code >}}
public final class A {
  public void metodo(){
    System.out.println("A");
  }
}

public class B extends A {
  public void metodo(){
    System.out.println("B");
  }

  public static void main(String args[]){
    B b = new B();
    b.metodo();
  }
}
{{< /code >}}

{{< alternativa >}} A {{< /alternativa >}}
{{< alternativa >}} B {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. Classe final não pode ser herdada. {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. Método final não pode ser sobrescrito. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="C">}} A classe A é declarada como final, portanto não pode ser estendida pela classe B, resultando em erro de compilação. {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise o código e identifique o que será impresso no terminal.

{{< code >}}
public class A {
  public void metodo1(){
    System.out.println("A1");
  }

  public void metodo2(){
    System.out.println("A2");
  }
}

public class B extends A {
  @Override
  public void metodo1(){
    System.out.println("B1");
  }
}

public class C extends B {
  @Override
  public void metodo2(){
    System.out.println("C2");
  }

  public static void main(String args[]){
    C obj = new C();
    obj.metodo1();
    obj.metodo2();
  }
}
{{< /code >}}

{{< alternativa >}} A1 e A2 {{< /alternativa >}}
{{< alternativa >}} B1 e A2 {{< /alternativa >}}
{{< alternativa >}} B1 e C2 {{< /alternativa >}}
{{< alternativa >}} A1 e C2 {{< /alternativa >}}
{{< alternativa >}} Erro de compilação {{< /alternativa >}}

{{< solucao letra="C">}} O método `metodo1()` é sobrescrito na classe B, então imprime "B1". O método `metodo2()` é sobrescrito na classe C, então imprime "C2". Portanto, a saída é "B1" e "C2". {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise o código e identifique o que será impresso no terminal.

{{< code >}}
public class A {
  public void metodo1(){
    System.out.println("A1");
  }

  public void metodo2(){
    System.out.println("A2");
  }
}

public class B extends A {
  @Override
  public void metodo1(){
    System.out.println("B1");
  }
}

public class C extends B {
  @Override
  public void metodo2(){
    System.out.println("C2");
  }
}

public class Main {
  public static void main(String args[]){
    A obj = new B();
    obj.metodo1();
    obj.metodo2();
  }
}
{{< /code >}}

{{< alternativa >}} A1 e A2 {{< /alternativa >}}
{{< alternativa >}} B1 e A2 {{< /alternativa >}}
{{< alternativa >}} B1 e C2 {{< /alternativa >}}
{{< alternativa >}} A1 e C2 {{< /alternativa >}}
{{< alternativa >}} Erro de compilação {{< /alternativa >}}

{{< solucao letra="B">}} O objeto real é do tipo B. O método `metodo1()` é sobrescrito em B, então imprime "B1". O método `metodo2()` não foi sobrescrito em B (nem em C no objeto real), então executa a versão de A, imprimindo "A2". Isso demonstra polimorfismo com referência do tipo A e objeto do tipo B. {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise o código e identifique o resultado da execução.

{{< code >}}
public class A { }

public class B extends A { }

public class C extends B { }

public class D extends B { }

public class Main {
  public static void main(String args[]){
    A obj = new C();

    D d = (D) obj;

    System.out.println("OK");
  }
}
{{< /code >}}

{{< alternativa >}} OK {{< /alternativa >}}
{{< alternativa >}} Erro de compilação {{< /alternativa >}}
{{< alternativa >}} Erro de execução (ClassCastException) {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< alternativa >}} O código não compila pois não há métodos {{< /alternativa >}}

{{< solucao letra="C">}} O código compila, pois o cast entre tipos relacionados é permitido em tempo de compilação. Porém, em tempo de execução ocorre `ClassCastException`, pois o objeto real é do tipo C e não pode ser convertido para D (classes irmãs na hierarquia). {{< /solucao >}}
{{< /questao >}}

{{< questao >}} 
Analise o código e identifique o resultado da execução.

{{< code >}}
public class A { }

public class B extends A { }

public class C extends B { }

public class D extends B { }

public class Main {
  public static void main(String args[]){
    A obj = new C();

    B b = (B) obj;

    System.out.println("OK");
  }
}
{{< /code >}}

{{< alternativa >}} OK {{< /alternativa >}}
{{< alternativa >}} Erro de compilação {{< /alternativa >}}
{{< alternativa >}} Erro de execução (ClassCastException) {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< alternativa >}} Conversão inválida entre classes {{< /alternativa >}}

{{< solucao letra="A">}} O código compila e executa corretamente. O objeto real é do tipo C, que é subclasse de B, então o cast `(B) obj` é válido. Após o casting, o programa imprime "OK". {{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

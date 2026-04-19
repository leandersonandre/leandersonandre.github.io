---
title: "Questões sobre Classes e Objetos"
slug: classes-objetos-questoes
description: "Lista de questões sobre classes e objetos"
tags:
- herança
- questões
---

{{< lista-questoes >}}

{{< questao >}}
O que é uma classe na programação orientada a objetos?
{{< alternativa >}} Um objeto já criado em memória. {{< /alternativa >}}
{{< alternativa >}} Um tipo de variável primitiva. {{< /alternativa >}}
{{< alternativa >}} Um molde (modelo) que define atributos e métodos para criar objetos. {{< /alternativa >}}
{{< alternativa >}} Um método que retorna valores. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="C" >}}
Uma classe é um modelo que define a estrutura (atributos) e comportamento (métodos) dos objetos.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que é um objeto na programação orientada a objetos?
{{< alternativa >}} Um molde usado para criar classes. {{< /alternativa >}}
{{< alternativa >}} Uma instância de uma classe, que possui atributos e métodos. {{< /alternativa >}}
{{< alternativa >}} Um tipo primitivo de dado. {{< /alternativa >}}
{{< alternativa >}} Um método que executa ações no programa. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="B" >}}
Um objeto é uma instância de uma classe, contendo atributos (dados) e métodos (comportamentos).
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Quais são os componentes de um objeto?

{{< alternativa >}} Objetos não possuem componentes. {{< /alternativa >}}
{{< alternativa >}} Somente atributos. {{< /alternativa >}}
{{< alternativa >}} Somente métodos. {{< /alternativa >}}
{{< alternativa >}} Atributos e métodos. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="D" >}} Atributos e métodos. {{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Quais são os pilares da programação orientada à objetos?

{{< alternativa >}} Funções, encapsulamento, herança e polimorfismo. {{< /alternativa >}}
{{< alternativa >}} Abstração, recursão, herança e polimorfismo. {{< /alternativa >}}
{{< alternativa >}} Compilação, encapsulamento, herança e polimorfismo. {{< /alternativa >}}
{{< alternativa >}} Abstração, encapsulamento, funções e polimorfismo. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="E" >}} Abstração, encapsulamento, herança e polimorfismo. {{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Quais é a definição de abstração no contexto de programação orientada à objetos?

{{< alternativa >}} Processo de ocultar os detalhes do objeto. {{< /alternativa >}}
{{< alternativa >}} Processo de isolar apenas as informações necessárias dos objetos. {{< /alternativa >}}
{{< alternativa >}} Processo de criar objetos com métodos pequenos. {{< /alternativa >}}
{{< alternativa >}} Processo de criar classes para representar os objetos. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="B" >}} Processo de isolar apenas as informações necessárias dos objetos. {{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Quais é a definição do conceito de atributo?

{{< alternativa >}} Característica/informação de um objeto. {{< /alternativa >}}
{{< alternativa >}} Função/sub-rotina de um objeto. {{< /alternativa >}}
{{< alternativa >}} Estrutura que define um objeto. {{< /alternativa >}}
{{< alternativa >}} Estrutura que permite reutilizar um objeto. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="A" >}} Característica/informação de um objeto. {{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Quais é a definição do conceito de método?

{{< alternativa >}} Característica/informação de um objeto. {{< /alternativa >}}
{{< alternativa >}} Função/sub-rotina de um objeto. {{< /alternativa >}}
{{< alternativa >}} Estrutura que define um objeto. {{< /alternativa >}}
{{< alternativa >}} Estrutura que permite reutilizar um objeto. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="B" >}} Função/sub-rotina de um objeto. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a diferença entre classe e objeto?
{{< alternativa >}} Não há diferença, são a mesma coisa. {{< /alternativa >}}
{{< alternativa >}} Classe é um método e objeto é uma variável. {{< /alternativa >}}
{{< alternativa >}} Classe é o molde e objeto é a instância criada a partir desse molde. {{< /alternativa >}}
{{< alternativa >}} Objeto define a classe. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="C" >}}
Classe é o modelo (molde), enquanto objeto é a instância concreta criada a partir dela.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o tipo de dados de seu atributo. 

{{< code >}}
public class Livro{
 String nome;
 public String nome(){
   return nome;
 }
}
{{< /code >}}

{{< alternativa >}} Livro {{< /alternativa >}}
{{< alternativa >}} void {{< /alternativa >}}
{{< alternativa >}} nome {{< /alternativa >}}
{{< alternativa >}} String. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="D" >}} String. {{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o estado atual do objeto x. 

{{< code >}}
// Arquivo Livro.java
public class Livro{
 String nome;
 public String nome(){
   return nome;
 }
}
// Arquivo Main.java
public Main{
  public static void main(String args[]){
    Livro x = new Livro();
 }
}
{{< /code >}}

{{< alternativa >}} Livro{nome=""} {{< /alternativa >}}
{{< alternativa >}} Livro{nome=0} {{< /alternativa >}}
{{< alternativa >}} Livro{nome=x} {{< /alternativa >}}
{{< alternativa >}} Livro{nome=null} {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="D" >}} Livro{nome=null} {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique o valor impresso.
{{< code >}}
public class Teste{
int valor = 5;
public int valor(){
return valor + 5;
}
}
public class Main{
public static void main(String[] args){
Teste t = new Teste();
System.out.println(t.valor());
}
}
{{< /code >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} null {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="B" >}}
O método retorna 5 + 5 = 10.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique o valor impresso.
{{< code >}}
public class Teste{
int valor = 5;
public int valor(){
return valor + 5;
}
}
public class Main{
public static void main(String[] args){
Teste t = new Teste();
System.out.println(t.valor);
}
}
{{< /code >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} null {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="A" >}}
Aqui é acessado o atributo diretamente, não o método.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique o estado atual do objeto x. 

{{< code >}}
// Arquivo Livro.java
public class Livro{
 String nome;
 public String nome(){
   return nome;
 }
}
// Arquivo Main.java
public Main{
  public static void main(String args[]){
    Livro x = new Livro();
    x.nome = "dicionario";
 }
}
{{< /code >}}

{{< alternativa >}} Livro{nome=""} {{< /alternativa >}}
{{< alternativa >}} Livro{nome="null"} {{< /alternativa >}}
{{< alternativa >}} Livro{nome="dicionario"} {{< /alternativa >}}
{{< alternativa >}} Livro{nome=null} {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="C" >}} Livro{nome="dicionario"} {{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o estado atual do objeto ponto. 

{{< code >}}
// Arquivo Ponto.java
public class Ponto{
 int x;
 int y;
}
// Arquivo Main.java
public Main{
  public static void main(String args[]){
    Ponto ponto = new Ponto();
 }
}
{{< /code >}}

{{< alternativa >}} Ponto{x=null, y=null} {{< /alternativa >}}
{{< alternativa >}} Ponto{x= , y= } {{< /alternativa >}}
{{< alternativa >}} Ponto{x=0, y=0} {{< /alternativa >}}
{{< alternativa >}} Ponto{x=-1  , y=-1   } {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="C" >}} Ponto{x=0, y=0} {{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o estado atual do objeto ponto. 

{{< code >}}
// Arquivo Ponto.java
public class Ponto{
 int x;
 int y;
}
// Arquivo Main.java
public Main{
  public static void main(String args[]){
    Ponto ponto = new Ponto();
    ponto.x = -1;
    ponto.y = 0;
 }
}
{{< /code >}}

{{< alternativa >}} Ponto{x=null, y=null} {{< /alternativa >}}
{{< alternativa >}} Ponto{x= , y= } {{< /alternativa >}}
{{< alternativa >}} Ponto{x=0, y=0} {{< /alternativa >}}
{{< alternativa >}} Ponto{x=-1  , y=-1   } {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="E" >}} Nenhuma das anteriores {{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o estado atual do objeto ponto. 

{{< code >}}
// Arquivo Ponto.java
public class Ponto{
 int x;
 int y;
}
// Arquivo Main.java
public Main{
  public static void main(String args[]){
    Ponto ponto = new Ponto();
    ponto.x = -1;
    ponto.y = 0;
    ponto.y = -1;
 }
}
{{< /code >}}

{{< alternativa >}} Ponto{x=null, y=null} {{< /alternativa >}}
{{< alternativa >}} Ponto{x= , y= } {{< /alternativa >}}
{{< alternativa >}} Ponto{x=0, y=0} {{< /alternativa >}}
{{< alternativa >}} Ponto{x=-1  , y=-1   } {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="D" >}} Ponto{x=-1  , y=-1   } {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique o estado atual do objeto ponto. 

{{< code >}}
// Arquivo Ponto.java
public class Ponto{
 int x = 9;
 int y = 8;
}
// Arquivo Main.java
public Main{
  public static void main(String args[]){
    Ponto ponto = new Ponto();
 }
}
{{< /code >}}

{{< alternativa >}} Ponto{x=null, y=null} {{< /alternativa >}}
{{< alternativa >}} Ponto{x= , y= } {{< /alternativa >}}
{{< alternativa >}} Ponto{x=0, y=0} {{< /alternativa >}}
{{< alternativa >}} Ponto{x=-1  , y=-1   } {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="E" >}}
Os atributos <code>x</code> e <code>y</code> foram inicializados diretamente na classe com os valores 9 e 8. Portanto, o estado do objeto é <code>Ponto{x=9, y=8}</code>, alternativa que não está listada.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o valor que será impresso no terminal. 

{{< code >}}
// Arquivo Retangulo.java
public class Retangulo{
 int largura = 5;
 int altura = 10;
 public int area(){
   return largura * altura;
 }
}
// Arquivo Main.java
public Main{
  public static void main(String args[]){
    Retangulo r = new Retangulo();
    System.out.println(r.area());
 }
}
{{< /code >}}

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 50 {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="D" >}}
O método <code>area()</code> retorna o produto de <code>largura * altura</code>, ou seja, 5 * 10 = 50.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o valor que será impresso no terminal. 

{{< code >}}
// Arquivo Retangulo.java
public class Retangulo{
 int largura = 10;
 int altura = 10;
 public int area(){
   return largura * altura;
 }
}
// Arquivo Main.java
public Main{
  public static void main(String args[]){
    Retangulo r = new Retangulo();
    System.out.println(r.area());
 }
}
{{< /code >}}

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 50 {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="E" >}}
O cálculo realizado é 10 * 10 = 100. Como esse valor não aparece nas alternativas, a resposta correta é "Nenhuma das anteriores".
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o valor que será impresso no terminal. 

{{< code >}}
// Arquivo Retangulo.java
public class Retangulo{
 int largura = 5;
 int altura = 10;
 public int area(){
   return largura + altura;
 }
}
// Arquivo Main.java
public Main{
  public static void main(String args[]){
    Retangulo r = new Retangulo();
    System.out.println(r.area());
 }
}
{{< /code >}}

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 15 {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="D" >}}
O método retorna a soma <code>largura + altura</code>, ou seja, 5 + 10 = 15.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o valor que será impresso no terminal. 

{{< code >}}
// Arquivo Retangulo.java
public class Retangulo{
 int largura = 5;
 int altura = 10;
 int area = 50;
 public int area(){
   return largura * altura;
 }
}
// Arquivo Main.java
public Main{
  public static void main(String args[]){
    Retangulo r = new Retangulo();
    System.out.println(r.area);
 }
}
{{< /code >}}

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 50 {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="D" >}}
O código imprime o atributo <code>area</code> diretamente (não o método). Esse atributo foi inicializado com valor 50.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o valor que será impresso no terminal. 

{{< code >}}
// Arquivo A.java
public class A{
 int b = 5;
 int c = 10;
 public int b(){
   return b * c;
 }
}
// Arquivo Main.java
public Main{
  public static void main(String args[]){
    A r = new A();
    System.out.println(r.b);
 }
}
{{< /code >}}

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 50 {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="B" >}}
O código acessa o atributo <code>b</code> diretamente (sem parênteses), cujo valor é 5. O método não é chamado.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o valor que será impresso no terminal. 

{{< code >}}
// Arquivo A.java
public class A{
 int b = 5;
 int c = 10;
 public int b(){
   return b * c;
 }
}
// Arquivo Main.java
public class Main{
  public static void main(String args[]){
    A a = new A();
    System.out.println(a.b());
 }
}
{{< /code >}}

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 50 {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="D" >}}
Neste caso o método <code>b()</code> é chamado, retornando <code>b * c</code>, ou seja, 5 * 10 = 50.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o diagrama abaixo e identifique a alternativa incorreta. 

{{< plantuml >}}
class Retangulo {
  largura : int
  altura : int
  obterArea() : int
}
{{< /plantuml >}}

{{< alternativa >}} A classe se chama Retangulo. {{< /alternativa >}}
{{< alternativa >}} A classe possui um método chamado obterArea. {{< /alternativa >}}
{{< alternativa >}} A classe possui um atributo chamado area. {{< /alternativa >}}
{{< alternativa >}} A classe possui um atributo chamado altura. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="C" >}}
O diagrama mostra apenas os atributos <code>largura</code> e <code>altura</code>. Não existe atributo chamado <code>area</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama abaixo e identifique a alternativa correta. 

{{< plantuml >}}
class A {
  nome : String
}
{{< /plantuml >}}

{{< alternativa >}} A classe se chama B. {{< /alternativa >}}
{{< alternativa >}} A classe possui um método chamado a. {{< /alternativa >}}
{{< alternativa >}} A classe possui um atributo chamado metodo. {{< /alternativa >}}
{{< alternativa >}} A classe possui um atributo com o tipo String. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="D" >}}
O diagrama mostra um atributo <code>nome</code> do tipo <code>String</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama abaixo e identifique a alternativa correta. 

{{< plantuml >}}
class A {
  +b:int
  +c:double
  metodo() : String
}
{{< /plantuml >}}

{{< alternativa >}} A classe se chama B. {{< /alternativa >}}
{{< alternativa >}} A classe possui um método chamado a. {{< /alternativa >}}
{{< alternativa >}} O método retorna um valor do tipo String. {{< /alternativa >}}
{{< alternativa >}} A classe possui um atributo com o tipo String. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="C" >}}
O método  possui retorno do tipo <code>String</code>, como indicado após os dois pontos.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama abaixo e identifique a alternativa correta. 

{{< plantuml >}}
class C {
  metodo() : String
}
{{< /plantuml >}}

{{< alternativa >}} A classe possui atributos. {{< /alternativa >}}
{{< alternativa >}} A classe não possui métodos. {{< /alternativa >}}
{{< alternativa >}} O método retorna um valor do tipo int. {{< /alternativa >}}
{{< alternativa >}} O método possui um parâmetro do tipo String. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="E" >}}
O diagrama mostra que o método retorna <code>String</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama abaixo e identifique a alternativa correta. 

{{< plantuml >}}
class D {
  + b : int
  executar(a:int) : int
}
{{< /plantuml >}}

{{< alternativa >}} A classe possui vários atributos. {{< /alternativa >}}
{{< alternativa >}} A classe não possui métodos. {{< /alternativa >}}
{{< alternativa >}} O método retorna um valor do tipo int. {{< /alternativa >}}
{{< alternativa >}} O método possui um parâmetro do tipo String. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="C" >}}
O diagrama mostra que o método retorna <code>int</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama abaixo e identifique a alternativa correta. 

{{< plantuml >}}
class D {
  + b : int
  executar(a:int)
}
{{< /plantuml >}}

{{< alternativa >}} A classe possui vários atributos. {{< /alternativa >}}
{{< alternativa >}} A classe não possui métodos. {{< /alternativa >}}
{{< alternativa >}} O método retorna um valor do tipo int. {{< /alternativa >}}
{{< alternativa >}} O método possui um parâmetro do tipo String. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="E" >}}
Nenhuma das alternativas anteriores está correta.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama abaixo e identifique a alternativa correta. 

{{< plantuml >}}
class D {
  b : int
  executar(a:int) : String
}
{{< /plantuml >}}

{{< alternativa >}} A classe possui vários atributos. {{< /alternativa >}}
{{< alternativa >}} A classe não possui métodos. {{< /alternativa >}}
{{< alternativa >}} O método retorna um valor do tipo int. {{< /alternativa >}}
{{< alternativa >}} O método possui um parâmetro do tipo String. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="E" >}}
Nenhuma das alternativas anteriores está correta.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama abaixo e identifique a alternativa correta. 

{{< plantuml >}}
class F {
  b : boolean
}
{{< /plantuml >}}

{{< alternativa >}} A classe possui vários atributos. {{< /alternativa >}}
{{< alternativa >}} A classe não possui métodos. {{< /alternativa >}}
{{< alternativa >}} O método retorna um valor do tipo int. {{< /alternativa >}}
{{< alternativa >}} O método possui um parâmetro do tipo String. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="B" >}}
A classe F não possui métodos.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama abaixo e identifique a alternativa correta. 

{{< plantuml >}}
class F {
  b : boolean
}
{{< /plantuml >}}

{{< alternativa >}} A classe possui um atributo com o tipo boolean. {{< /alternativa >}}
{{< alternativa >}} A classe possui um atributo com o nome boolean. {{< /alternativa >}}
{{< alternativa >}} A classe possui um método com o nome b. {{< /alternativa >}}
{{< alternativa >}} A classe possui um método com o nome boolean. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="A" >}}
O atributo <code>b</code> é do tipo <code>boolean</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama abaixo e identifique a alternativa correta. 

{{< plantuml >}}
class G {
  executar() : void
}
{{< /plantuml >}}

{{< alternativa >}} A classe possui um método que não possui retorno. {{< /alternativa >}}
{{< alternativa >}} A classe possui um método que possui retorno com o tipo int. {{< /alternativa >}}
{{< alternativa >}} A classe possui um método que possui retorno com o tipo String. {{< /alternativa >}}
{{< alternativa >}} A classe possui um método que possui retorno com o tipo Vazio. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="A" >}}
O tipo <code>void</code> representa ausência de retorno (valor vazio).
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

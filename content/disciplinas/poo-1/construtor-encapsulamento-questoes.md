---
title: "Questões sobre Construtor e Encapsulamento"
slug: construtor-encapsulamento-questoes
description: "Lista de questões sobre construtor e encapsulamento"
tags:
- construtor
- encapsulamento
- questões
---

{{< lista-questoes >}}


{{< questao >}}
Qual é a definição do construtor?

{{< alternativa >}} Método especial para comparar objeto. {{< /alternativa >}}
{{< alternativa >}} Método especial para reservar um espaço na memória para armazenar o objeto. {{< /alternativa >}}
{{< alternativa >}} Método especial para liberar o  espaço ocupado pelo objeto na memória. {{< /alternativa >}}
{{< alternativa >}} Método especial para auxiliar a inicialização do objeto. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="D">}} O construtor é responsável por inicializar o objeto no momento de sua criação, preparando seus atributos para uso. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a definição do construtor padrão na linguagem Java?

{{< alternativa >}} Construtor obrigatório criado pelo programador. {{< /alternativa >}}
{{< alternativa >}} Construtor obrigatório com vários parâmetros. {{< /alternativa >}}
{{< alternativa >}} Construtor sem parâmetros e vazio gerado automaticamente. {{< /alternativa >}}
{{< alternativa >}} Construtor sem parâmetros e vazio criado pelo programador. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="C">}} O compilador Java gera automaticamente um construtor padrão vazio quando nenhum construtor é definido na classe. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Quais é a definição de encapsulamento no contexto de programação orientada à objetos?

{{< alternativa >}} Processo de ocultar os detalhes do objeto. {{< /alternativa >}}
{{< alternativa >}} Processo de isolar apenas as informações necessárias dos objetos. {{< /alternativa >}}
{{< alternativa >}} Processo de criar objetos com métodos pequenos. {{< /alternativa >}}
{{< alternativa >}} Processo de criar classes para representar os objetos. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="A">}} Encapsulamento consiste em esconder os detalhes internos da implementação e expor apenas o necessário. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é o modificador de acesso que permite o acesso livre?

{{< alternativa >}} público. {{< /alternativa >}}
{{< alternativa >}} protegido. {{< /alternativa >}}
{{< alternativa >}} padrão. {{< /alternativa >}}
{{< alternativa >}} privado. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="A">}} O modificador público permite acesso irrestrito a partir de qualquer classe. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é o modificador de acesso que permite apenas pela própria classe acessar?

{{< alternativa >}} público. {{< /alternativa >}}
{{< alternativa >}} protegido. {{< /alternativa >}}
{{< alternativa >}} padrão. {{< /alternativa >}}
{{< alternativa >}} privado. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="D">}} O modificador privado restringe o acesso apenas à própria classe. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é o propósito do operador new?

{{< alternativa >}} Apenas reservar um espaço na memória para o novo objeto. {{< /alternativa >}}
{{< alternativa >}} Apenas criar um novo objeto. {{< /alternativa >}}
{{< alternativa >}} Auxiliar na inicialização dos atributos de um objeto. {{< /alternativa >}}
{{< alternativa >}} Criar e reservar um espaço na memória para o novo objeto. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="D">}} O operador new cria o objeto e aloca memória para ele. {{< /solucao >}}
{{< /questao >}}



{{< questao >}}
Analise o código abaixo e identifique a forma correta de criar um objeto da classe B. 

{{< code >}}
public class B{
  int a; 
}
{{< /code >}}

{{< alternativa >}} B b= new B(10); {{< /alternativa >}}
{{< alternativa >}} B b= new B(a = 10); {{< /alternativa >}}
{{< alternativa >}} B b= new B(); {{< /alternativa >}}
{{< alternativa >}} B b =  B(); {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="C">}} Como não há construtor definido, o Java cria automaticamente um construtor padrão sem parâmetros. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique a forma correta de criar um objeto da classe B. 

{{< code >}}
public class B{
  int a; 
  public B(){ }
}
{{< /code >}}

{{< alternativa >}} B b= new B(10); {{< /alternativa >}}
{{< alternativa >}} B b= new B(); {{< /alternativa >}}
{{< alternativa >}} B b= new B(a = 10); {{< /alternativa >}}
{{< alternativa >}} B b =  B(); {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="B">}} Existe um construtor sem parâmetros, então a criação correta é com new B(). {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique a forma correta de criar um objeto da classe B. 

{{< code >}}
public class B{
  int a; 
  public B(int a){ }
}
{{< /code >}}

{{< alternativa >}} B b= new B(10); {{< /alternativa >}}
{{< alternativa >}} B b= new B(); {{< /alternativa >}}
{{< alternativa >}} B b= new B(a = 10); {{< /alternativa >}}
{{< alternativa >}} B b =  B(); {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="A">}} Como existe apenas construtor com parâmetro, é obrigatório passar um valor. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique o estado do objeto x. 

{{< code >}}
public class B{
  int a; 
  public B(int a){ this.a = a; }
}
public class Main{
  public static void main(String args[]){
    B x = new B(10);
  }
}
{{< /code >}}

{{< alternativa >}} B{a = 0 }; {{< /alternativa >}}
{{< alternativa >}} B{a = 10 }; {{< /alternativa >}}
{{< alternativa >}} B{a = null }; {{< /alternativa >}}
{{< alternativa >}} B{a = false }; {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="B">}} O valor recebido é atribuído ao atributo usando this.a = a. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique o estado do objeto x. 

{{< code >}}
public class B{
  int a; 
  public B(int a){  a = a;}
}
public class Main{
  public static void main(String args[]){
    B x = new B(10);
  }
}
{{< /code >}}

{{< alternativa >}} B{a = 0 }; {{< /alternativa >}}
{{< alternativa >}} B{a = 10 }; {{< /alternativa >}}
{{< alternativa >}} B{a = null }; {{< /alternativa >}}
{{< alternativa >}} B{a = false }; {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="A">}} A atribuição a = a não altera o atributo da classe, pois usa apenas o parâmetro local. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique o estado do objeto x. 

{{< code >}}
public class B{
  int a; 
  public void setA(int a){ this.a = a * 2;}
}
public class Main{
  public static void main(String args[]){
    B x = new B();
    x.setA(5);
  }
}
{{< /code >}}

{{< alternativa >}} B{a = 0 }; {{< /alternativa >}}
{{< alternativa >}} B{a = 10 }; {{< /alternativa >}}
{{< alternativa >}} B{a = 5 }; {{< /alternativa >}}
{{< alternativa >}} B{a = 20 }; {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="B">}} O valor passado (5) é multiplicado por 2 antes de ser atribuído, resultando em 10. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
De acordo com o padrão Getter/Setter, como deve ser definido um método para obter o valor de um atributo do tipo String nomeado de codigo?

{{< alternativa >}} public String get(){ return codigo; } {{< /alternativa >}}
{{< alternativa >}} public getCodigo(){ return codigo; } {{< /alternativa >}}
{{< alternativa >}} public String getCodigo(){ return codigo; } {{< /alternativa >}}
{{< alternativa >}} public String codigo(){ return codigo; } {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="C">}} O padrão correto é get + nome do atributo com tipo de retorno adequado. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
De acordo com o padrão Getter/Setter, como deve ser definido um método para obter o valor de um atributo do tipo booleano nomeado de ativo?

{{< alternativa >}} public boolean get(){ return ativo;} {{< /alternativa >}}
{{< alternativa >}} public boolean isAtivo(){ return ativo; } {{< /alternativa >}}
{{< alternativa >}} public boolean getAtivo(){ return ativo; } {{< /alternativa >}}
{{< alternativa >}} public boolean ativo(){ return ativo; } {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="B">}} Para booleanos, usa-se o prefixo is. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
De acordo com o padrão Getter/Setter, como deve ser definido um método para modificar o valor de um atributo do tipo double nomeado de preco?

{{< alternativa >}} public void setPreco(double preco){ this.preco = preco; } {{< /alternativa >}}
{{< alternativa >}} public void setPreco(){ this.preco = preco; } {{< /alternativa >}}
{{< alternativa >}} public void setPreco(double preco){ preco = preco; } {{< /alternativa >}}
{{< alternativa >}} public double setPreco(){ return preco; } {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="A">}} Setter correto recebe parâmetro e usa this para atribuir ao atributo. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique o estado do objeto x. 

{{< code >}}
// arquivo B.java
public class B{
  int a; 
  public void setA(int a){ this.a = a;}
  public int getA(){ return a;}
}
// arquivo Main.java
public class Main{
  public static void main(String args[]){
    B x = new B();
    x.setA(5);
  }
}
{{< /code >}}

{{< alternativa >}} B{a = 0 }; {{< /alternativa >}}
{{< alternativa >}} B{a = 10 }; {{< /alternativa >}}
{{< alternativa >}} B{a = 5 }; {{< /alternativa >}}
{{< alternativa >}} B{a = 20 }; {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="C">}}
O objeto é criado com valor padrão 0. Em seguida, o método setA(5) é chamado, que atribui diretamente o valor 5 ao atributo usando this.a = a. Portanto, o estado final do objeto é a = 5.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o diagrama abaixo e identifique a visibilidade do atributo c. 

{{< plantuml >}}
class A{
+b:int
-c:double
+metodo():String
}
{{< /plantuml >}}

{{< alternativa >}} público. {{< /alternativa >}}
{{< alternativa >}} protegido. {{< /alternativa >}}
{{< alternativa >}} padrão. {{< /alternativa >}}
{{< alternativa >}} privado. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="D">}}
Em diagramas UML, o símbolo "-" indica visibilidade privada. Portanto, o atributo c é privado.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o diagrama abaixo e identifique a visibilidade do atributo a. 

{{< plantuml >}}
class H{
+a:int
-c:double
+metodo():String
}
{{< /plantuml >}}

{{< alternativa >}} público. {{< /alternativa >}}
{{< alternativa >}} protegido. {{< /alternativa >}}
{{< alternativa >}} padrão. {{< /alternativa >}}
{{< alternativa >}} privado. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="A">}}
Em UML, o símbolo "+" indica visibilidade pública. Portanto, o atributo a é público.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o diagrama abaixo e identifique a definição correta da classe H na linguagem Java. 

{{< plantuml >}}
class H{
+a:int
+b:int
+metodo():String
}
{{< /plantuml >}}

{{< alternativa >}} public class H { int a; int b; } {{< /alternativa >}}
{{< alternativa >}} public class H { private int a; int b; } {{< /alternativa >}}
{{< alternativa >}} public class H { int a; private int b; } {{< /alternativa >}}
{{< alternativa >}} public class H { public int a; public int b; } {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="D">}}
O diagrama indica ambos os atributos com símbolo "+", ou seja, públicos. Portanto, ambos devem ser declarados como public.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o diagrama abaixo e identifique a definição correta da classe J na linguagem Java. 

{{< plantuml >}}
class J{
+fun():double
}
{{< /plantuml >}}

{{< alternativa >}} public class J { public fun(){ } } {{< /alternativa >}}
{{< alternativa >}} public class J { private fun(){ }  } {{< /alternativa >}}
{{< alternativa >}} public class J { public double fun(){ }  } {{< /alternativa >}}
{{< alternativa >}} public class J { public double fun(){ return 0;  }  } {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="D">}}
O diagrama indica método público com retorno double. Em Java, métodos com retorno devem obrigatoriamente retornar um valor, portanto a alternativa correta inclui "return 0".
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o diagrama abaixo e identifique a definição correta da classe J na linguagem Java. 

{{< plantuml >}}
class J{
+fun(a:int)
}
{{< /plantuml >}}

{{< alternativa >}} public class J { public fun(a : int){ } } {{< /alternativa >}}
{{< alternativa >}} public class J { private void fun(){ }  } {{< /alternativa >}}
{{< alternativa >}} public class J { public int fun(){ }  } {{< /alternativa >}}
{{< alternativa >}} public class J { public int fun(int a){ return 0; }  } {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="E">}}
O diagrama indica método público com parâmetro inteiro e sem retorno. Em Java, isso corresponde a "public void fun(int a)" com retorno válido.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o diagrama abaixo e identifique a definição correta da classe J na linguagem Java. 

{{< plantuml >}}
class J{
-fun(a:int)
}
{{< /plantuml >}}

{{< alternativa >}} public class J { public fun(a : int){ } } {{< /alternativa >}}
{{< alternativa >}} public class J { private void fun(){ }  } {{< /alternativa >}}
{{< alternativa >}} public class J { private void fun(int a){ }  } {{< /alternativa >}}
{{< alternativa >}} public class J { public int fun(int a){ return 0; }  } {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="C">}}
O diagrama mostra método privado com parâmetro inteiro e sem retorno (void), portanto corresponde a "private void fun(int a)".
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o diagrama abaixo e identifique a definição correta da classe J na linguagem Java. 

{{< plantuml >}}
class J{
+fun(b:String, a:int) : int
}
{{< /plantuml >}}

{{< alternativa >}} public class J { public fun(b: String, a : int){ } } {{< /alternativa >}}
{{< alternativa >}} public class J { private String fun( int a){ }  } {{< /alternativa >}}
{{< alternativa >}} public class J { private void fun(int a){ }  } {{< /alternativa >}}
{{< alternativa >}} public class J { public int fun(String b, int a){ return 0; }  } {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="D">}}
O diagrama indica método público com dois parâmetros (String e int) e retorno inteiro. A alternativa correta respeita assinatura e retorno.
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

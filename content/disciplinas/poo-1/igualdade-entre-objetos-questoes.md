---
title: "Questões sobre Igualdade entre objetos"
slug: igualdade-entre-objetos-questoes
description: "Lista de questões sobre igualdade entre objetos"
tags:
- igualdade
- equals
- hashcode
- questões
---

{{< lista-questoes >}}


{{< questao >}}
Qual é o objetivo do método toString?

{{< alternativa >}} Método  para comparar igualdade entre objetos. {{< /alternativa >}}
{{< alternativa >}} Método  que transforma o objeto em uma representação de texto. {{< /alternativa >}}
{{< alternativa >}} Método  que transforma o objeto em um único número. {{< /alternativa >}}
{{< alternativa >}} Método especial para auxiliar a inicialização do objeto. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="B">}} O método toString é utilizado para retornar uma representação textual do objeto. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é o objetivo do método hashCode?

{{< alternativa >}} Método  para comparar igualdade entre objetos. {{< /alternativa >}}
{{< alternativa >}} Método  que transforma o objeto em uma representação de texto. {{< /alternativa >}}
{{< alternativa >}} Método  que transforma o objeto em um único número. {{< /alternativa >}}
{{< alternativa >}} Método especial para auxiliar a inicialização do objeto. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="C">}} O método hashCode retorna um número inteiro que representa o objeto, usado em estruturas como HashMap. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é o objetivo do método equals?

{{< alternativa >}} Método  para comparar igualdade entre objetos. {{< /alternativa >}}
{{< alternativa >}} Método  que transforma o objeto em uma representação de texto. {{< /alternativa >}}
{{< alternativa >}} Método  que transforma o objeto em um único número. {{< /alternativa >}}
{{< alternativa >}} Método especial para auxiliar a inicialização do objeto. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="A">}} O método equals é utilizado para comparar se dois objetos são considerados iguais. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique qual informação é mais provável ser impressa no terminal. 

{{< code >}}
// Arquivo Retangulo.java
public class Retangulo{ }
// Arquivo Main.java
public class Main{
  public static void main(String args[]){
    Retangulo r = new Retangulo();
    System.out.println(r);
  }
}
{{< /code >}}

{{< alternativa >}} r {{< /alternativa >}}
{{< alternativa >}} 12334 {{< /alternativa >}}
{{< alternativa >}} Retangulo {{< /alternativa >}}
{{< alternativa >}} Retangulo@F123A {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="D">}} Sem sobrescrever toString, o Java imprime o nome da classe seguido de um código hexadecimal. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique qual informação é mais provável ser impressa no terminal. 

{{< code >}}
// Arquivo Retangulo.java
public class Retangulo{  
 public String toString(){
   return "Retangulo";
 }
}
// Arquivo Main.java
public class Main{
  public static void main(String args[]){
    Retangulo r = new Retangulo();
    System.out.println(r);
  }
}
{{< /code >}}

{{< alternativa >}} r {{< /alternativa >}}
{{< alternativa >}} 12334 {{< /alternativa >}}
{{< alternativa >}} Retangulo {{< /alternativa >}}
{{< alternativa >}} Retangulo@F123A {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="C">}} O método toString foi sobrescrito para retornar "Retangulo". {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique qual informação é mais provável ser impressa no terminal. 

{{< code >}}
// Arquivo Retangulo.java
public class Retangulo{  
 public String toString(){
   return "Retangulo";
 }
}
// Arquivo Main.java
public class Main{
  public static void main(String args[]){
    Retangulo r = new Retangulo();
    System.out.println(r.hashCode());
  }
}
{{< /code >}}

{{< alternativa >}} r {{< /alternativa >}}
{{< alternativa >}} 12334 {{< /alternativa >}}
{{< alternativa >}} Retangulo {{< /alternativa >}}
{{< alternativa >}} Retangulo@F123A {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="B">}} O método hashCode retorna um número inteiro, portanto será exibido um valor numérico. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique qual informação é mais provável ser impressa no terminal. 

{{< code >}}
// Arquivo Retangulo.java
public class Retangulo{  
 public int hashCode(){
   return 0;
 }
}
// Arquivo Main.java
public class Main{
  public static void main(String args[]){
    Retangulo r = new Retangulo();
    System.out.println(r);
  }
}
{{< /code >}}

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 12334 {{< /alternativa >}}
{{< alternativa >}} Retangulo {{< /alternativa >}}
{{< alternativa >}} Retangulo@F123A {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="D">}} O método toString não foi sobrescrito, então a saída será o padrão (classe + hash em hexadecimal). {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere uma classe chamada Retangulo. Nesta classe não foi implementado os métodos equals e hashCode. Analise o código abaixo e identifique qual informação é mais provável ser impressa no terminal. 

{{< code >}}
public class Main{
  public static void main(String args[]){
    Retangulo r1 = new Retangulo();
    r1.setLargura(10);
    r1.setAltura(10);
    Retangulo r2 = new Retangulo();
    r2.setLargura(10);
    r2.setAltura(10);
    System.out.println(r1 == r2);
  }
}
{{< /code >}}

{{< alternativa >}} false, porque os objetos possuem valores diferentes. {{< /alternativa >}}
{{< alternativa >}} false, porque os objetos possuem endereços de memória diferentes. {{< /alternativa >}}
{{< alternativa >}} true, porque os objetos possuem o mesmo endereço de memória. {{< /alternativa >}}
{{< alternativa >}} true, porque os objetos possuem os mesmos valores. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="B">}} O operador == compara referências, não conteúdo. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere uma classe chamada Retangulo. Nesta classe não foi implementado os métodos equals e hashCode. Analise o código abaixo e identifique qual informação é mais provável ser impressa no terminal. 

{{< code >}}
public class Main{
  public static void main(String args[]){
    Retangulo r1 = new Retangulo();
    r1.setLargura(10);
    r1.setAltura(10);
    Retangulo r2 = new Retangulo();
    r2.setLargura(10);
    r2.setAltura(10);
    System.out.println(r1.equals(r2));
  }
}
{{< /code >}}

{{< alternativa >}} false, porque os objetos possuem valores diferentes. {{< /alternativa >}}
{{< alternativa >}} false, porque os objetos possuem endereços de memória diferentes. {{< /alternativa >}}
{{< alternativa >}} true, porque os objetos possuem o mesmo endereço de memória. {{< /alternativa >}}
{{< alternativa >}} true, porque os objetos possuem os mesmos valores. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="B">}} Sem sobrescrita, equals se comporta como ==. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere uma classe chamada Retangulo. Nesta classe foi implementado corretamente os métodos equals e hashCode. Analise o código abaixo e identifique qual informação é mais provável ser impressa no terminal. 

{{< code >}}
public class Main{
  public static void main(String args[]){
    Retangulo r1 = new Retangulo();
    r1.setLargura(10);
    r1.setAltura(10);
    Retangulo r2 = new Retangulo();
    r2.setLargura(10);
    r2.setAltura(10);
    System.out.println(r1 == r2);
  }
}
{{< /code >}}

{{< alternativa >}} false, porque os objetos possuem valores diferentes. {{< /alternativa >}}
{{< alternativa >}} false, porque os objetos possuem endereços de memória diferentes. {{< /alternativa >}}
{{< alternativa >}} true, porque os objetos possuem o mesmo endereço de memória. {{< /alternativa >}}
{{< alternativa >}} true, porque os objetos possuem os mesmos valores. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="B">}} Mesmo com equals/hashCode implementados, == compara referência. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere uma classe chamada Retangulo. Nesta classe  foi implementado corretamente os métodos equals e hashCode. Analise o código abaixo e identifique qual informação é mais provável ser impressa no terminal. 

{{< code >}}
public class Main{
  public static void main(String args[]){
    Retangulo r1 = new Retangulo();
    r1.setLargura(10);
    r1.setAltura(10);
    Retangulo r2 = new Retangulo();
    r2.setLargura(10);
    r2.setAltura(10);
    System.out.println(r1.equals(r2));
  }
}
{{<  /code >}}

{{< alternativa >}} false, porque os objetos possuem valores diferentes. {{< /alternativa >}}
{{< alternativa >}} false, porque os objetos possuem endereços de memória diferentes. {{< /alternativa >}}
{{< alternativa >}} true, porque os objetos possuem o mesmo endereço de memória. {{< /alternativa >}}
{{< alternativa >}} true, porque os objetos possuem os mesmos valores. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="D">}} Com equals implementado corretamente, objetos com mesmos valores são iguais. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere uma classe chamada Retangulo. Nesta classe  foi implementado corretamente os métodos equals e hashCode. Analise o código abaixo e identifique qual informação é mais provável ser impressa no terminal. 

{{<  code >}}
public class Main{
  public static void main(String args[]){
    Retangulo r1 = new Retangulo();
    r1.setLargura(10);
    r1.setAltura(10);
    Retangulo r2 = new Retangulo();
    r2.setLargura(20);
    r2.setAltura(10);
    System.out.println(r1.equals(r2));
  }
}
{{<  /code >}}

{{< alternativa >}} false, porque os objetos possuem valores diferentes. {{< /alternativa >}}
{{< alternativa >}} false, porque os objetos possuem endereços de memória diferentes. {{< /alternativa >}}
{{< alternativa >}} true, porque os objetos possuem o mesmo endereço de memória. {{< /alternativa >}}
{{< alternativa >}} true, porque os objetos possuem os mesmos valores. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}
{{< solucao letra="A">}} Como os valores são diferentes, equals retorna false. {{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

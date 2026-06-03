---
title: "Questões sobre Tipos Genéricos"
slug: tipos-genericos-questoes
description: "Lista de questões sobre tipos genéricos"
tags:
- tipos genericos
- questões
---

{{< lista-questoes >}}

{{< questao >}}
O que são tipos genéricos (Generics) em Java?

{{< alternativa >}} Um mecanismo para criar classes sem atributos. {{< /alternativa >}}
{{< alternativa >}} Um recurso que permite parametrizar tipos. {{< /alternativa >}}
{{< alternativa >}} Um tipo especial de interface. {{< /alternativa >}}
{{< alternativa >}} Um modificador de acesso. {{< /alternativa >}}

{{< solucao letra="B" >}}
Generics permitem criar classes, interfaces e métodos que trabalham com diferentes tipos de dados de forma segura.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Qual símbolo é utilizado para declarar um parâmetro de tipo genérico?

{{< alternativa >}} (T) {{< /alternativa >}}
{{< alternativa >}} [T] {{< /alternativa >}}
{{< alternativa >}} <T> {{< /alternativa >}}
{{< alternativa >}} {T} {{< /alternativa >}}

{{< solucao letra="C" >}}
Os parâmetros de tipo são declarados entre sinais de menor e maior, como <code>&lt;T&gt;</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public class Caixa<T>{
}
{{< /code >}}

Qual alternativa está correta?

{{< alternativa >}} Caixa é uma interface. {{< /alternativa >}}
{{< alternativa >}} Caixa possui um parâmetro de tipo chamado T. {{< /alternativa >}}
{{< alternativa >}} T é um atributo. {{< /alternativa >}}
{{< alternativa >}} O código possui erro. {{< /alternativa >}}

{{< solucao letra="B" >}}
A classe foi declarada com um parâmetro de tipo genérico chamado <code>T</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Qual é o principal benefício dos tipos genéricos?

{{< alternativa >}} Aumentar o tamanho dos objetos. {{< /alternativa >}}
{{< alternativa >}} Eliminar a necessidade de classes. {{< /alternativa >}}
{{< alternativa >}} Proporcionar segurança de tipos em tempo de compilação. {{< /alternativa >}}
{{< alternativa >}} Tornar todos os métodos estáticos. {{< /alternativa >}}

{{< solucao letra="C" >}}
Generics ajudam a detectar erros de tipo durante a compilação.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
Caixa<String> caixa = new Caixa<>();
{{< /code >}}

Qual é o tipo associado ao parâmetro T?

{{< alternativa >}} Object {{< /alternativa >}}
{{< alternativa >}} String {{< /alternativa >}}
{{< alternativa >}} int {{< /alternativa >}}
{{< alternativa >}} Caixa {{< /alternativa >}}

{{< solucao letra="B" >}}
Ao utilizar <code>Caixa&lt;String&gt;</code>, o parâmetro genérico T representa o tipo String.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public class Caixa<T>{
    private T valor;
}
{{< /code >}}

Qual é o tipo do atributo valor?

{{< alternativa >}} String {{< /alternativa >}}
{{< alternativa >}} int {{< /alternativa >}}
{{< alternativa >}} T {{< /alternativa >}}
{{< alternativa >}} Object {{< /alternativa >}}

{{< solucao letra="C" >}}
O atributo utiliza o parâmetro genérico T definido pela classe.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
List<String> nomes = new ArrayList<>();
{{< /code >}}

Qual tipo de elemento pode ser armazenado na lista?

{{< alternativa >}} Apenas String. {{< /alternativa >}}
{{< alternativa >}} Apenas Integer. {{< /alternativa >}}
{{< alternativa >}} Qualquer objeto. {{< /alternativa >}}
{{< alternativa >}} Apenas Object. {{< /alternativa >}}

{{< solucao letra="A" >}}
A lista foi parametrizada com <code>String</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
List<Integer> numeros = new ArrayList<>();
numeros.add(10);
numeros.add(20);
{{< /code >}}

Quantos elementos existem na lista?

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}

{{< solucao letra="C" >}}
Foram adicionados dois elementos do tipo Integer.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
List<Integer> numeros = new ArrayList<>();
numeros.add("10");
{{< /code >}}

O que acontece?

{{< alternativa >}} O código executa normalmente. {{< /alternativa >}}
{{< alternativa >}} O valor é convertido automaticamente. {{< /alternativa >}}
{{< alternativa >}} Ocorre erro de compilação. {{< /alternativa >}}
{{< alternativa >}} O valor é ignorado. {{< /alternativa >}}

{{< solucao letra="C" >}}
A lista aceita apenas elementos do tipo Integer.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public class Par<K,V>{
}
{{< /code >}}

Quantos parâmetros de tipo foram declarados?

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}

{{< solucao letra="C" >}}
A classe possui dois parâmetros genéricos: <code>K</code> e <code>V</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public class Caixa<T>{
    private T valor;

    public T getValor(){
        return valor;
    }
}
{{< /code >}}

Qual é o tipo de retorno do método getValor?

{{< alternativa >}} void {{< /alternativa >}}
{{< alternativa >}} Object {{< /alternativa >}}
{{< alternativa >}} T {{< /alternativa >}}
{{< alternativa >}} String {{< /alternativa >}}

{{< solucao letra="C" >}}
O método retorna um valor do tipo definido pelo parâmetro genérico T.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
class Caixa<T> {
  valor : T
}
{{< /plantuml >}}

Qual é o tipo do atributo valor?

{{< alternativa >}} String {{< /alternativa >}}
{{< alternativa >}} int {{< /alternativa >}}
{{< alternativa >}} T {{< /alternativa >}}
{{< alternativa >}} Object {{< /alternativa >}}

{{< solucao letra="C" >}}
O atributo utiliza o parâmetro de tipo genérico T.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
class Par<K,V> {
}
{{< /plantuml >}}

Qual alternativa está correta?

{{< alternativa >}} Par possui dois parâmetros genéricos. {{< /alternativa >}}
{{< alternativa >}} Par possui dois atributos. {{< /alternativa >}}
{{< alternativa >}} Par é uma interface. {{< /alternativa >}}
{{< alternativa >}} O diagrama possui erro. {{< /alternativa >}}

{{< solucao letra="A" >}}
A notação <code>&lt;K,V&gt;</code> indica dois parâmetros de tipo.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
class Caixa<T> {
  +getValor() : T
}
{{< /plantuml >}}

Qual é o tipo de retorno de getValor()?

{{< alternativa >}} void {{< /alternativa >}}
{{< alternativa >}} T {{< /alternativa >}}
{{< alternativa >}} String {{< /alternativa >}}
{{< alternativa >}} int {{< /alternativa >}}

{{< solucao letra="B" >}}
O método retorna um valor do tipo genérico T.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
class Repositorio<T> {
  +salvar(obj : T) : void
}
{{< /plantuml >}}

Quantos parâmetros possui o método salvar?

{{< alternativa >}} Nenhum {{< /alternativa >}}
{{< alternativa >}} Um parâmetro do tipo T {{< /alternativa >}}
{{< alternativa >}} Dois parâmetros do tipo T {{< /alternativa >}}
{{< alternativa >}} Um parâmetro do tipo Object {{< /alternativa >}}

{{< solucao letra="B" >}}
O método recebe um parâmetro chamado <code>obj</code> do tipo T.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
List<Double> notas = new ArrayList<>();
{{< /code >}}

Qual alternativa está correta?

{{< alternativa >}} A lista armazena apenas Double. {{< /alternativa >}}
{{< alternativa >}} A lista armazena apenas String. {{< /alternativa >}}
{{< alternativa >}} A lista armazena qualquer tipo. {{< /alternativa >}}
{{< alternativa >}} O código possui erro. {{< /alternativa >}}

{{< solucao letra="A" >}}
O parâmetro genérico define que apenas objetos do tipo Double podem ser armazenados.
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

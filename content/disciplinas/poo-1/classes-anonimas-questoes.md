---
title: "Questões sobre Classes Anônimas"
slug: classes-anonimas-questoes
description: "Lista de questões sobre classes anônimas"
tags:
- classes abstratas
- questões
---

{{< lista-questoes >}}

{{< questao >}}
O que é uma classe anônima em Java?

{{< alternativa >}} Uma classe declarada sem atributos. {{< /alternativa >}}
{{< alternativa >}} Uma classe que não possui construtor. {{< /alternativa >}}
{{< alternativa >}} Uma classe sem nome criada no momento da instanciação. {{< /alternativa >}}
{{< alternativa >}} Uma interface sem métodos. {{< /alternativa >}}

{{< solucao letra="C" >}}
Uma classe anônima é uma classe sem nome declarada e instanciada em uma única expressão.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Qual é uma característica das classes anônimas?

{{< alternativa >}} Podem ser reutilizadas em vários arquivos. {{< /alternativa >}}
{{< alternativa >}} Não possuem nome explícito. {{< /alternativa >}}
{{< alternativa >}} Devem ser declaradas em arquivos próprios. {{< /alternativa >}}
{{< alternativa >}} Não podem sobrescrever métodos. {{< /alternativa >}}

{{< solucao letra="B" >}}
Classes anônimas não recebem um nome definido pelo programador.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
Runnable r = new Runnable() {
    public void run() {
        System.out.println("Executando");
    }
};
{{< /code >}}

Qual alternativa está correta?

{{< alternativa >}} Foi criada uma classe anônima. {{< /alternativa >}}
{{< alternativa >}} Foi criada uma interface. {{< /alternativa >}}
{{< alternativa >}} O código possui erro de compilação. {{< /alternativa >}}
{{< alternativa >}} Runnable é uma classe abstrata. {{< /alternativa >}}

{{< solucao letra="A" >}}
Uma implementação anônima da interface Runnable foi criada.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Uma classe anônima pode herdar de uma classe?

{{< alternativa >}} Sim. {{< /alternativa >}}
{{< alternativa >}} Não. {{< /alternativa >}}
{{< alternativa >}} Apenas se a classe for final. {{< /alternativa >}}
{{< alternativa >}} Apenas se a classe for abstrata. {{< /alternativa >}}

{{< solucao letra="A" >}}
Uma classe anônima pode estender uma classe existente.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Uma classe anônima pode implementar interfaces?

{{< alternativa >}} Sim. {{< /alternativa >}}
{{< alternativa >}} Não. {{< /alternativa >}}
{{< alternativa >}} Apenas interfaces funcionais. {{< /alternativa >}}
{{< alternativa >}} Apenas interfaces vazias. {{< /alternativa >}}

{{< solucao letra="A" >}}
É comum utilizar classes anônimas para implementar interfaces.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
Runnable r = new Runnable() {
    public void run() {
        System.out.println("Olá");
    }
};
{{< /code >}}

Qual método foi implementado?

{{< alternativa >}} start() {{< /alternativa >}}
{{< alternativa >}} execute() {{< /alternativa >}}
{{< alternativa >}} run() {{< /alternativa >}}
{{< alternativa >}} main() {{< /alternativa >}}

{{< solucao letra="C" >}}
A interface Runnable possui o método <code>run()</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
Object obj = new Object() {
};
{{< /code >}}

Qual alternativa está correta?

{{< alternativa >}} Foi criada uma classe anônima que estende Object. {{< /alternativa >}}
{{< alternativa >}} O código possui erro. {{< /alternativa >}}
{{< alternativa >}} Foi criada uma interface. {{< /alternativa >}}
{{< alternativa >}} Object tornou-se abstrata. {{< /alternativa >}}

{{< solucao letra="A" >}}
A expressão cria uma subclasse anônima de Object.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Qual é a principal vantagem das classes anônimas?

{{< alternativa >}} Reduzir código quando a implementação será utilizada apenas uma vez. {{< /alternativa >}}
{{< alternativa >}} Aumentar o desempenho da JVM. {{< /alternativa >}}
{{< alternativa >}} Eliminar o uso de interfaces. {{< /alternativa >}}
{{< alternativa >}} Evitar a criação de objetos. {{< /alternativa >}}

{{< solucao letra="A" >}}
Classes anônimas são úteis para implementações simples e de uso único.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public abstract class Animal {
    public abstract void emitirSom();
}

Animal a = new Animal() {
    public void emitirSom() {
        System.out.println("Som");
    }
};
{{< /code >}}

Qual alternativa está correta?

{{< alternativa >}} O código possui erro. {{< /alternativa >}}
{{< alternativa >}} Foi criada uma classe anônima que implementa emitirSom(). {{< /alternativa >}}
{{< alternativa >}} Animal deixou de ser abstrata. {{< /alternativa >}}
{{< alternativa >}} emitirSom() tornou-se estático. {{< /alternativa >}}

{{< solucao letra="B" >}}
A classe anônima fornece a implementação do método abstrato.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
Runnable r = new Runnable() {
    public void run() {
        System.out.println("Executando");
    }
};
r.run();
{{< /code >}}

O que será exibido?

{{< alternativa >}} Nada. {{< /alternativa >}}
{{< alternativa >}} Erro de compilação. {{< /alternativa >}}
{{< alternativa >}} Executando {{< /alternativa >}}
{{< alternativa >}} run {{< /alternativa >}}

{{< solucao letra="C" >}}
O método <code>run()</code> imprime a mensagem "Executando".
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
interface Runnable {
  +run() : void
}
{{< /plantuml >}}

Qual método deve ser implementado por uma classe anônima baseada nessa interface?

{{< alternativa >}} start() {{< /alternativa >}}
{{< alternativa >}} execute() {{< /alternativa >}}
{{< alternativa >}} run() {{< /alternativa >}}
{{< alternativa >}} main() {{< /alternativa >}}

{{< solucao letra="C" >}}
A interface define apenas o método <code>run()</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
abstract class Animal {
  {abstract} emitirSom() : void
}
{{< /plantuml >}}

Para criar uma instância utilizando classe anônima é necessário:

{{< alternativa >}} Remover o abstract da classe. {{< /alternativa >}}
{{< alternativa >}} Implementar os métodos abstratos. {{< /alternativa >}}
{{< alternativa >}} Tornar o método privado. {{< /alternativa >}}
{{< alternativa >}} Transformar a classe em interface. {{< /alternativa >}}

{{< solucao letra="B" >}}
A classe anônima deve fornecer implementação para todos os métodos abstratos.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
Comparator<Integer> c = new Comparator<Integer>() {
    public int compare(Integer a, Integer b) {
        return a - b;
    }
};
{{< /code >}}

Qual método foi implementado?

{{< alternativa >}} equals() {{< /alternativa >}}
{{< alternativa >}} compare() {{< /alternativa >}}
{{< alternativa >}} sort() {{< /alternativa >}}
{{< alternativa >}} compareTo() {{< /alternativa >}}

{{< solucao letra="B" >}}
A interface Comparator define o método <code>compare()</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
interface Comparator<T> {
  +compare(a:T, b:T) : int
}
{{< /plantuml >}}

Qual é o tipo de retorno do método compare?

{{< alternativa >}} boolean {{< /alternativa >}}
{{< alternativa >}} void {{< /alternativa >}}
{{< alternativa >}} String {{< /alternativa >}}
{{< alternativa >}} int {{< /alternativa >}}

{{< solucao letra="D" >}}
O diagrama indica retorno do tipo <code>int</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o diagrama UML abaixo.

{{< plantuml >}}
interface Acao {
  +executar() : void
}
{{< /plantuml >}}

Qual código representa uma implementação por classe anônima?

{{< alternativa >}}
{{< code >}}
Acao a = new Acao() {
    public void executar() {}
};
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
Acao a = new Acao();
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
new interface Acao();
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
Acao.executar();
{{< /code >}}
{{< /alternativa >}}

{{< solucao letra="A" >}}
Uma classe anônima implementa o método da interface diretamente na instanciação.
{{< /solucao >}}
{{< /questao >}}


{{< /lista-questoes >}}

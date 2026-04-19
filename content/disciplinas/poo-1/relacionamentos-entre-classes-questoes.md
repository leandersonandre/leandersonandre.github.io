---
title: "Questões sobre Relacionamentos entre classes"
slug: relacionamento-entre-objetos-questoes
description: "Lista de questões sobre relacionamentos entre objetos"
tags:
- agregação
- composição
- dependência
- associação
- questões
---

{{< lista-questoes >}}

{{< lista-questoes >}}

{{< questao >}}
Qual é a definição de dependência entre classes na Programação Orientada a Objetos?
{{< alternativa >}} Relação em que uma classe possui outra como atributo permanente. {{< /alternativa >}}
{{< alternativa >}} Relação fraca em que uma classe utiliza outra temporariamente. {{< /alternativa >}}
{{< alternativa >}} Relação em que duas classes têm o mesmo ciclo de vida. {{< /alternativa >}}
{{< alternativa >}} Relação em que uma classe herda de outra. {{< /alternativa >}}
{{< solucao letra="B">}} Dependência ocorre quando uma classe usa outra apenas em algum método, sem manter referência permanente. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a definição de associação entre classes?
{{< alternativa >}} Relação de uso temporário entre classes. {{< /alternativa >}}
{{< alternativa >}} Relação estrutural onde uma classe mantém referência a outra. {{< /alternativa >}}
{{< alternativa >}} Relação de herança entre classes. {{< /alternativa >}}
{{< alternativa >}} Relação onde objetos são destruídos juntos sempre. {{< /alternativa >}}
{{< solucao letra="B">}} Associação representa uma relação estrutural entre objetos, geralmente com referência em atributos. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
No diagrama abaixo, qual tipo de relacionamento é representado?
{{< plantuml >}}
class A
class B
A .L.> B
{{< /plantuml >}}
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< alternativa >}} Associação {{< /alternativa >}}
{{< alternativa >}} Agregação {{< /alternativa >}}
{{< alternativa >}} Composição {{< /alternativa >}}
{{< solucao letra="A">}} A seta simples com linha tracejada indica dependência em UML. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
No diagrama abaixo, qual tipo de relacionamento é representado?
{{< plantuml >}}
class A
class B
A -L- B
{{< /plantuml >}}
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< alternativa >}} Associação {{< /alternativa >}}
{{< alternativa >}} Herança {{< /alternativa >}}
{{< alternativa >}} Composição {{< /alternativa >}}
{{< solucao letra="B">}} Linha simples indica associação entre classes. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a principal característica da agregação?
{{< alternativa >}} Forte dependência de ciclo de vida. {{< /alternativa >}}
{{< alternativa >}} Relação onde o todo controla a existência das partes. {{< /alternativa >}}
{{< alternativa >}} Relação fraca onde partes podem existir independentemente. {{< /alternativa >}}
{{< alternativa >}} Relação de herança múltipla. {{< /alternativa >}}
{{< solucao letra="C">}} Na agregação, objetos podem existir independentemente do todo. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a principal característica da composição?
{{< alternativa >}} Objetos independentes. {{< /alternativa >}}
{{< alternativa >}} Parte pode existir sem o todo. {{< /alternativa >}}
{{< alternativa >}} Forte relação de ciclo de vida compartilhado. {{< /alternativa >}}
{{< alternativa >}} Relação de dependência temporária. {{< /alternativa >}}
{{< solucao letra="C">}} Na composição, a parte depende totalmente do todo. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
No diagrama abaixo, qual relacionamento é representado?
{{< plantuml >}}
class A
class B
A o-R- B
{{< /plantuml >}}
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< alternativa >}} Associação {{< /alternativa >}}
{{< alternativa >}} Agregação {{< /alternativa >}}
{{< alternativa >}} Composição {{< /alternativa >}}
{{< solucao letra="C">}} O losango vazio indica agregação. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
No diagrama abaixo, qual relacionamento é representado?
{{< plantuml >}}
class A
class B
A *-R- B
{{< /plantuml >}}
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< alternativa >}} Associação {{< /alternativa >}}
{{< alternativa >}} Agregação {{< /alternativa >}}
{{< alternativa >}} Composição {{< /alternativa >}}
{{< solucao letra="D">}} O losango preenchido indica composição. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual cenário melhor representa dependência?
{{< alternativa >}} Carro possui motor. {{< /alternativa >}}
{{< alternativa >}} Pessoa usa uma calculadora em um método. {{< /alternativa >}}
{{< alternativa >}} Escola possui alunos. {{< /alternativa >}}
{{< alternativa >}} Casa possui quartos. {{< /alternativa >}}
{{< solucao letra="B">}} Uso temporário caracteriza dependência. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual cenário melhor representa composição?
{{< alternativa >}} Carro e motor. {{< /alternativa >}}
{{< alternativa >}} Professor usa livro. {{< /alternativa >}}
{{< alternativa >}} Cliente usa sistema. {{< /alternativa >}}
{{< alternativa >}} Aluno consulta biblioteca. {{< /alternativa >}}
{{< solucao letra="A">}} Motor não existe sem o carro (composição). {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual cenário melhor representa agregação?
{{< alternativa >}} Casa e parede. {{< /alternativa >}}
{{< alternativa >}} Escola e alunos. {{< /alternativa >}}
{{< alternativa >}} Motor e carro. {{< /alternativa >}}
{{< alternativa >}} Pessoa e coração. {{< /alternativa >}}
{{< solucao letra="B">}} Alunos podem existir independentemente da escola. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo:
{{< code >}}
class A {
    void metodo() {
        B b = new B();
    }
}
{{< /code >}}
Qual relacionamento existe?
{{< alternativa >}} Associação {{< /alternativa >}}
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< alternativa >}} Composição {{< /alternativa >}}
{{< alternativa >}} Agregação {{< /alternativa >}}
{{< solucao letra="B">}} O objeto é usado apenas dentro do método. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo:
{{< code >}}
class A {
    B b;
}
{{< /code >}}
Qual relacionamento existe?
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< alternativa >}} Associação {{< /alternativa >}}
{{< alternativa >}} Herança {{< /alternativa >}}
{{< alternativa >}} Nenhum {{< /alternativa >}}
{{< solucao letra="B">}} Uso como atributo indica associação. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo:
{{< code >}}
class Casa {
    private final Porta porta = new Porta();
}
{{< /code >}}
Qual relacionamento existe?
{{< alternativa >}} Agregação {{< /alternativa >}}
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< alternativa >}} Composição {{< /alternativa >}}
{{< alternativa >}} Associação simples {{< /alternativa >}}
{{< solucao letra="C">}} Porta criada internamente indica composição. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o diagrama abaixo:
{{< plantuml >}}
class Escola
class Aluno
Escola "1" o-- "*" Aluno
{{< /plantuml >}}
Qual relacionamento?
{{< alternativa >}} Composição {{< /alternativa >}}
{{< alternativa >}} Agregação {{< /alternativa >}}
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< alternativa >}} Herança {{< /alternativa >}}
{{< solucao letra="B">}} Multiplicidade com losango vazio indica agregação. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o diagrama abaixo:
{{< plantuml >}}
class Carro
class Motor
Carro *-- Motor
{{< /plantuml >}}
Qual relacionamento?
{{< alternativa >}} Agregação {{< /alternativa >}}
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< alternativa >}} Composição {{< /alternativa >}}
{{< alternativa >}} Associação {{< /alternativa >}}
{{< solucao letra="C">}} Losango preenchido indica composição. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que significa multiplicidade 1..*?
{{< alternativa >}} Nenhum objeto {{< /alternativa >}}
{{< alternativa >}} Exatamente um objeto {{< /alternativa >}}
{{< alternativa >}} Um ou mais objetos {{< /alternativa >}}
{{< alternativa >}} Zero ou um objeto {{< /alternativa >}}
{{< solucao letra="C">}} Indica um ou mais instâncias. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que significa multiplicidade 0..1?
{{< alternativa >}} Um ou mais objetos {{< /alternativa >}}
{{< alternativa >}} Zero ou um objeto {{< /alternativa >}}
{{< alternativa >}} Exatamente um objeto {{< /alternativa >}}
{{< alternativa >}} Zero ou mais objetos {{< /alternativa >}}
{{< solucao letra="B">}} Pode existir ou não existir objeto. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual relacionamento é mais fraco?
{{< alternativa >}} Composição {{< /alternativa >}}
{{< alternativa >}} Agregação {{< /alternativa >}}
{{< alternativa >}} Associação {{< /alternativa >}}
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< solucao letra="D">}} Dependência é o relacionamento mais fraco. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual relacionamento representa “tem-um” forte?
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< alternativa >}} Associação {{< /alternativa >}}
{{< alternativa >}} Agregação {{< /alternativa >}}
{{< alternativa >}} Composição {{< /alternativa >}}
{{< solucao letra="D">}} Composição representa forte relação de posse. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual relacionamento representa “usa-um”?
{{< alternativa >}} Composição {{< /alternativa >}}
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< alternativa >}} Herança {{< /alternativa >}}
{{< alternativa >}} Agregação {{< /alternativa >}}
{{< solucao letra="B">}} Uso temporário indica dependência. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é o símbolo de agregação em UML?
{{< alternativa >}} Setinha simples {{< /alternativa >}}
{{< alternativa >}} Losango vazio {{< /alternativa >}}
{{< alternativa >}} Losango cheio {{< /alternativa >}}
{{< alternativa >}} Linha pontilhada {{< /alternativa >}}
{{< solucao letra="B">}} Agregação usa losango vazio. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é o símbolo de composição em UML?
{{< alternativa >}} Losango vazio {{< /alternativa >}}
{{< alternativa >}} Losango preenchido {{< /alternativa >}}
{{< alternativa >}} Linha simples {{< /alternativa >}}
{{< alternativa >}} Linha pontilhada {{< /alternativa >}}
{{< solucao letra="B">}} Composição usa losango preenchido. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual relacionamento é mais adequado para “Livro e Página”?
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< alternativa >}} Associação {{< /alternativa >}}
{{< alternativa >}} Agregação {{< /alternativa >}}
{{< alternativa >}} Composição {{< /alternativa >}}
{{< solucao letra="D">}} Página depende do livro (composição). {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual relacionamento é mais adequado para “Professor e Disciplina”?
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< alternativa >}} Associação {{< /alternativa >}}
{{< alternativa >}} Agregação {{< /alternativa >}}
{{< alternativa >}} Composição {{< /alternativa >}}
{{< solucao letra="B">}} Relação estrutural sem dependência de vida. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual relacionamento é mais adequado para “Carrinho de compras e Produto”?
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< alternativa >}} Agregação {{< /alternativa >}}
{{< alternativa >}} Composição {{< /alternativa >}}
{{< alternativa >}} Herança {{< /alternativa >}}
{{< solucao letra="B">}} Produtos podem existir fora do carrinho. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual relacionamento indica ciclo de vida independente?
{{< alternativa >}} Composição {{< /alternativa >}}
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< alternativa >}} Agregação {{< /alternativa >}}
{{< alternativa >}} Herança {{< /alternativa >}}
{{< solucao letra="C">}} Agregação permite existência independente. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual relacionamento indica forte acoplamento?
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< alternativa >}} Agregação {{< /alternativa >}}
{{< alternativa >}} Composição {{< /alternativa >}}
{{< alternativa >}} Associação leve {{< /alternativa >}}
{{< solucao letra="C">}} Composição é o mais forte acoplamento estrutural. {{< /solucao >}}
{{< /questao >}}



{{< questao >}}
Qual relacionamento representa “usa em método”?
{{< code >}}
class A {
    void metodo(B b) { }
}
{{< /code >}}
{{< alternativa >}} Associação {{< /alternativa >}}
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< alternativa >}} Agregação {{< /alternativa >}}
{{< alternativa >}} Composição {{< /alternativa >}}
{{< solucao letra="B">}} Uso por parâmetro indica dependência. {{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual relacionamento melhor representa “Time e Jogador (profissional)”?
{{< alternativa >}} Dependência {{< /alternativa >}}
{{< alternativa >}} Agregação {{< /alternativa >}}
{{< alternativa >}} Composição {{< /alternativa >}}
{{< alternativa >}} Herança {{< /alternativa >}}
{{< solucao letra="B">}} Jogadores podem existir fora do time. {{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}


{{< /lista-questoes >}}

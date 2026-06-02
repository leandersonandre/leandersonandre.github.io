---
title: "Questões sobre Enumerações"
slug: "enums-questoes"
description: "Questões sobre Tipo Enum"
tags:
- enum
- questoes
---

{{< questao >}}
O que é uma enumeração (enum) em Java?

{{< alternativa >}} Uma variável especial que armazena números inteiros. {{< /alternativa >}}
{{< alternativa >}} Um tipo que define um conjunto fixo de constantes. {{< /alternativa >}}
{{< alternativa >}} Um método utilizado para criar objetos. {{< /alternativa >}}
{{< alternativa >}} Um atributo compartilhado entre classes. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores. {{< /alternativa >}}

{{< solucao letra="B" >}}
Uma enumeração define um conjunto limitado e fixo de valores constantes.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public enum Dia {
    SEGUNDA,
    TERCA,
    QUARTA
}
{{< /code >}}

Quantos valores a enumeração possui?

{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores. {{< /alternativa >}}

{{< solucao letra="C" >}}
A enumeração possui os valores SEGUNDA, TERCA e QUARTA.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public enum Cor {
    VERMELHO,
    VERDE,
    AZUL
}
{{< /code >}}

Qual das alternativas representa um valor válido da enumeração?

{{< alternativa >}} Cor {{< /alternativa >}}
{{< alternativa >}} AZUL {{< /alternativa >}}
{{< alternativa >}} String {{< /alternativa >}}
{{< alternativa >}} cor {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores. {{< /alternativa >}}

{{< solucao letra="B" >}}
AZUL é um dos valores definidos na enumeração.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public enum Status {
    ABERTO,
    FECHADO
}
{{< /code >}}

O que acontece se tentarmos utilizar o valor CANCELADO?

{{< alternativa >}} O programa funcionará normalmente. {{< /alternativa >}}
{{< alternativa >}} CANCELADO será criado automaticamente. {{< /alternativa >}}
{{< alternativa >}} Ocorrerá erro, pois o valor não existe na enumeração. {{< /alternativa >}}
{{< alternativa >}} CANCELADO será convertido para ABERTO. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores. {{< /alternativa >}}

{{< solucao letra="C" >}}
Somente os valores definidos na enumeração podem ser utilizados.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o estado atual da variável dia.

{{< code >}}
public enum Dia {
    SEGUNDA,
    TERCA
}

Dia dia = Dia.TERCA;
{{< /code >}}

{{< alternativa >}} Dia.SEGUNDA {{< /alternativa >}}
{{< alternativa >}} Dia.TERCA {{< /alternativa >}}
{{< alternativa >}} null {{< /alternativa >}}
{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="B" >}}
A variável recebeu explicitamente o valor Dia.TERCA.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o valor impresso.

{{< code >}}
public enum Status {
    ABERTO,
    FECHADO
}

public class Main {
    public static void main(String[] args) {
        Status s = Status.ABERTO;
        System.out.println(s);
    }
}
{{< /code >}}

{{< alternativa >}} Status {{< /alternativa >}}
{{< alternativa >}} ABERTO {{< /alternativa >}}
{{< alternativa >}} FECHADO {{< /alternativa >}}
{{< alternativa >}} null {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="B" >}}
O método println imprime o nome do valor da enumeração.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o valor impresso.

{{< code >}}
public enum Nivel {
    BAIXO,
    MEDIO,
    ALTO
}

public class Main {
    public static void main(String[] args) {
        Nivel n = Nivel.ALTO;
        System.out.println(n.ordinal());
    }
}
{{< /code >}}

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="C" >}}
Os índices começam em 0: BAIXO=0, MEDIO=1 e ALTO=2.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public enum Moeda {
    REAL,
    DOLAR,
    EURO
}
{{< /code >}}

Qual alternativa representa corretamente o tipo da variável?

{{< code >}}
Moeda m = Moeda.REAL;
{{< /code >}}

{{< alternativa >}} REAL {{< /alternativa >}}
{{< alternativa >}} String {{< /alternativa >}}
{{< alternativa >}} Moeda {{< /alternativa >}}
{{< alternativa >}} enum {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="C" >}}
A variável possui tipo Moeda.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise a UML abaixo.

{{< plantuml >}}
enum Status {
  ABERTO
  FECHADO
}
{{< /plantuml >}}

Qual alternativa está correta?

{{< alternativa >}} A enumeração possui um método chamado ABERTO. {{< /alternativa >}}
{{< alternativa >}} A enumeração possui dois valores. {{< /alternativa >}}
{{< alternativa >}} A enumeração possui dois atributos. {{< /alternativa >}}
{{< alternativa >}} A enumeração possui duas classes internas. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores. {{< /alternativa >}}

{{< solucao letra="B" >}}
ABERTO e FECHADO são valores da enumeração.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public enum Prioridade {
    BAIXA,
    MEDIA,
    ALTA
}
{{< /code >}}

Qual é a principal vantagem de utilizar enumerações?

{{< alternativa >}} Permitir qualquer valor possível. {{< /alternativa >}}
{{< alternativa >}} Garantir que apenas valores previamente definidos sejam utilizados. {{< /alternativa >}}
{{< alternativa >}} Tornar todos os atributos públicos. {{< /alternativa >}}
{{< alternativa >}} Eliminar a necessidade de classes. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores. {{< /alternativa >}}

{{< solucao letra="B" >}}
Enums restringem os valores possíveis a um conjunto conhecido.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo.

{{< code >}}
public enum Dia {
    SEGUNDA,
    TERCA,
    QUARTA
}
{{< /code >}}

Qual método retorna todos os valores da enumeração?

{{< alternativa >}} valueOf() {{< /alternativa >}}
{{< alternativa >}} values() {{< /alternativa >}}
{{< alternativa >}} getValues() {{< /alternativa >}}
{{< alternativa >}} listar() {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="B" >}}
O método estático <code>values()</code> retorna um vetor contendo todos os valores da enumeração.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o valor impresso.

{{< code >}}
public enum Cor {
    VERMELHO,
    VERDE,
    AZUL
}

public class Main {
    public static void main(String[] args) {
        System.out.println(Cor.values().length);
    }
}
{{< /code >}}

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="D" >}}
A enumeração possui três valores, portanto o tamanho retornado é 3.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o valor impresso.

{{< code >}}
public enum Status {
    ABERTO,
    FECHADO
}

public class Main {
    public static void main(String[] args) {
        Status s = Status.valueOf("FECHADO");
        System.out.println(s);
    }
}
{{< /code >}}

{{< alternativa >}} ABERTO {{< /alternativa >}}
{{< alternativa >}} FECHADO {{< /alternativa >}}
{{< alternativa >}} Status {{< /alternativa >}}
{{< alternativa >}} null {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="B" >}}
O método <code>valueOf()</code> retorna o valor da enumeração correspondente ao texto informado.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public enum Status {
    ABERTO,
    FECHADO
}
{{< /code >}}

O que acontece ao executar o código abaixo?

{{< code >}}
Status.valueOf("CANCELADO");
{{< /code >}}

{{< alternativa >}} Retorna null. {{< /alternativa >}}
{{< alternativa >}} Retorna ABERTO. {{< /alternativa >}}
{{< alternativa >}} Retorna FECHADO. {{< /alternativa >}}
{{< alternativa >}} Ocorre erro em tempo de execução. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores. {{< /alternativa >}}

{{< solucao letra="D" >}}
O texto informado não corresponde a nenhum valor da enumeração.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise a enumeração abaixo.

{{< code >}}
public enum Nivel {
    BAIXO,
    MEDIO,
    ALTO
}
{{< /code >}}

Qual valor possui ordinal igual a 1?

{{< alternativa >}} BAIXO {{< /alternativa >}}
{{< alternativa >}} MEDIO {{< /alternativa >}}
{{< alternativa >}} ALTO {{< /alternativa >}}
{{< alternativa >}} null {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="B" >}}
Os índices são: BAIXO=0, MEDIO=1 e ALTO=2.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
public enum Moeda {
    REAL("R$"),
    DOLAR("$");

    private String simbolo;

    Moeda(String simbolo){
        this.simbolo = simbolo;
    }

    public String getSimbolo(){
        return simbolo;
    }
}
{{< /code >}}

Qual é o tipo do atributo <code>simbolo</code>?

{{< alternativa >}} Moeda {{< /alternativa >}}
{{< alternativa >}} enum {{< /alternativa >}}
{{< alternativa >}} String {{< /alternativa >}}
{{< alternativa >}} Object {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="C" >}}
O atributo foi declarado como <code>private String simbolo</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o valor impresso.

{{< code >}}
public enum Moeda {
    REAL("R$"),
    DOLAR("$");

    private String simbolo;

    Moeda(String simbolo){
        this.simbolo = simbolo;
    }

    public String getSimbolo(){
        return simbolo;
    }
}

public class Main {
    public static void main(String[] args) {
        System.out.println(Moeda.REAL.getSimbolo());
    }
}
{{< /code >}}

{{< alternativa >}} REAL {{< /alternativa >}}
{{< alternativa >}} R$ {{< /alternativa >}}
{{< alternativa >}} $ {{< /alternativa >}}
{{< alternativa >}} simbolo {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="B" >}}
O valor associado ao elemento REAL é "R$".
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o valor impresso.

{{< code >}}
public enum Prioridade {
    BAIXA(1),
    ALTA(2);

    private int codigo;

    Prioridade(int codigo){
        this.codigo = codigo;
    }

    public int getCodigo(){
        return codigo;
    }
}

public class Main {
    public static void main(String[] args) {
        System.out.println(Prioridade.ALTA.getCodigo());
    }
}
{{< /code >}}

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} ALTA {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="C" >}}
O valor ALTA foi associado ao código 2.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise a UML abaixo.

{{< plantuml >}}
enum Moeda {
  REAL
  DOLAR
}
{{< /plantuml >}}

Qual código Java corresponde ao diagrama?

{{< alternativa >}}
{{< code >}}
public class Moeda {
    REAL,
    DOLAR
}
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
public enum Moeda {
    REAL,
    DOLAR
}
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
public interface Moeda {
    REAL,
    DOLAR
}
{{< /code >}}
{{< /alternativa >}}

{{< alternativa >}}
{{< code >}}
public record Moeda {
    REAL,
    DOLAR
}
{{< /code >}}
{{< /alternativa >}}

{{< solucao letra="B" >}}
O diagrama representa uma enumeração chamada Moeda.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise a UML abaixo.

{{< plantuml >}}
enum Prioridade {
  BAIXA
  ALTA
  +getCodigo(): int
}
{{< /plantuml >}}

Qual alternativa está correta?

{{< alternativa >}} A enumeração possui apenas valores. {{< /alternativa >}}
{{< alternativa >}} A enumeração possui um método chamado getCodigo. {{< /alternativa >}}
{{< alternativa >}} A enumeração possui um atributo chamado getCodigo. {{< /alternativa >}}
{{< alternativa >}} A enumeração não possui métodos. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="B" >}}
O diagrama mostra explicitamente um método público chamado <code>getCodigo()</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise a UML abaixo.

{{< plantuml >}}
enum Status {
  ABERTO
  FECHADO
  +isFinalizado(): boolean
}
{{< /plantuml >}}

Qual alternativa está correta?

{{< alternativa >}} O método retorna boolean. {{< /alternativa >}}
{{< alternativa >}} O método retorna String. {{< /alternativa >}}
{{< alternativa >}} O método retorna int. {{< /alternativa >}}
{{< alternativa >}} O método possui um parâmetro boolean. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="A" >}}
O tipo indicado após os dois pontos é <code>boolean</code>.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Qual das alternativas é uma vantagem do uso de enumerações em relação ao uso de Strings?

{{< alternativa >}} Permitem qualquer valor textual. {{< /alternativa >}}
{{< alternativa >}} Ocupam sempre menos memória. {{< /alternativa >}}
{{< alternativa >}} Reduzem erros causados por valores inválidos. {{< /alternativa >}}
{{< alternativa >}} Eliminam a necessidade de classes. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="C" >}}
A enumeração restringe os valores possíveis a um conjunto previamente definido.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Qual das alternativas é verdadeira sobre enumerações em Java?

{{< alternativa >}} Não podem possuir métodos. {{< /alternativa >}}
{{< alternativa >}} Não podem possuir atributos. {{< /alternativa >}}
{{< alternativa >}} Podem possuir atributos, construtores e métodos. {{< /alternativa >}}
{{< alternativa >}} São equivalentes a variáveis String. {{< /alternativa >}}
{{< alternativa >}} Nenhuma das anteriores {{< /alternativa >}}

{{< solucao letra="C" >}}
Enums em Java são tipos completos e podem conter atributos, construtores e métodos.
{{< /solucao >}}
{{< /questao >}}

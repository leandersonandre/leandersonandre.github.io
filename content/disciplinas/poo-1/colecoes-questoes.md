---
title: "Questões sobre coleções"
slug: "colecoes-questoes"
description: "Questões sobre coleções"
tags:
- questoes
- colecoes
---


{{< lista-questoes >}}

{{< questao >}}
Qual interface representa listas no framework Collections do Java?

{{< alternativa >}} Set {{< /alternativa >}}
{{< alternativa >}} Map {{< /alternativa >}}
{{< alternativa >}} List {{< /alternativa >}}
{{< alternativa >}} Queue {{< /alternativa >}}

{{< solucao letra="C" >}}
A interface <code>List</code> representa coleções ordenadas que permitem elementos repetidos.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Qual classe é uma implementação da interface List?

{{< alternativa >}} HashSet {{< /alternativa >}}
{{< alternativa >}} HashMap {{< /alternativa >}} 
{{< alternativa >}} ArrayList {{< /alternativa >}}
{{< alternativa >}} TreeMap {{< /alternativa >}}

{{< solucao letra="C" >}}
ArrayList é uma das implementações mais utilizadas da interface List.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Qual característica é verdadeira sobre listas?

{{< alternativa >}} Não permitem elementos repetidos. {{< /alternativa >}}
{{< alternativa >}} Permitem elementos repetidos e possuem ordem. {{< /alternativa >}}
{{< alternativa >}} Associam chaves e valores. {{< /alternativa >}}
{{< alternativa >}} Não possuem tamanho variável. {{< /alternativa >}}

{{< solucao letra="B" >}}
As listas mantêm a ordem dos elementos e permitem repetições.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
var lista = new ArrayList<Integer>();
lista.add(10);
lista.add(20);
lista.add(30);

System.out.println(lista.get(1));
{{< /code >}}

Qual valor será impresso?

{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 30 {{< /alternativa >}}
{{< alternativa >}} Erro de compilação {{< /alternativa >}}

{{< solucao letra="B" >}}
O elemento da posição 1 é o valor 20.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
var lista = new ArrayList<Integer>();
lista.add(1);
lista.add(2);
lista.add(3);

lista.add(1,99);
{{< /code >}}

Qual elemento ficará na posição 1?

{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 99 {{< /alternativa >}}

{{< solucao letra="D" >}}
O método <code>add(index,elemento)</code> insere o elemento na posição indicada.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
var lista = new ArrayList<Integer>();
lista.add(10);
lista.add(20);

System.out.println(lista.size());
{{< /code >}}

Qual valor será impresso?

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}

{{< solucao letra="C" >}}
O método <code>size()</code> retorna a quantidade de elementos da lista.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Qual interface representa conjuntos no framework Collections?

{{< alternativa >}} List {{< /alternativa >}}
{{< alternativa >}} Set {{< /alternativa >}}
{{< alternativa >}} Map {{< /alternativa >}}
{{< alternativa >}} CollectionMap {{< /alternativa >}}

{{< solucao letra="B" >}}
A interface Set representa conjuntos.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Qual característica é verdadeira sobre conjuntos?

{{< alternativa >}} Permitem elementos repetidos. {{< /alternativa >}}
{{< alternativa >}} Mantêm obrigatoriamente a ordem de inserção. {{< /alternativa >}}
{{< alternativa >}} Não permitem elementos repetidos. {{< /alternativa >}}
{{< alternativa >}} Associam chaves e valores. {{< /alternativa >}}

{{< solucao letra="C" >}}
Conjuntos não permitem elementos duplicados.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
var conjunto = new HashSet<Integer>();

conjunto.add(1);
conjunto.add(1);
conjunto.add(1);

System.out.println(conjunto.size());
{{< /code >}}

Qual valor será impresso?

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}

{{< solucao letra="B" >}}
O conjunto armazena apenas um elemento com valor 1.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
var conjunto = new HashSet<Integer>();
conjunto.add(10);

System.out.println(conjunto.contains(10));
{{< /code >}}

Qual valor será impresso?

{{< alternativa >}} true {{< /alternativa >}}
{{< alternativa >}} false {{< /alternativa >}}
{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} null {{< /alternativa >}}

{{< solucao letra="A" >}}
O elemento 10 existe no conjunto.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Qual interface representa mapas no framework Collections?

{{< alternativa >}} Set {{< /alternativa >}}
{{< alternativa >}} List {{< /alternativa >}}
{{< alternativa >}} Map {{< /alternativa >}}
{{< alternativa >}} Collection {{< /alternativa >}}

{{< solucao letra="C" >}}
A interface Map representa associações entre chaves e valores.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
var mapa = new HashMap<Integer,String>();

mapa.put(1,"Brasil");
mapa.put(2,"Argentina");

System.out.println(mapa.get(2));
{{< /code >}}

Qual valor será impresso?

{{< alternativa >}} Brasil {{< /alternativa >}}
{{< alternativa >}} Argentina {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} null {{< /alternativa >}}

{{< solucao letra="B" >}}
A chave 2 está associada ao valor "Argentina".
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
var mapa = new HashMap<Integer,String>();

mapa.put(1,"Brasil");
mapa.put(1,"Chile");

System.out.println(mapa.get(1));
{{< /code >}}

Qual valor será impresso?

{{< alternativa >}} Brasil {{< /alternativa >}}
{{< alternativa >}} Chile {{< /alternativa >}}
{{< alternativa >}} null {{< /alternativa >}}
{{< alternativa >}} Erro de compilação {{< /alternativa >}}

{{< solucao letra="B" >}}
Ao inserir uma chave já existente, o valor anterior é substituído.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
var mapa = new HashMap<Integer,String>();

mapa.put(1,"Brasil");

System.out.println(mapa.containsKey(1));
{{< /code >}}

Qual valor será impresso?

{{< alternativa >}} true {{< /alternativa >}}
{{< alternativa >}} false {{< /alternativa >}}
{{< alternativa >}} Brasil {{< /alternativa >}}
{{< alternativa >}} null {{< /alternativa >}}

{{< solucao letra="A" >}}
A chave 1 existe no mapa.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo.

{{< code >}}
var mapa = new HashMap<Integer,String>();

mapa.put(1,"Brasil");

System.out.println(mapa.containsValue("Argentina"));
{{< /code >}}

Qual valor será impresso?

{{< alternativa >}} true {{< /alternativa >}}
{{< alternativa >}} false {{< /alternativa >}}
{{< alternativa >}} Argentina {{< /alternativa >}}
{{< alternativa >}} null {{< /alternativa >}}

{{< solucao letra="B" >}}
O valor "Argentina" não está armazenado no mapa.
{{< /solucao >}}
{{< /questao >}}


{{< /lista-questoes >}}

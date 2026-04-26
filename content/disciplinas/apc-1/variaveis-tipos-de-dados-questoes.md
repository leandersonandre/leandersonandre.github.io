---
title: "Questões sobre Variáveis e tipos de dados"
slug: variaveis-tipos-de-dados-questoes
description: "Questões sobre Variáveis e tipos de dados em Python"
tags:
- python
- variável
- tipo de dados
- questões
---

{{< questao >}}
O que é uma variável em Python?

{{< alternativa >}} Um tipo de dado fixo {{< /alternativa >}}
{{< alternativa >}} Um espaço na memória para armazenar um valor {{< /alternativa >}}
{{< alternativa >}} Um comando de repetição {{< /alternativa >}}
{{< alternativa >}} Um operador matemático {{< /alternativa >}}
{{< solucao letra="B" >}}
Uma variável armazena um valor na memória.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual das opções representa corretamente a criação de uma variável?

{{< alternativa >}} int x = 10 {{< /alternativa >}}
{{< alternativa >}} x := 10 {{< /alternativa >}}
{{< alternativa >}} x = 10 {{< /alternativa >}}
{{< alternativa >}} var x = 10 {{< /alternativa >}}
{{< solucao letra="C" >}}
Em Python, utiliza-se x = 10 para atribuição.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será o tipo da variável?

{{< code >}}
x = 10
{{< /code >}}

{{< alternativa >}} float {{< /alternativa >}}
{{< alternativa >}} int {{< /alternativa >}}
{{< alternativa >}} str {{< /alternativa >}}
{{< alternativa >}} bool {{< /alternativa >}}
{{< solucao letra="B" >}}
10 é um número inteiro.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será o tipo da variável?

{{< code >}}
x = 3.14
{{< /code >}}

{{< alternativa >}} int {{< /alternativa >}}
{{< alternativa >}} float {{< /alternativa >}}
{{< alternativa >}} str {{< /alternativa >}}
{{< alternativa >}} bool {{< /alternativa >}}
{{< solucao letra="B" >}}
3.14 é um número decimal (float).
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será o tipo da variável?

{{< code >}}
x = "Python"
{{< /code >}}

{{< alternativa >}} int {{< /alternativa >}}
{{< alternativa >}} float {{< /alternativa >}}
{{< alternativa >}} str {{< /alternativa >}}
{{< alternativa >}} bool {{< /alternativa >}}
{{< solucao letra="C" >}}
Texto é do tipo string.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será o tipo da variável?

{{< code >}}
x = True
{{< /code >}}

{{< alternativa >}} int {{< /alternativa >}}
{{< alternativa >}} float {{< /alternativa >}}
{{< alternativa >}} str {{< /alternativa >}}
{{< alternativa >}} bool {{< /alternativa >}}
{{< solucao letra="D" >}}
True é um valor booleano.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual função retorna o tipo de uma variável?

{{< alternativa >}} type() {{< /alternativa >}}
{{< alternativa >}} typeof() {{< /alternativa >}}
{{< alternativa >}} class() {{< /alternativa >}}
{{< alternativa >}} var() {{< /alternativa >}}
{{< solucao letra="A" >}}
A função type() mostra o tipo da variável.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será a saída?

{{< code >}}
x = 10
print(type(x))

{{< /code >}}

{{< alternativa >}} int {{< /alternativa >}}
{{< alternativa >}} <class 'int'> {{< /alternativa >}}
{{< alternativa >}} number {{< /alternativa >}}
{{< alternativa >}} type int {{< /alternativa >}}
{{< solucao letra="B" >}}
O Python exibe o tipo como <class 'int'>.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será o tipo da variável?

{{< code >}}
x = "10"
y = 10

{{< /code >}}

{{< alternativa >}} x e y têm o mesmo tipo {{< /alternativa >}}
{{< alternativa >}} x é string e y é inteiro {{< /alternativa >}}
{{< alternativa >}} ambos são inteiros {{< /alternativa >}}
{{< alternativa >}} ambos são strings {{< /alternativa >}}
{{< solucao letra="B" >}}
x é string e y é inteiro.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será o resultado?

{{< code >}}
x = 5
y = 2
print(x / y)

{{< /code >}}

{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 2.5 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
A divisão retorna float.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será o resultado?

{{< code >}}
x = 5
y = 2
print(x // y)
{{< /code >}}

{{< alternativa >}} 2.5 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
// retorna divisão inteira.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual conversão transforma string em inteiro?

{{< alternativa >}} str() {{< /alternativa >}}
{{< alternativa >}} int() {{< /alternativa >}}
{{< alternativa >}} float() {{< /alternativa >}}
{{< alternativa >}} bool() {{< /alternativa >}}
{{< solucao letra="B" >}}
int() converte para inteiro.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será o resultado?

{{< code >}}
x = int("5")
print(x + 2)

{{< /code >}}

{{< alternativa >}} 52 {{< /alternativa >}}
{{< alternativa >}} 7 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
A string foi convertida para inteiro.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será o tipo da variável?

{{< code >}}
x = float(3)
{{< /code >}}

{{< alternativa >}} x será inteiro {{< /alternativa >}}
{{< alternativa >}} x será float {{< /alternativa >}}
{{< alternativa >}} x será string {{< /alternativa >}}
{{< alternativa >}} erro {{< /alternativa >}}
{{< solucao letra="B" >}}
float(3) converte para 3.0.
{{< /solucao >}}
{{< /questao >}}

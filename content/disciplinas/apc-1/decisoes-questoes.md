---
title: "Questões sobre Decisões"
description: "Questões sobre Estrutura de decisões em Python"
slug: decisoes-questoes
tags:
- python
- repetições
- questões
---

{{< lista-questoes >}}

{{< questao >}}
O que é uma estrutura de decisão em Python?
{{< alternativa >}} Uma estrutura usada para repetir blocos de código. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que permite executar diferentes caminhos com base em condições. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que armazena dados em memória. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura usada apenas para entrada de dados. {{< /alternativa >}}
{{< solucao letra="B" >}}
Uma estrutura que permite escolher diferentes caminhos de execução com base em condições.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a função da cláusula <b>else</b> em uma estrutura condicional?

{{< alternativa >}} Executar um bloco de código sempre que a condição for verdadeira {{< /alternativa >}}
{{< alternativa >}} Executar um bloco de código quando nenhuma das condições anteriores for verdadeira {{< /alternativa >}}
{{< alternativa >}} Repetir uma condição até que seja falsa {{< /alternativa >}}
{{< alternativa >}} Encerrar a execução do programa {{< /alternativa >}}
{{< solucao letra="B" >}}
O else é executado quando todas as condições anteriores (if e elif) são falsas.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é o papel da cláusula <b>elif</b> em uma estrutura condicional?

{{< alternativa >}} Substituir o if principal {{< /alternativa >}}
{{< alternativa >}} Criar uma repetição condicional {{< /alternativa >}}
{{< alternativa >}} Testar uma nova condição caso a anterior seja falsa {{< /alternativa >}}
{{< alternativa >}} Finalizar o bloco condicional {{< /alternativa >}}
{{< solucao letra="C" >}}
O elif permite testar novas condições quando a condição do if (ou de elif anteriores) não é satisfeita.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Sobre o uso de <b>if, elif e else</b>, qual alternativa está correta?

{{< alternativa >}} É obrigatório utilizar else em toda estrutura condicional {{< /alternativa >}}
{{< alternativa >}} Pode haver múltiplos elif, mas apenas um else {{< /alternativa >}}
{{< alternativa >}} Só é permitido um elif por estrutura {{< /alternativa >}}
{{< alternativa >}} O else deve sempre vir antes do elif {{< /alternativa >}}
{{< solucao letra="B" >}}
Podemos ter vários elif, mas apenas um else, que deve ser o último bloco da estrutura.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Em uma estrutura condicional, quando o bloco <b>else</b> é executado?

{{< alternativa >}} Sempre que o programa inicia {{< /alternativa >}}
{{< alternativa >}} Quando a primeira condição (if) for verdadeira {{< /alternativa >}}
{{< alternativa >}} Quando todas as condições anteriores forem falsas {{< /alternativa >}}
{{< alternativa >}} Apenas quando existe um elif {{< /alternativa >}}
{{< solucao letra="C" >}}
O else é executado somente quando nenhuma das condições anteriores é satisfeita.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
x = 10
if x > 5:
  print("A")
else:
  print("B")
{{< /code >}}

{{< alternativa >}} A {{< /alternativa >}}
{{< alternativa >}} B {{< /alternativa >}}
{{< alternativa >}} A B {{< /alternativa >}}
{{< alternativa >}} Nada será impresso {{< /alternativa >}}
{{< solucao letra="A" >}}
Como x é maior que 5, o bloco do if será executado.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
x = 3
if x > 5:
  print("A")
elif x > 2:
  print("B")
else:
  print("C")
{{< /code >}}

{{< alternativa >}} A {{< /alternativa >}}
{{< alternativa >}} B {{< /alternativa >}}
{{< alternativa >}} C {{< /alternativa >}}
{{< alternativa >}} Nada {{< /alternativa >}}
{{< solucao letra="B" >}}
A primeira condição é falsa, mas a segunda é verdadeira, então imprime B.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
x = 7
if x < 5:
  print("A")
elif x < 7:
  print("B")
else:
  print("C")
{{< /code >}}

{{< alternativa >}} A {{< /alternativa >}}
{{< alternativa >}} B {{< /alternativa >}}
{{< alternativa >}} C {{< /alternativa >}}
{{< alternativa >}} Nada {{< /alternativa >}}
{{< solucao letra="C" >}}
Nenhuma das condições anteriores é verdadeira, então executa o else.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
x = 4
if x > 2:
  if x < 5:
    print("A")
  else:
    print("B")
else:
  print("C")
{{< /code >}}

{{< alternativa >}} A {{< /alternativa >}}
{{< alternativa >}} B {{< /alternativa >}}
{{< alternativa >}} C {{< /alternativa >}}
{{< alternativa >}} Nada {{< /alternativa >}}
{{< solucao letra="A" >}}
x é maior que 2 e menor que 5, então imprime A.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
x = 5
if x == 5:
  print("A")
if x > 3:
  print("B")
{{< /code >}}

{{< alternativa >}} A {{< /alternativa >}}
{{< alternativa >}} B {{< /alternativa >}}
{{< alternativa >}} A B {{< /alternativa >}}
{{< alternativa >}} Nada será impresso.{{< /alternativa >}}
{{< solucao letra="C" >}}
As duas condições são verdadeiras, então ambos os prints são executados.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
x = 3
if x == 5:
  print("A")
if x > 3:
  print("B")
{{< /code >}}

{{< alternativa >}} A {{< /alternativa >}}
{{< alternativa >}} B {{< /alternativa >}}
{{< alternativa >}} A B {{< /alternativa >}}
{{< alternativa >}} Nada será impresso.{{< /alternativa >}}
{{< solucao letra="D" >}}
As duas condições são falsa, então ambos os prints não são executados.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique em qual linha há um erro.

{{< code >}}
1 | x = 10
2 | if x > 5
3 |   print("Maior que 5")
{{< /code >}}

{{< alternativa >}} Linha 1 {{< /alternativa >}}
{{< alternativa >}} Linha 2 {{< /alternativa >}}
{{< alternativa >}} Linha 3 {{< /alternativa >}}
{{< alternativa >}} Não há erro {{< /alternativa >}}
{{< solucao letra="B" >}}
Falta os dois pontos ":" ao final da condição do if na linha 2.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique em qual linha há um erro.

{{< code >}}
1 | x = 3
2 | if x > 5:
3 | print("A")
4 | else:
5 |   print("B")
{{< /code >}}

{{< alternativa >}} Linha 2 {{< /alternativa >}}
{{< alternativa >}} Linha 3 {{< /alternativa >}}
{{< alternativa >}} Linha 4 {{< /alternativa >}}
{{< alternativa >}} Linha 5 {{< /alternativa >}}
{{< solucao letra="B" >}}
A linha 3 deveria estar indentada, pois faz parte do bloco do if.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique em qual linha há um erro.

{{< code >}}
1 | x = 7
2 | if x > 5:
3 |   print("A")
4 | elif x < 10
5 |   print("B")
{{< /code >}}

{{< alternativa >}} Linha 2 {{< /alternativa >}}
{{< alternativa >}} Linha 3 {{< /alternativa >}}
{{< alternativa >}} Linha 4 {{< /alternativa >}}
{{< alternativa >}} Linha 5 {{< /alternativa >}}
{{< solucao letra="C" >}}
Falta os dois pontos ":" ao final da condição do elif na linha 4.
{{< /solucao >}}
{{< /questao >}}


{{< /lista-questoes >}}

---
title: "Questões sobre Entrada e Saída de dados"
slug: entrada-saida-de-dados-questoes
description: "Questões sobre Entrada e saída de dados em Python"
tags:
- python
- print
- input
- questões
---

{{< questao >}}
Qual função é utilizada para ler dados do usuário em Python?

{{< alternativa >}} read() {{< /alternativa >}}
{{< alternativa >}} input() {{< /alternativa >}}
{{< alternativa >}} scan() {{< /alternativa >}}
{{< alternativa >}} get() {{< /alternativa >}}
{{< solucao letra="B" >}}
A função input() é usada para ler dados digitados pelo usuário.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será o tipo do valor retornado por input()?

{{< alternativa >}} int {{< /alternativa >}}
{{< alternativa >}} float {{< /alternativa >}}
{{< alternativa >}} str {{< /alternativa >}}
{{< alternativa >}} bool {{< /alternativa >}}
{{< solucao letra="C" >}}
O input() sempre retorna uma string.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será a saída do código?

{{< code >}}
nome = input("Digite seu nome: ")
print(nome)

{{< /code >}}

{{< alternativa >}} Sempre imprime "nome" {{< /alternativa >}}
{{< alternativa >}} Imprime o texto digitado pelo usuário {{< /alternativa >}}
{{< alternativa >}} Dá erro {{< /alternativa >}}
{{< alternativa >}} Não imprime nada {{< /alternativa >}}
{{< solucao letra="B" >}}
O valor digitado pelo usuário será exibido.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Como converter um valor lido com input() para inteiro?

{{< alternativa >}} int(input()) {{< /alternativa >}}
{{< alternativa >}} input(int) {{< /alternativa >}}
{{< alternativa >}} str(input()) {{< /alternativa >}}
{{< alternativa >}} float(input()) {{< /alternativa >}}
{{< solucao letra="A" >}}
Utiliza-se int(input()) para converter para inteiro.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Como converter um valor lido com input() para decimal?

{{< alternativa >}} int(input()) {{< /alternativa >}}
{{< alternativa >}} input(int) {{< /alternativa >}}
{{< alternativa >}} str(input()) {{< /alternativa >}}
{{< alternativa >}} float(input()) {{< /alternativa >}}
{{< solucao letra="A" >}}
Utiliza-se float(input()) para converter para decimal.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será a saída?

{{< code >}}
print("A", "B", "C")

{{< /code >}}

{{< alternativa >}} ABC {{< /alternativa >}}
{{< alternativa >}} A B C {{< /alternativa >}}
{{< alternativa >}} A,B,C {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
Os valores são separados por espaço por padrão.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual parâmetro do print() controla o separador entre valores?

{{< alternativa >}} end {{< /alternativa >}}
{{< alternativa >}} sep {{< /alternativa >}}
{{< alternativa >}} join {{< /alternativa >}}
{{< alternativa >}} space {{< /alternativa >}}
{{< solucao letra="B" >}}
O parâmetro sep define o separador entre os elementos.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será a saída?

{{< code >}}
print("A", "B", sep="-")

{{< /code >}}

{{< alternativa >}} A B {{< /alternativa >}}
{{< alternativa >}} A-B {{< /alternativa >}}
{{< alternativa >}} AB {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
O separador foi definido como "-".
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual parâmetro do print() controla o que acontece ao final da impressão?

{{< alternativa >}} sep {{< /alternativa >}}
{{< alternativa >}} end {{< /alternativa >}}
{{< alternativa >}} stop {{< /alternativa >}}
{{< alternativa >}} break {{< /alternativa >}}
{{< solucao letra="B" >}}
O parâmetro end define o final da linha.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será a saída?

{{< code >}}
print("A", end="")
print("B")

{{< /code >}}

{{< alternativa >}} A B {{< /alternativa >}}
{{< alternativa >}} AB {{< /alternativa >}}
{{< alternativa >}} A\nB {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
O end="" remove a quebra de linha.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual sequência representa quebra de linha?

{{< alternativa >}} \t {{< /alternativa >}}
{{< alternativa >}} \n {{< /alternativa >}}
{{< alternativa >}} \r {{< /alternativa >}}
{{< alternativa >}} \b {{< /alternativa >}}
{{< solucao letra="B" >}}
\n representa quebra de linha.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual sequência representa tabulação?

{{< alternativa >}} \n {{< /alternativa >}}
{{< alternativa >}} \t {{< /alternativa >}}
{{< alternativa >}} \s {{< /alternativa >}}
{{< alternativa >}} \b {{< /alternativa >}}
{{< solucao letra="B" >}}
\t representa tabulação.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será a saída?

{{< code >}}
print("A\nB")

{{< /code >}}

{{< alternativa >}} A B {{< /alternativa >}}
{{< alternativa >}} AB {{< /alternativa >}}
{{< alternativa >}} A na linha 1 e B na linha 2 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="C" >}}
\n quebra a linha.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será a saída?

{{< code >}}
print("A\tB")

{{< /code >}}

{{< alternativa >}} A B {{< /alternativa >}}
{{< alternativa >}} A\tB {{< /alternativa >}}
{{< alternativa >}} A    B {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="C" >}}
\t cria um espaço de tabulação.
{{< /solucao >}}
{{< /questao >}}

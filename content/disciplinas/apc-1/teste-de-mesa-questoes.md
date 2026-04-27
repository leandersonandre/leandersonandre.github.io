---
title: "Questões sobre Teste de Mesa"
description: "Questões sobre Teste de Mesa"
slug: teste-de-mesa-questoes
tags:
- python
- teste-de-mesa
- variáveis
- simulação
- questões
---

{{< lista-questoes >}}

{{< questao >}}
Analise o código abaixo e identifique o valor final de x.

{{< code >}}
x = 1

for i in range(3):
    x = x + i
{{< /code >}}

{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}} 
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 6 {{< /alternativa >}}

{{< solucao letra="B" >}}

<table border="1">
<tr><th>Passo</th><th>Instrução</th><th>i</th><th>x</th></tr>
<tr><td>1</td><td>x = 1</td><td>-</td><td>1</td></tr>
<tr><td>2</td><td>i = 0 → x = x + i</td><td>0</td><td>1</td></tr>
<tr><td>3</td><td>i = 1 → x = x + i</td><td>1</td><td>2</td></tr>
<tr><td>4</td><td>i = 2 → x = x + i</td><td>2</td><td>4</td></tr>
</table>

Resposta: x = 4

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Simule o código abaixo e identifique a saída.

{{< code >}}
for i in range(1, 4):
    print(i * 2)
{{< /code >}}

{{< alternativa >}} 1 2 3 {{< /alternativa >}}
{{< alternativa >}} 2 4 6 {{< /alternativa >}}
{{< alternativa >}} 2 3 4 {{< /alternativa >}}
{{< alternativa >}} 0 2 4 {{< /alternativa >}}

{{< solucao letra="B" >}}

<table border="1">
<tr><th>Passo</th><th>i</th><th>Saída</th></tr>
<tr><td>1</td><td>1</td><td>2</td></tr>
<tr><td>2</td><td>2</td><td>4</td></tr>
<tr><td>3</td><td>3</td><td>6</td></tr>
</table>

Saída final: 2 4 6

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o valor final de soma.

{{< code >}}
soma = 0

for i in range(2, 5):
    soma += i
{{< /code >}}

{{< alternativa >}} 6 {{< /alternativa >}}
{{< alternativa >}} 7 {{< /alternativa >}}
{{< alternativa >}} 9 {{< /alternativa >}}
{{< alternativa >}} 12 {{< /alternativa >}}

{{< solucao letra="C" >}}

<table border="1">
<tr><th>Passo</th><th>i</th><th>soma</th></tr>
<tr><td>1</td><td>2</td><td>2</td></tr>
<tr><td>2</td><td>3</td><td>5</td></tr>
<tr><td>3</td><td>4</td><td>9</td></tr>
</table>

Resposta: soma = 9

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Simule o código abaixo e identifique a saída.

{{< code >}}
i = 0

while i < 3:
    print(i)
    i += 1
{{< /code >}}

{{< alternativa >}} 1 2 3 {{< /alternativa >}}
{{< alternativa >}} 0 1 2 {{< /alternativa >}}
{{< alternativa >}} 0 1 2 3 {{< /alternativa >}}
{{< alternativa >}} Loop infinito {{< /alternativa >}}

{{< solucao letra="B" >}}

<table border="1">
<tr><th>Passo</th><th>Condição</th><th>i</th><th>Saída</th></tr>
<tr><td>1</td><td>0 &lt; 3 (true)</td><td>0</td><td>0</td></tr>
<tr><td>2</td><td>1 &lt; 3 (true)</td><td>1</td><td>1</td></tr>
<tr><td>3</td><td>2 &lt; 3 (true)</td><td>2</td><td>2</td></tr>
<tr><td>4</td><td>3 &lt; 3 (false)</td><td>3</td><td>-</td></tr>
</table>

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique o valor final de x.

{{< code >}}
x = 0

for i in range(3):
    x += 2
{{< /code >}}

{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< alternativa >}} 6 {{< /alternativa >}}
{{< alternativa >}} 8 {{< /alternativa >}}

{{< solucao letra="C" >}}

<table border="1">
<tr><th>Passo</th><th>i</th><th>x</th></tr>
<tr><td>1</td><td>0</td><td>2</td></tr>
<tr><td>2</td><td>1</td><td>4</td></tr>
<tr><td>3</td><td>2</td><td>6</td></tr>
</table>

Resposta: x = 6

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo e identifique a saída.

{{< code >}}
for i in range(3):
    if i == 1:
        continue
    print(i)
{{< /code >}}

{{< alternativa >}} 0 1 2 {{< /alternativa >}}
{{< alternativa >}} 1 2 {{< /alternativa >}}
{{< alternativa >}} 0 2 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}

{{< solucao letra="C" >}}

<table border="1">
<tr><th>Passo</th><th>i</th><th>Ação</th><th>Saída</th></tr>
<tr><td>1</td><td>0</td><td>print</td><td>0</td></tr>
<tr><td>2</td><td>1</td><td>continue</td><td>-</td></tr>
<tr><td>3</td><td>2</td><td>print</td><td>2</td></tr>
</table>

Saída final: 0 2

{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

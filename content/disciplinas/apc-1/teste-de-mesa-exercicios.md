---
title: "Exercícios sobre Teste de Mesa"
description: "Exercícios para simular execução de algoritmos"
slug: teste-de-mesa-exercicios
tags:
- python
- lógica
- teste-de-mesa
- questões
---

{{< lista-questoes >}}

{{< questao >}}
Dado o código abaixo, faça o teste de mesa e informe os valores finais de x, y e z.

{{< code >}}
x = 5
y = 3
z = x + y
x = z - 2
y = x + z
{{< /code >}}

{{< solucao letra=" " >}}

<table border="1">
  <tr>
    <th>Passo</th>
    <th>Instrução</th>
    <th>x</th>
    <th>y</th>
    <th>z</th>
  </tr>
  <tr>
    <td>1</td>
    <td>x = 5</td>
    <td>5</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>2</td>
    <td>y = 3</td>
    <td>5</td>
    <td>3</td>
    <td>-</td>
  </tr>
  <tr>
    <td>3</td>
    <td>z = x + y</td>
    <td>5</td>
    <td>3</td>
    <td>8</td>
  </tr>
  <tr>
    <td>4</td>
    <td>x = z - 2</td>
    <td>6</td>
    <td>3</td>
    <td>8</td>
  </tr>
  <tr>
    <td>5</td>
    <td>y = x + z</td>
    <td>6</td>
    <td>14</td>
    <td>8</td>
  </tr>
</table>

Resposta final:  
x = 6, y = 14, z = 8

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Simule a execução do código e informe o valor impresso.

{{< code >}}
a = 10
b = 2
c = a * b
c = c - a
print(c)
{{< /code >}}

{{< solucao letra=" " >}}

<table border="1">
  <tr>
    <th>Passo</th>
    <th>Instrução</th>
    <th>a</th>
    <th>b</th>
    <th>c</th>
    <th>Saída</th>
  </tr>
  <tr>
    <td>1</td>
    <td>a = 10</td>
    <td>10</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>2</td>
    <td>b = 2</td>
    <td>10</td>
    <td>2</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>3</td>
    <td>c = a * b</td>
    <td>10</td>
    <td>2</td>
    <td>20</td>
    <td>-</td>
  </tr>
  <tr>
    <td>4</td>
    <td>c = c - a</td>
    <td>10</td>
    <td>2</td>
    <td>10</td>
    <td>-</td>
  </tr>
  <tr>
    <td>5</td>
    <td>print(c)</td>
    <td>10</td>
    <td>2</td>
    <td>10</td>
    <td>10</td>
  </tr>
</table>

Resposta final: 10

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Dado o código abaixo, qual será a saída?

{{< code >}}
x = 4
y = 6

if x > y:
    print(x)
else:
    print(y)
{{< /code >}}

{{< solucao letra=" " >}}

<table border="1">
  <tr>
    <th>Passo</th>
    <th>Instrução</th>
    <th>x</th>
    <th>y</th>
    <th>Saída</th>
  </tr>
  <tr>
    <td>1</td>
    <td>x = 4</td>
    <td>4</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>2</td>
    <td>y = 6</td>
    <td>4</td>
    <td>6</td>
    <td>-</td>
  </tr>
  <tr>
    <td>3</td>
    <td>x &gt; y → false</td>
    <td>4</td>
    <td>6</td>
    <td>-</td>
  </tr>
  <tr>
    <td>4</td>
    <td>else → print(y)</td>
    <td>4</td>
    <td>6</td>
    <td>6</td>
  </tr>
</table>

Resposta final: 6

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Faça o teste de mesa do código abaixo e informe a saída.

{{< code >}}
x = 7

if x % 2 == 0:
    print("Par")
else:
    print("Ímpar")
{{< /code >}}

{{< solucao letra=" " >}}

<table border="1">
  <tr>
    <th>Passo</th>
    <th>Instrução</th>
    <th>x</th>
    <th>Saída</th>
  </tr>
  <tr>
    <td>1</td>
    <td>x = 7</td>
    <td>7</td>
    <td>-</td>
  </tr>
  <tr>
    <td>2</td>
    <td>x % 2 == 0 → false</td>
    <td>7</td>
    <td>-</td>
  </tr>
  <tr>
    <td>3</td>
    <td>else → print("Ímpar")</td>
    <td>7</td>
    <td>Ímpar</td>
  </tr>
</table>

Resposta final: Ímpar

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Simule a execução do código e informe o valor final de soma.

{{< code >}}
soma = 0

for i in range(1, 4):
    soma += i
{{< /code >}}

{{< solucao letra=" " >}}

<table border="1">
  <tr>
    <th>Passo</th>
    <th>Instrução</th>
    <th>i</th>
    <th>soma</th>
  </tr>
  <tr>
    <td>1</td>
    <td>soma = 0</td>
    <td>-</td>
    <td>0</td>
  </tr>
  <tr>
    <td>2</td>
    <td>i = 1</td>
    <td>1</td>
    <td>0</td>
  </tr>
  <tr>
    <td>3</td>
    <td>soma += i</td>
    <td>1</td>
    <td>1</td>
  </tr>
  <tr>
    <td>4</td>
    <td>i = 2</td>
    <td>2</td>
    <td>1</td>
  </tr>
  <tr>
    <td>5</td>
    <td>soma += i</td>
    <td>2</td>
    <td>3</td>
  </tr>
  <tr>
    <td>6</td>
    <td>i = 3</td>
    <td>3</td>
    <td>3</td>
  </tr>
  <tr>
    <td>7</td>
    <td>soma += i</td>
    <td>3</td>
    <td>6</td>
  </tr>
  <tr>
    <td>8</td>
    <td>fim do for</td>
    <td>-</td>
    <td>6</td>
  </tr>
</table>

Resposta final: soma = 6

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Dado o código abaixo, informe a saída.

{{< code >}}
for i in range(3):
    print(i)
{{< /code >}}

{{< solucao letra=" " >}}

<table border="1">
  <tr>
    <th>Passo</th>
    <th>Instrução</th>
    <th>Saída</th>
    <th>i</th>
  </tr>
  <tr>
    <td>1</td>
    <td>Início do for</td>
    <td>-</td>
    <td>-</td>
  </tr>
  <tr>
    <td>2</td>
    <td>i = 0</td>
    <td>-</td>
    <td>0</td>
  </tr>
  <tr>
    <td>3</td>
    <td>print(i)</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
    <td>4</td>
    <td>i = 1</td>
    <td>-</td>
    <td>1</td>
  </tr>
  <tr>
    <td>5</td>
    <td>print(i)</td>
    <td>1</td>
    <td>1</td>
  </tr>
  <tr>
    <td>6</td>
    <td>i = 2</td>
    <td>-</td>
    <td>2</td>
  </tr>
  <tr>
    <td>7</td>
    <td>print(i)</td>
    <td>2</td>
    <td>2</td>
  </tr>
  <tr>
    <td>8</td>
    <td>fim do for</td>
    <td>-</td>
    <td>-</td>
  </tr>
</table>

Resposta final: 
<br>
0  
<br>
1  
<br>
2

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Faça o teste de mesa e informe o valor final de x.

{{< code >}}
x = 1

for i in range(4):
    x = x * 2
{{< /code >}}

{{< solucao letra=" " >}}

<table border="1">
  <tr>
    <th>Passo</th>
    <th>Instrução</th>
    <th>i</th>
    <th>x</th>
  </tr>
  <tr>
    <td>1</td>
    <td>Inicialização</td>
    <td>-</td>
    <td>1</td>
  </tr>
  <tr>
    <td>2</td>
    <td>for i = 0</td>
    <td>0</td>
    <td>1</td>
  </tr>
  <tr>
    <td>3</td>
    <td>x = x * 2</td>
    <td>0</td>
    <td>2</td>
  </tr>
  <tr>
    <td>4</td>
    <td>for i = 1</td>
    <td>1</td>
    <td>2</td>
  </tr>
  <tr>
    <td>5</td>
    <td>x = x * 2</td>
    <td>1</td>
    <td>4</td>
  </tr>
  <tr>
    <td>6</td>
    <td>for i = 2</td>
    <td>2</td>
    <td>4</td>
  </tr>
  <tr>
    <td>7</td>
    <td>x = x * 2</td>
    <td>2</td>
    <td>8</td>
  </tr>
  <tr>
    <td>8</td>
    <td>for i = 3</td>
    <td>3</td>
    <td>8</td>
  </tr>
  <tr>
    <td>9</td>
    <td>x = x * 2</td>
    <td>3</td>
    <td>16</td>
  </tr>
  <tr>
    <td>10</td>
    <td>fim do for</td>
    <td>-</td>
    <td>16</td>
  </tr>
</table>

Resposta final: x = 16

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Simule o código abaixo e informe a saída.

{{< code >}}
x = 0

while x < 3:
    print(x)
    x += 1
{{< /code >}}

{{< solucao letra=" " >}}

<table border="1">
  <tr>
    <th>Passo</th>
    <th>Instrução</th>
    <th>Saída</th>
    <th>x</th>
  </tr>
  <tr>
    <td>1</td>
    <td>x = 0</td>
    <td>-</td>
    <td>0</td>
  </tr>
  <tr>
    <td>2</td>
    <td>while (0 &lt; 3) → true</td>
    <td>-</td>
    <td>0</td>
  </tr>
  <tr>
    <td>3</td>
    <td>print(x)</td>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
    <td>4</td>
    <td>x += 1</td>
    <td>-</td>
    <td>1</td>
  </tr>
  <tr>
    <td>5</td>
    <td>while (1 &lt; 3) → true</td>
    <td>-</td>
    <td>1</td>
  </tr>
  <tr>
    <td>6</td>
    <td>print(x)</td>
    <td>1</td>
    <td>1</td>
  </tr>
  <tr>
    <td>7</td>
    <td>x += 1</td>
    <td>-</td>
    <td>2</td>
  </tr>
  <tr>
    <td>8</td>
    <td>while (2 &lt; 3) → true</td>
    <td>-</td>
    <td>2</td>
  </tr>
  <tr>
    <td>9</td>
    <td>print(x)</td>
    <td>2</td>
    <td>2</td>
  </tr>
  <tr>
    <td>10</td>
    <td>x += 1</td>
    <td>-</td>
    <td>3</td>
  </tr>
  <tr>
    <td>11</td>
    <td>while (3 &lt; 3) → false</td>
    <td>-</td>
    <td>3</td>
  </tr>
</table>

Resposta final:  
<br>
0  
<br>
1  
<br>
2

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Dado o código abaixo, qual será o valor final de y?

{{< code >}}
x = 2
y = 5

while x < 5:
    y += x
    x += 1
{{< /code >}}

{{< solucao letra=" " >}}

<table border="1">
  <tr>
    <th>Passo</th>
    <th>Instrução</th>
    <th>Saída</th>
    <th>x</th>
    <th>y</th>
  </tr>
  <tr>
    <td>1</td>
    <td>Inicialização</td>
    <td>-</td>
    <td>2</td>
    <td>5</td>
  </tr>
  <tr>
    <td>2</td>
    <td>while (2 &lt; 5) → true</td>
    <td>-</td>
    <td>2</td>
    <td>5</td>
  </tr>
  <tr>
    <td>3</td>
    <td>y += x</td>
    <td>-</td>
    <td>2</td>
    <td>7</td>
  </tr>
  <tr>
    <td>4</td>
    <td>x += 1</td>
    <td>-</td>
    <td>3</td>
    <td>7</td>
  </tr>
  <tr>
    <td>5</td>
    <td>while (3 &lt; 5) → true</td>
    <td>-</td>
    <td>3</td>
    <td>7</td>
  </tr>
  <tr>
    <td>6</td>
    <td>y += x</td>
    <td>-</td>
    <td>3</td>
    <td>10</td>
  </tr>
  <tr>
    <td>7</td>
    <td>x += 1</td>
    <td>-</td>
    <td>4</td>
    <td>10</td>
  </tr>
  <tr>
    <td>8</td>
    <td>while (4 &lt; 5) → true</td>
    <td>-</td>
    <td>4</td>
    <td>10</td>
  </tr>
  <tr>
    <td>9</td>
    <td>y += x</td>
    <td>-</td>
    <td>4</td>
    <td>14</td>
  </tr>
  <tr>
    <td>10</td>
    <td>x += 1</td>
    <td>-</td>
    <td>5</td>
    <td>14</td>
  </tr>
  <tr>
    <td>11</td>
    <td>while (5 &lt; 5) → false</td>
    <td>-</td>
    <td>5</td>
    <td>14</td>
  </tr>
</table>

Resposta final: y = 14

{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Simule a execução e informe a saída.

{{< code >}}
a = 3
b = 4

if a > 2 and b < 5:
    print("A")
else:
    print("B")
{{< /code >}}

{{< solucao letra=" " >}}

<table border="1">
  <tr>
    <th>Passo</th>
    <th>Instrução</th>
    <th>Saída</th>
    <th>a</th>
    <th>b</th>
  </tr>
  <tr>
    <td>1</td>
    <td>Inicialização</td>
    <td>-</td>
    <td>3</td>
    <td>4</td>
  </tr>
  <tr>
    <td>2</td>
    <td>a &gt; 2 → true</td>
    <td>-</td>
    <td>3</td>
    <td>4</td>
  </tr>
  <tr>
    <td>3</td>
    <td>b &lt; 5 → true</td>
    <td>-</td>
    <td>3</td>
    <td>4</td>
  </tr>
  <tr>
    <td>4</td>
    <td>true and true → true</td>
    <td>-</td>
    <td>3</td>
    <td>4</td>
  </tr>
  <tr>
    <td>5</td>
    <td>print("A")</td>
    <td>A</td>
    <td>3</td>
    <td>4</td>
  </tr>
</table>

Resposta final: A

{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

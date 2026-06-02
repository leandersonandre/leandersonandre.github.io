---
title: "Exercícios sobre Enumerações"
slug: "enums-exercicios"
description: "Exercícios sobre Tipo Enum"
tags:
- enum
- exercicios
---

{{< lista-questoes >}}

{{< questao >}}
Crie uma classe <code>Semaforo</code> para representar um semáforo de trânsito. As fases do semáforo (<code>VERMELHO</code>,  <code>AMARELO</code> e <code>VERDE</code>) devem ser representadas por uma enumeração. 
<br>
A classe deve armazenar a fase atual e possuir um método <code>trocarFase()</code> que avance para a próxima fase da sequência:
<br>
<br>
VERMELHO → VERDE → AMARELO → VERMELHO.
{{< /questao >}}

{{< questao >}}
Crie uma classe `Dinheiro` para representar um valor monetário. Os tipos de moeda (<code>REAL</code>, <code>DOLAR</code> e <code>EURO</code>) devem ser representadas por uma enumeração.
<br>
A classe deve armazenar o tipo da moeda e o valor monetário. Implemente um método <code>converterPara(tipoDaMoeda)</code> que converta o valor utilizando as taxas da tabela abaixo e retorne um novo objeto Dinheiro com o valor convertido.
<br>
<br>
<table>
  <thead>
    <tr>
      <th>Moeda</th>
      <th>Valor em Real (BRL)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>REAL</td>
      <td>1.00</td>
    </tr>
    <tr>
      <td>DOLAR</td>
      <td>5.00</td>
    </tr>
    <tr>
      <td>EURO</td>
      <td>5.50</td>
    </tr>
  </tbody>
</table>
{{< /questao >}}

{{< questao >}}
Crie uma classe <code>Carta</code> para representar uma carta de baralho. O naipe e o valor da carta devem ser representados por enumerações.

A classe <code>Carta</code> deve armazenar o naipe e o valor da carta, além de implementar um método <code>compararCom(carta)</code> que compare duas cartas e retorne:
<ul>
<li>1 se a carta atual possuir valor maior;</li>
<li>0 se as cartas possuírem o mesmo valor;</li>
<li>-1 se a carta atual possuir valor menor.</li>
</ul>
<br>
Exemplo:
{{< code >}}
Carta c1 = new Carta(Naipe.COPAS, Valor.REI);
Carta c2 = new Carta(Naipe.ESPADAS, Valor.DEZ);
// Saída: 1
System.out.println(c1.compararCom(c2));
{{< /code >}}

{{< /questao >}}

{{< questao >}}

Crie uma enumeração <code>Operacao</code> para representar operações matemáticas básicas.
A enumeração deve possuir os seguintes enumeradores:

<ul>
    <li>SOMA</li>
    <li>SUBTRACAO</li>
    <li>DIVISAO</li>
    <li>MULTIPLICACAO</li>
</ul>

Implemente um método <code>calcular(a, b)</code> que receba dois valores numéricos e retorne o resultado da operação correspondente.
<br>
Exemplos:
{{< code >}}
// Saída: 15
System.out.println(Operacao.SOMA.calcular(10, 5));
// Saída: 50
System.out.println(Operacao.MULTIPLICACAO.calcular(10, 5));
{{< /code >}}
{{< /questao >}}

{{< /lista-questoes >}}

---
title: "Exercícios"
description: "Exercícios"
slug: exercicios-02
tags:
- python
- exercícios
---

{{< lista-questoes >}}


{{< questao >}}

<b>Problema J - João João (adaptado de Maratona Fase Regional 2025)</b>
<br>

Em 2025, o responsável por coordenar a equipe criadora da prova da OBI – Olimpíada Brasileira de Influenciadores – é o professor João João, que, além de professor, é um famoso e influente influenciador.
<br>
Até o momento, a equipe criou 10 tarefas, e cada uma dessas tarefas foi categorizada em um de quatro níveis de dificuldade: 1, 2, 3 e 4.
<br>
O professor João João deseja saber quantas tarefas ainda faltam ser criadas para que seja possível montar uma prova composta de exatamente quatro tarefas, sendo cada tarefa de um nível de dificuldade distinto.
<br>
Dada a lista dos níveis de dificuldade das tarefas já criadas, você poderia ajudar o professor João João a determinar quantas tarefas faltam ser criadas?
<br>
<b>Entrada</b><br>
A entrada é composta por 10 linhas. Cada linha contém um inteiro D<sub>i</sub>, representando o nível de dificuldade da tarefa i 
(1 ≤ D<sub>i</sub> ≤ 4, para 1 ≤ i ≤ 10).
<br>
<b>Saída</b><br>
Seu programa deve produzir uma única linha na saída, contendo um único número inteiro: a menor quantidade de tarefas que precisam ser criadas para que uma prova com quatro tarefas de níveis distintos possa ser produzida.

<table border="1" cellpadding="8" cellspacing="0">
  <tr>
    <th>Exemplo de entrada 1</th>
    <th>Exemplo de saída 1</th>
  </tr>
  <tr>
    <td>1<br>3<br>4<br>1<br>3<br>4<br>1<br>3<br>4<br>1</td>
    <td style="vertical-align: top;">1</td>
  </tr>
</table>
Explicação do exemplo 1:
Já foram criadas tarefas de níveis de dificuldade 1, 3 e 4. Falta apenas uma tarefa de nível 2, então a resposta é 1.

<table border="1" cellpadding="8" cellspacing="0">
  <tr>
    <th>Exemplo de entrada 2</th>
    <th>Exemplo de saída 2</th>
  </tr>
  <tr>
    <td>4<br>1<br>1<br>4<br>3<br>1<br>2<br>1<br>2<br>2</td>
    <td style="vertical-align: top;">0</td>
  </tr>
</table>
Explicação do exemplo 2:
Já foram criadas tarefas de níveis de dificuldade 1, 2, 3 e 4. Como não falta nenhum nível de dificuldade, a resposta é 0.

{{< solucao letra=" " >}}
{{< code >}}

{{< /code >}}
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}

<b>Problema A - Andando no tempo (adaptado de Maratona Fase Regional 2016)</b>
<br>

Imagine que você tenha uma máquina do tempo que pode ser usada no máximo três vezes, e a cada uso da máquina você pode escolher voltar para o passado ou ir para o futuro. A máquina possui três créditos fixos; cada crédito representa uma certa quantidade de anos, e pode ser usado para ir essa quantidade de anos para o passado ou para o futuro. Você pode fazer uma, duas ou três viagens, e cada um desses três créditos pode ser usado uma vez apenas. Por exemplo, se os créditos forem 5, 12 e 9, você poderia decidir fazer duas viagens: ir 5 anos para o futuro e, depois, voltar 9 anos para o passado. Dessa forma, você terminaria quatro anos no passado, em 2022. Também poderia fazer três viagens, todas indo para o futuro, usando os créditos em qualquer ordem, terminando em 2052.
<br>
Neste problema, dados os valores dos três créditos da máquina, seu programa deve dizer se é ou não possível viajar no tempo e voltar para o presente, fazendo pelo menos uma viagem e, no máximo, três viagens; sempre usando cada um dos três créditos no máximo uma vez.
<br>
<b>Entrada</b><br>
A entrada consiste de três linhas, cada uma contendo o valor de um crédito: A, B e C (1 ≤ A, B, C ≤ 1000).
<br>
<b>Saída</b><br>
Seu programa deve imprimir uma linha contendo o caractere “S” se é possível viajar e voltar para o presente, ou “N” caso contrário.
<table border="1" cellpadding="8" cellspacing="0">
  <tr>
    <th>Exemplo de entrada 1</th>
    <th>Exemplo de saída 1</th>
  </tr>
  <tr>
    <td>22<br>5<br>22</td>
    <td style="vertical-align: top;">S</td>
  </tr>

  <tr>
    <th>Exemplo de entrada 2</th>
    <th>Exemplo de saída 2</th>
  </tr>
  <tr>
    <td>31<br>110<br>79</td>
    <td style="vertical-align: top;">S</td>
  </tr>

  <tr>
    <th>Exemplo de entrada 3</th>
    <th>Exemplo de saída 3</th>
  </tr>
  <tr>
    <td>45<br>8<br>7</td>
    <td style="vertical-align: top;">N</td>
  </tr>
</table>
{{< solucao letra=" " >}}
{{< code >}}

{{< /code >}}
{{< /solucao >}}

{{< /questao >}}

{{< questao >}}

<b>Problema B - Bobo da Corte (Maratona Fase Regional 2019)</b>
<br>

 <a href="https://github.com/univille-cp/cadernos-de-problemas/blob/main/maratona-de-programacao/regional/2019.pdf">Descrição da questão </a>

<br>
<a href="https://judge.beecrowd.com/pt/problems/view/2963">
    Submeta a sua solução no Beecrowd</a>

{{< solucao letra=" " >}}
{{< code >}}

{{< /code >}}
{{< /solucao >}}

{{< /questao >}}

{{< questao >}}

<b>Problema D - Desvendando Mounty hall (Maratona Fase Regional 2018)</b>
<br>

 <a href="https://github.com/univille-cp/cadernos-de-problemas/blob/main/maratona-de-programacao/regional/2018.pdf">Descrição da questão </a>

<br>
<a href="https://codeforces.com/gym/101908/problem/D">
    Submeta a sua solução no CodeForces</a>

{{< solucao letra=" " >}}
{{< code >}}

{{< /code >}}
{{< /solucao >}}

{{< /questao >}}

{{< /lista-questoes >}}

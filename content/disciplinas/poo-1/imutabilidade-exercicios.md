---
title: "Exercícios sobre Imutabilidade"
slug: "imutabilidade-exercicios"
description: "Exercícios sobre imutabilidade"
tags:
- imutabilidade
- record
- exercicios
---

{{< lista-questoes >}}


{{< questao >}}

<p>
Desenvolva uma classe imutável chamada <code>LicensePlate</code> para representar
a placa de um veículo. A classe deve armazenar o número da placa e garantir que
esse valor não possa ser alterado após a criação do objeto.
</p>

<p>
Implemente um construtor que receba o número da placa e realize as validações
necessárias. Considere apenas placas no formato Mercosul, por exemplo:
<code>ABC1D23</code>.
</p>

<p>
A classe não deve possuir métodos <em>setters</em>. Após a criação da instância,
o número da placa deve permanecer inalterado durante toda a vida do objeto.
</p>

<p>
Implemente um método de acesso para consultar o número da placa.
</p>

<p>
Adicione também um método chamado <code>withNumber()</code> que permita criar uma
nova placa com outro número. Como a classe é imutável, esse método não deve
alterar o objeto atual. Em vez disso, ele deve retornar uma nova instância com
o novo valor informado.
</p>

<p>
Ao concluir a implementação, verifique que o objeto original permanece
inalterado após a criação da nova placa.
</p>

{{< /questao >}}


{{< questao >}}
<p>
Desenvolva uma classe imutável chamada <code>Time</code> para representar um horário
composto por horas e minutos. A classe deve garantir que seu estado não possa ser
alterado após a criação da instância.
</p>

<p>
Os valores de hora devem estar no intervalo de <code>0</code> a <code>23</code>, e os
valores de minuto no intervalo de <code>0</code> a <code>59</code>. Realize as validações
necessárias durante a construção do objeto.
</p>

<p>
Implemente métodos que permitam adicionar e subtrair horas e minutos. Como a classe é
imutável, essas operações não devem modificar o objeto atual. Em vez disso, cada método
deve retornar uma nova instância de <code>Time</code> contendo o horário resultante da
operação.
</p>

<p>
Considere também situações em que a operação provoque a mudança de dia. Por exemplo,
ao adicionar 30 minutos ao horário <code>23:45</code>, o resultado deve ser
<code>00:15</code>. Da mesma forma, ao subtrair 20 minutos de <code>00:10</code>,
o resultado deve ser <code>23:50</code>.
</p>

<p>
Implemente um método para exibir o horário no formato <code>HH:mm</code>, garantindo
que horas e minutos sejam apresentados com dois dígitos.
</p>

<p>
Ao concluir a implementação, verifique se o objeto original permanece inalterado após
cada operação, confirmando que a classe é verdadeiramente imutável. Também é recomendável
implementar os métodos <code>equals()</code> e <code>hashCode()</code> para que dois
objetos que representem o mesmo horário sejam considerados equivalentes.
</p>

<p>
Como desafio adicional, reimplemente a solução utilizando um <code>record</code>.
</p>

{{< /questao >}}


{{< /lista-questoes >}}

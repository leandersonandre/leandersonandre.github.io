---
title: "Exercícios sobre Interfaces"
slug: "interfaces-exercicios"
description: "Exercícios sobre Interfaces"
tags:
- interface
- java
---

{{< lista-questoes >}}


{{< questao >}}
Implemente a interface e as classes apresentadas no diagrama abaixo, respeitando as assinaturas dos métodos definidas.
Considere que construtores, getters e setters não estão representados no diagrama, mas devem ser implementados quando necessário.
Após a implementação, instancie objetos de cada classe e apresente no terminal os valores de área e perímetro correspondentes.

{{< plantuml >}}
interface Shape <<interface>>{
  +getArea(): double
  +getPerimeter(): double
}

class Rect{
  -width: double
  -height: double
}

class Triangle{
  -sideA: double
  -sideB: double
  -sideC: double
}

class Circle{
  -radius: double
}

Shape <|.. Rect
Shape <|.. Triangle
Shape <|.. Circle

{{< /plantuml >}}

{{< /questao >}}


{{< questao >}}
Crie uma nova classe responsável por operações com objetos do tipo Shape.
Nessa classe, implemente um método que receba uma lista de Shape e calcule a soma das áreas de todos os elementos. O método deve utilizar apenas a interface Shape (não usar instanceof).
O resultado deve ser retornado como um valor do tipo double.

{{< plantuml >}}
class ShapeUtils {
  -ShapeUtils()
  {static} +getTotalArea(shapes: List<Shape>): double
}
{{< /plantuml >}}
Após implementar:
Crie uma lista contendo objetos Rect, Triangle e Circle
Utilize o método da nova classe para calcular a área total
Exiba o resultado no terminal. 

<b>Observação:</b> O método getTotalArea está sublinhado no diagrama, ou seja, deve ser static.
{{< /questao >}}

{{< questao >}}
Implemente a interface Scalable e adapte as classes já existentes para suportar redimensionamento.
A interface deve permitir que uma forma geométrica tenha suas dimensões alteradas por um fator de escala.
<br>
Regras:
<ul>
  <li>O fator de escala será um valor do tipo double</li>
  <li>Um fator maior que 1 aumenta o tamanho</li>
  <li>Um fator entre 0 e 1 diminui o tamanho</li>
  <li>Considere que o fator será sempre positivo</li>
</ul>

{{< plantuml >}}
interface Scalable <<interface>>{
+scale(factor: double): void
}
interface Shape {
+getArea(): double
+getPerimeter(): double
}

class Rect{
  -width: double
  -height: double
}

class Triangle{
  -sideA: double
  -sideB: double
  -sideC: double
}

class Circle{
  -radius: double
}

Shape <|.. Rect
Shape <|.. Circle
Shape <|.. Triangle

Scalable <|.up. Rect
Scalable <|.up. Circle
Scalable <|.up. Triangle

{{< /plantuml >}}

Após a implementação, crie pelo menos um objeto de cada classe (Rect, Circle e Triangle), exiba a área e o perímetro originais, aplique um fator de escala (por exemplo, 2.0) e, em seguida, exiba novamente a área e o perímetro após o redimensionamento.


{{< /questao >}}

{{< /lista-questoes >}}

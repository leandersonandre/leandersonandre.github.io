---
title : "Algoritmos Gulosos"
slug: "algoritmos-gulosos"
outputs : ["Reveal"]
reveal_hugo:
  theme: "serif"
  custom_css: "css/univille.css"
---

{{% slide-capa titulo="Algoritmos Gulosos" subtitulo="Algoritmos e Programação de Computadores II" %}}

---

## Algoritmos Gulosos

{{% block titulo="Definição" %}}
Algoritmos Gulosos (do inglês, *Greedy Algorithms*) são uma **Técnica de Design de Algoritmos** que consiste em construir uma solução passo a passo, escolhendo, em cada etapa, a alternativa que parece ser a melhor naquele momento, sem reconsiderar as escolhas anteriores, com o objetivo de encontrar uma solução ótima para o problema.
{{% /block %}}

---

## Algoritmos Gulosos

<img src="https://www.clker.com/cliparts/7/c/0/e/15168570801900545645low-hanging-fruit-clipart.hi.png" height="300">



Algoritmos gulosos utilizam a estratégia de *low hanging fruit*.

---

## Algoritmos Gulosos

{{% block titulo="Importante" %}}
Não existem garantias que o algoritmo guloso irá encontrar a solução ótima do problema.
{{% /block %}}


---

## Problema do Troco

{{% block titulo="Algoritmo Guloso" %}}
Escolher sempre a maior moeda sem ultrapassar o valor alvo.
{{% /block %}}


**Exemplo:** moedas = {1,2,5}, alvo = 12.

{{% fragment %}}Escolhido a moeda: 5 (restante: 7)<br>{{% /fragment %}}
{{% fragment %}}Escolhido a moeda: 5 (restante: 2)<br>{{% /fragment %}}
{{% fragment %}}Escolhido a moeda: 2 (restante: 0)<br>{{% /fragment %}}
{{% fragment %}}<b>Solução ótima encontrada: 3 moedas.</b>{{% /fragment %}}

---

## Problema do Troco

{{% block titulo="Algoritmo Guloso" %}}
Escolher sempre a maior moeda sem ultrapassar o valor alvo.
{{% /block %}}


**Exemplo:** moedas = {1,3,4}, alvo = 6.

{{% fragment %}}Escolhido a moeda: 4 (restante: 2)<br>{{% /fragment %}}
{{% fragment %}}Escolhido a moeda: 1 (restante: 1)<br>{{% /fragment %}}
{{% fragment %}}Escolhido a moeda: 1 (restante: 0)<br>{{% /fragment %}}
{{% fragment %}}<b>Solução encontrada. 3 moedas</b><br>{{% /fragment %}}
{{% fragment %}}<b>Solução ótima: 2 moedas ( 3 + 3).</b>{{% /fragment %}}

___

## Problema da Seleção de Atividades

Dado um conjunto de atividades = {a<sub>1</sub>, a<sub>2</sub>, ..., a<sub>n</sub>}, em que cada atividade possui um horário de início e término, encontre o maior subconjunto de atividades que podem ser realizadas sem que haja sobreposição de horários.

___


# Problema da Seleção de Atividades

**Exemplo:** considere as seguintes atividades:

<table style="font-size: 0.7em; margin: auto;">
  <thead>
    <tr>
      <th>Atividade</th>
      <th>Início</th>
      <th>Término</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>A</td><td>1</td><td>4</td></tr>
    <tr><td>B</td><td>3</td><td>5</td></tr>
    <tr><td>C</td><td>0</td><td>6</td></tr>
    <tr><td>D</td><td>5</td><td>7</td></tr>
    <tr><td>E</td><td>8</td><td>9</td></tr>
    <tr><td>F</td><td>5</td><td>9</td></tr>
  </tbody>
</table>

Qual é o maior número de atividades que podem ser realizadas sem sobreposição de horários?

____

# Problema da Seleção de Atividades

**3 atividades**

A (1–4) + D (5–7) + E (8–9)

<table style="font-size: 0.7em; margin: auto;">
  <thead>
    <tr>
      <th>Atividade</th>
      <th>Início</th>
      <th>Término</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>A</td><td>1</td><td>4</td></tr>
    <tr><td>B</td><td>3</td><td>5</td></tr>
    <tr><td>C</td><td>0</td><td>6</td></tr>
    <tr><td>D</td><td>5</td><td>7</td></tr>
    <tr><td>E</td><td>8</td><td>9</td></tr>
    <tr><td>F</td><td>5</td><td>9</td></tr>
  </tbody>
</table>

---

## Problema da Seleção de Atividades

{{% block titulo="Algoritmo Guloso" %}}
Escolher sempre a atividade que termina primeiro, desde que não haja sobreposição com as atividades já selecionadas.
{{% /block %}}

___
## Problema da Mochila Fracionária

Dado um conjunto de itens = {i<sub>1</sub>, i<sub>2</sub>, ..., i<sub>n</sub>}, em que cada item possui um peso e um valor associado, e uma mochila com capacidade máxima de peso, determine a quantidade de cada item que deve ser colocada na mochila para maximizar o valor total transportado, permitindo que os itens sejam divididos em frações.

___

# Problema da Mochila Fracionária

**Exemplo:** considere os seguintes itens e uma mochila com capacidade máxima de 50 kg:

<table style="font-size: 0.7em; margin: auto;">
  <thead>
    <tr>
      <th>Item</th>
      <th>Peso (kg)</th>
      <th>Valor (R$)</th>
      <th>Valor por kg (R$/kg)</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>A</td><td>10</td><td>60</td><td>6</td></tr>
    <tr><td>B</td><td>20</td><td>100</td><td>5</td></tr>
    <tr><td>C</td><td>30</td><td>120</td><td>4</td></tr>
  </tbody>
</table>

Qual é a melhor combinação de itens, considerando que eles podem ser divididos em frações, para maximizar o valor total transportado sem ultrapassar a capacidade da mochila?

___
# Problema da Mochila Fracionária

**Valor máximo: R$ 240,00**

A (10 kg) + B (20 kg) + 2/3 de C (20 kg)

<table style="font-size: 0.7em; margin: auto;">
  <thead>
    <tr>
      <th>Item</th>
      <th>Peso (kg)</th>
      <th>Valor (R$)</th>
      <th>Valor por kg (R$/kg)</th>
      <th>Quantidade utilizada</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>A</td><td>10</td><td>60</td><td>6</td><td>100%</td></tr>
    <tr><td>B</td><td>20</td><td>100</td><td>5</td><td>100%</td></tr>
    <tr><td>C</td><td>30</td><td>120</td><td>4</td><td>66,67%</td></tr>
  </tbody>
</table>

**Capacidade utilizada:** 50 kg

**Valor total:** R\\$60 + R\\$100 + R\\$80 = **R$ 240,00**
___

## Problema da Mochila Fracionária

{{% block titulo="Algoritmo Guloso" %}}
Escolher sempre o item com maior valor por unidade de peso (R$/kg), adicionando-o à mochila até atingir sua capacidade. Se não houver espaço suficiente para o próximo item, adicionar apenas a fração que couber.
{{% /block %}}
___

# Exercícios

{{% block titulo="Exercício 1" %}}
Dado o problema da seleção de atividades, crie a solução utilizando algoritmos gulosos.
{{% /block %}}

{{% block titulo="Exercício 2" %}}
Dado o problema da mochila fracionária, crie a solução  utilizando algoritmos gulosos.
{{% /block %}}

___ 

{{% slide-contracapa %}}

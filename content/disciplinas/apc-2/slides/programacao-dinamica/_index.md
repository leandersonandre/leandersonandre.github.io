---
title : "Programação Dinâmica"
slug: "teste"
outputs : ["Reveal"]
reveal_hugo:
  theme: "serif"
  custom_css: "css/univille.css"
---

{{% slide-capa titulo="Programação Dinâmica" subtitulo="Algoritmos e Programação de Computadores II" %}}


---

## Programação Dinâmica

{{% block titulo="Definição" %}}
**Técnica de Design de Algoritmo** que pode ser utilizada pra encontrar soluções ótima para problemas e contar o número de soluções.
{{% /block %}}
---

## Problema do Troco

Dado um conjunto de moedas  = {c<sub>1</sub>,c<sub>2</sub>,...c<sub>k</sub>} e uma quantidade dinheiro alvo *n*, encontre a menor combinação de moedas que somados resulta na quantidade *n*.

<img src="https://cdn.kastatic.org/ka-perseus-images/0d45efb90c57c071c2495f188bf4e5066555c6b7.png"
     alt="Moedas do real brasileiro"
     style="height: 200px; width: auto;">

---

# Problema do Troco

**Exemplo:** moedas = {1,2,5}, alvo = 12.

Qual é a solução ótima?

{{% fragment %}} 
3 moedas<br>
5 + 5 + 2 = 12
{{% /fragment %}}

---

# Problema do Troco
**Exemplo:** moedas = {1,2,5}, alvo = 12.

Qual foi a estratégia adotada?

{{% fragment %}} Selecione sempre a maior moeda sem exceder o valor da soma.{{% /fragment %}}
<br>
{{% fragment %}} **Algoritmo guloso** {{% /fragment %}}


---

# Problema do Troco

**Exemplo:** moedas = {1,3, 4}, alvo = 6.

Qual é a solução ótima?


{{% fragment %}}**Algoritmo guloso:** 3 moedas: 4 + 1 + 1 = 6 {{% /fragment %}}
<br>
{{% fragment %}}**Solução ótima:**  2 moedas: 3 + 3 = 6 {{% /fragment %}}

---

# Problema do Troco

Algoritmos gulosos <b>não garantem</b> a solução ótima.
<br><br>

Algoritmos de força bruta <b>garantem a solução ótima</b> por explorar todas as possibilidades, mas podem ser <b>muito lentos</b> para uma grande quantidade de dados de entrada.

---

 ### Qual é a alternativa?

 A programação dinâmica pode encontrar a solução ótima como a força bruta mas sendo <b>eficiente</b>.
___


 ### Procurando a solução ótima
O problema pode ser reformulado de maneira recursiva para encontrar a solução para os seus subproblemas.

___

**Por exemplo:** moedas  = {1,3,4}

| Expressão  | Valor | Expressão   | Valor |
| ---------- | ----- | ----------- | ----- |
| `resolver(0)` | 0     | `resolver(6)`  | 2     |
| `resolver(1)` | 1     | `resolver(7)`  | 2     |
| `resolver(2)` | 2     | `resolver(8)`  | 2     |
| `resolver(3)` | 1     | `resolver(9)`  | 3     |
| `resolver(4)` | 1     | `resolver(10)` | 3     |
| `resolver(5)` | 2     |             |       |

___

A propriedade essencial de *resolver* é que seus valores podem ser calculadas recursivamente para os valores menores.
<br>
**Por exemplo:** moedas  = {1,3,4}
```
resolver(x) = min(resolver(x-1) + 1,
                  resolver(x-3) + 1,
                  resolver(x-4) + 1)
                  
```

O caso base da recursão é resolver(0) = 0.
___

# Chamadas recursivas do algortimo

A cada nível, uma moeda é utilizada.

<div class="sem-margem">
{{< plantuml >}}

@startuml
top to bottom direction
skinparam linetype ortho
skinparam shadowing false
skinparam rectangle {
  BorderColor #444444
  FontColor black
}

rectangle "10" as n10 #D9EAF7

rectangle "9" as n9 #D5F5E3
rectangle "7" as n8 #FCF3CF
rectangle "6" as n6 #E8DAEF

rectangle "8" as n9_1 #FCF3CF
rectangle "6" as n9_2 #F5CBA7
rectangle "5" as n9_4 #FADBD8

rectangle "6" as n8_1 #F5CBA7
rectangle "4" as n8_2 #E8DAEF
rectangle "3" as n8_4 #D6EAF8

rectangle "5" as n6_1 #FADBD8
rectangle "3" as n6_2 #D6EAF8
rectangle "2" as n6_4 #D5DBDB

rectangle "7" as n9_1_1 #F5CBA7
rectangle "5" as n9_1_2 #E8DAEF
rectangle "4" as n9_1_4 #D6EAF8

rectangle "5" as n9_2_1 #E8DAEF
rectangle "3" as n9_2_2 #FADBD8
rectangle "2" as n9_2_4 #E5E7E9

rectangle "4" as n9_4_1 #D6EAF8
rectangle "2" as n9_4_2 #E5E7E9
rectangle "1" as n9_4_4 #D5DBDB

rectangle "5" as n8_1_1 #E8DAEF
rectangle "3" as n8_1_2 #FADBD8
rectangle "2" as n8_1_4 #E5E7E9

rectangle "3" as n8_2_1 #FADBD8
rectangle "1" as n8_2_2 #D6EAF8
rectangle "0" as n8_2_4 #D5DBDB

rectangle "2" as n8_4_1 #E5E7E9
rectangle "0" as n8_4_2 #D5DBDB
rectangle "-1" as n8_4_4 #D5F5E3

rectangle "4" as n6_1_1 #D6EAF8
rectangle "2" as n6_1_2 #E5E7E9
rectangle "1" as n6_1_4 #D5DBDB

rectangle "2" as n6_2_1 #E5E7E9
rectangle "0" as n6_2_2 #D5DBDB
rectangle "-1" as n6_2_4 #D5F5E3

rectangle "1" as n6_4_1 #D5DBDB
rectangle "-1" as n6_4_2 #D5F5E3
rectangle "-2" as n6_4_4 #F5B7B1

n10 --> n9
n10 --> n8
n10 --> n6

n9 --> n9_1
n9 --> n9_2
n9 --> n9_4

n8 --> n8_1
n8 --> n8_2
n8 --> n8_4

n6 --> n6_1
n6 --> n6_2
n6 --> n6_4

n9_1 --> n9_1_1
n9_1 --> n9_1_2
n9_1 --> n9_1_4

n9_2 --> n9_2_1
n9_2 --> n9_2_2
n9_2 --> n9_2_4

n9_4 --> n9_4_1
n9_4 --> n9_4_2
n9_4 --> n9_4_4

n8_1 --> n8_1_1
n8_1 --> n8_1_2
n8_1 --> n8_1_4

n8_2 --> n8_2_1
n8_2 --> n8_2_2
n8_2 --> n8_2_4

n8_4 --> n8_4_1
n8_4 --> n8_4_2
n8_4 --> n8_4_4

n6_1 --> n6_1_1
n6_1 --> n6_1_2
n6_1 --> n6_1_4

n6_2 --> n6_2_1
n6_2 --> n6_2_2
n6_2 --> n6_2_4

n6_4 --> n6_4_1
n6_4 --> n6_4_2
n6_4 --> n6_4_4

@enduml
</div>
{{< /plantuml >}}

___

# Chamadas recursivas do algortimo

Caminhos das soluções possíveis.

<div class="sem-margem">
{{< plantuml >}}

@startuml
top to bottom direction
skinparam linetype ortho
skinparam shadowing false
skinparam rectangle {
  BorderColor #444444
  FontColor WHITE
}

rectangle "10" as n10 #000000

rectangle "9" as n9 #FFFFFF
rectangle "7" as n8 #000000
rectangle "6" as n6 #000000

rectangle "8" as n9_1 #FFFFFF
rectangle "6" as n9_2 #FFFFFF
rectangle "5" as n9_4 #FFFFFF

rectangle "6" as n8_1 #FFFFFF
rectangle "4" as n8_2 #000000
rectangle "3" as n8_4 #000000

rectangle "5" as n6_1 #FFFFFF
rectangle "3" as n6_2 #000000
rectangle "2" as n6_4 #FFFFFF

rectangle "7" as n9_1_1 #FFFFFF
rectangle "5" as n9_1_2 #FFFFFF
rectangle "4" as n9_1_4 #FFFFFF

rectangle "5" as n9_2_1 #FFFFFF
rectangle "3" as n9_2_2 #FFFFFF
rectangle "2" as n9_2_4 #FFFFFF

rectangle "4" as n9_4_1 #FFFFFF
rectangle "2" as n9_4_2 #FFFFFF
rectangle "1" as n9_4_4 #FFFFFF

rectangle "5" as n8_1_1 #FFFFFF
rectangle "3" as n8_1_2 #FFFFFF
rectangle "2" as n8_1_4 #FFFFFF

rectangle "3" as n8_2_1 #FFFFFF
rectangle "1" as n8_2_2 #FFFFFF
rectangle "0" as n8_2_4 #000000

rectangle "2" as n8_4_1 #FFFFFF
rectangle "0" as n8_4_2 #000000
rectangle "-1" as n8_4_4 #FFFFFF

rectangle "4" as n6_1_1 #FFFFFF
rectangle "2" as n6_1_2 #FFFFFF
rectangle "1" as n6_1_4 #FFFFFF

rectangle "2" as n6_2_1 #FFFFFF
rectangle "0" as n6_2_2 #000000
rectangle "-1" as n6_2_4 #FFFFFF

rectangle "1" as n6_4_1 #FFFFFF
rectangle "-1" as n6_4_2 #FFFFFF
rectangle "-2" as n6_4_4 #FFFFFF

n10 --> n9
n10 --> n8
n10 --> n6

n9 --> n9_1
n9 --> n9_2
n9 --> n9_4

n8 --> n8_1
n8 --> n8_2
n8 --> n8_4

n6 --> n6_1
n6 --> n6_2
n6 --> n6_4

n9_1 --> n9_1_1
n9_1 --> n9_1_2
n9_1 --> n9_1_4

n9_2 --> n9_2_1
n9_2 --> n9_2_2
n9_2 --> n9_2_4

n9_4 --> n9_4_1
n9_4 --> n9_4_2
n9_4 --> n9_4_4

n8_1 --> n8_1_1
n8_1 --> n8_1_2
n8_1 --> n8_1_4

n8_2 --> n8_2_1
n8_2 --> n8_2_2
n8_2 --> n8_2_4

n8_4 --> n8_4_1
n8_4 --> n8_4_2
n8_4 --> n8_4_4

n6_1 --> n6_1_1
n6_1 --> n6_1_2
n6_1 --> n6_1_4

n6_2 --> n6_2_1
n6_2 --> n6_2_2
n6_2 --> n6_2_4

n6_4 --> n6_4_1
n6_4 --> n6_4_2
n6_4 --> n6_4_4

@enduml
</div>
{{< /plantuml >}}

___

# Solução

**Por exemplo:** moedas  = {1,3,4}, soma = 10
```
resolver(10) = resolver(7) + 1  // x - 3
             = resolver(4) + 2  // x - 2
             = resolver(0) + 3  // x - 4     
             = 3           
```

___

# Algoritmo recursivo

```math

\operatorname{resolver}(x)=
\begin{cases}
\infty, & x < 0 \\
0, & x = 0 \\
\displaystyle\min_{c \in \text{moedas}}
\left\{\operatorname{resolver}(x-c)+1\right\}, & x > 0
\end{cases}
```


{{% block titulo="Exercício" %}}
Codifique a solução recursiva para o problema do troco utilizando a linguagem Python.

**Entrada:** moedas = {1,3,4},  x = 10

**Saída:** 3
{{% /block %}}
___

# Solução
```python
def resolver(soma,moedas):
    if soma < 0:
        return float('inf')
    if soma == 0:
        return 0
    menor = float('inf')
    for m in moedas:
        r = resolver(soma-m, moedas)
        menor = min(menor,r)
    return menor
```


```python
moedas = [1,3,4]
resultado = resolver(10,moedas)
print("Resultado:",resultado)
```

___



{{% slide-contracapa %}}

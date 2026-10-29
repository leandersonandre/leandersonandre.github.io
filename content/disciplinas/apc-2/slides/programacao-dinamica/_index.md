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
### Programação Dinâmica

Técnica de Design de Algoritmo que pode ser utilizada pra encontrar soluções ótima para problemas e contar o número de soluções.


---

## Problema do Troco

Dado um conjunto de moedas  = {c<sub>1</sub>,c<sub>2</sub>,...c<sub>k</sub>} e uma quantidade dinheiro alvo *n*, encontre a menor combinação de moedas que somados resulta na quantidade *n*.

---

**Exemplo:** moedas = {1,2,5}, alvo = 12.

Qual é a solução ótima?

{{% fragment %}} 
3 moedas<br>
5 + 5 + 2 = 12
{{% /fragment %}}

---

**Exemplo:** moedas = {1,2,5}, alvo = 12.

Qual foi a estratégia adotada?

{{% fragment %}} Selecione sempre a maior moeda sem exceder o valor da soma.{{% /fragment %}}
<br>
{{% fragment %}} **Algoritmo guloso** {{% /fragment %}}


---


**Exemplo:** moedas = {1,3, 4}, alvo = 6.

Qual é a solução ótima?


{{% fragment %}}**Algoritmo guloso:** 3 moedas: 4 + 1 + 1 = 6 {{% /fragment %}}
<br>
{{% fragment %}}**Solução ótima:**  2 moedas: 3 + 3 = 6 {{% /fragment %}}

---


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


**Por exemplo:** moedas  = {1,3,4}, soma = 10
```
resolver(10) = resolver(7) + 1  // x - 3
             = resolver(4) + 2  // x - 2
             = resolver(0) + 3  // x - 4     
             = 3           
```

___

```math

\operatorname{resolver}(x)=
\begin{cases}
\infty, & x < 0 \\
0, & x = 0 \\
\displaystyle\min_{c \in \text{moedas}}
\left\{\operatorname{resolver}(x-c)+1\right\}, & x > 0
\end{cases}
```

**Resolver:** moedas  = {1,3,4}, soma = 10
___


{{% slide-contracapa %}}

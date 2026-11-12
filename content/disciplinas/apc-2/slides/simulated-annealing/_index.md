---
title : "Simulated Annealing"
slug: "simulated-annealing"
outputs : ["Reveal"]
reveal_hugo:
  theme: "serif"
  custom_css: "css/univille.css"
---

{{% slide-capa titulo="Simulated Annealing" subtitulo="Algoritmos e Programação de Computadores II" %}}


---

## Simulated Annealing

{{% block titulo="Definição" %}}
**Recozimento Simulado (Simulated Annealing):** metaheurística de otimização inspirada no processo de aquecimento e resfriamento controlado de materiais, utilizado na metalurgia.
{{% /block %}}

Proposto por Kirkpatrick, Gelatt e Vecchi (1983).


---

## Simulated Annealing

Processo de recozimento de materiais metálicos.

<img  src="https://rs.jlccnc.com/static/image/blog/Knowledge-Hub/CNC-Machining-Fundamentals/Annealing-steel-slabs-in-the-hot-rolling-mill.jpg" height="400px">



---


## Simulated Annealing

{{% block titulo="Aplicações" %}}
* **Engenharia:** otimização de circuitos, projetos e estruturas.
* **Medicina:** planejamento de radioterapia e processamento de imagens médicas.
* **Pesquisa operacional:** problemas de roteamento, escalonamento e alocação de recursos.
{{% /block %}}

---

## Analogia com o recozimento

| Processo físico | Algoritmo |
|---|---|
| Temperatura | Temperatura de controle |
| Estado do material | Solução candidata |
| Energia do material | Função de custo |
| Resfriamento gradual | Redução da temperatura |
| Equilíbrio térmico | Estabilização da busca |

___

## Analogia com o recozimento

- **Temperaturas elevadas:** permitem maior mobilidade dos átomos, favorecendo a exploração de diferentes regiões do espaço de busca (diversificação).
- **Temperaturas baixas:** reduzem a mobilidade dos átomos, favorecendo a estabilização em regiões promissoras (intensificação).

---

## Simulated Annealing

{{% block titulo="Características" %}}
* **Solução única:** trabalha com uma solução candidata por vez.
* **Iterativo:** gera soluções vizinhas e atualiza a solução atual ao longo das iterações.
* **Espaço de busca:** pode ser aplicado a problemas de otimização contínua e discreta.
{{% /block %}}
---

## Pseudocódigo

<pre>
<b>x</b> ← solução inicial
<b>E</b> ← custo(x)
<b>T</b> ← temperatura inicial

<b>enquanto</b> critério de parada não for atingido <b>faça</b>
    T ← atualizar temperatura(T)

    x' ← gerar vizinho(x)
    E' ← custo(x')

    ΔE ← E' - E

    <b>se</b> ΔE < 0 <b>ou</b> aleatório(0,1) < exp(-ΔE/T) <b>então</b>
        x ← x'
        E ← E'
    <b>fim se</b>
<b>fim enquanto</b>

<b>retornar</b> x
</pre>

---

## Geração da solução inicial

{{% block titulo="" %}}
* **Solução inicial:** pode ser gerada aleatoriamente ou construída por meio de uma heurística.
* **Avaliação:** calcula-se o custo da solução inicial.
* **Inicialização:** a solução gerada passa a ser a solução atual e a melhor solução encontrada.
{{% /block %}}

---

## Critério de parada

{{% block titulo="" %}}
O algoritmo pode encerrar sua execução quando uma das seguintes condições for atingida:

* **Temperatura mínima:** a temperatura atinge um valor limite predefinido.
* **Número máximo de iterações:** atinge-se o limite de iterações estabelecido.
* **Número de iterações sem melhoria:** não ocorre melhoria na melhor solução encontrada após determinado número de iterações.
* **Tempo máximo:** o tempo de execução atinge o limite estabelecido.
{{% /block %}}

___

## Atualização da temperatura

{{% block titulo="" %}}
A temperatura é reduzida gradualmente durante a execução do algoritmo, controlando a probabilidade de aceitação de soluções piores.
{{% /block %}}

**Resfriamento geométrico:**

```math
T_{k+1} = \alpha \cdot T_k
```

___

## Simulated Annealing

Onde:
- $T_k$: temperatura atual.
- $T_{k+1}$: nova temperatura.
- $\alpha$: taxa de resfriamento, com $0 < \alpha < 1$.
- $\alpha$ próximo de 1: resfriamento mais lento.
- $\alpha$ menor: resfriamento mais rápido.

---

## Geração do vizinho (perturbação)

{{% block titulo="" %}}
Consiste em modificar a solução atual para gerar uma nova solução candidata.

* **Problemas discretos:** troca, inserção, remoção ou inversão de elementos.
* **Problemas contínuos:** alteração dos valores das variáveis por meio de pequenas perturbações.
* **Vizinhança:** conjunto de soluções que podem ser obtidas a partir da solução atual.
{{% /block %}}

___


## Perturbação em domínio contínuo

{{% block titulo="" %}}
A nova solução é gerada adicionando um ruído aleatório com distribuição normal à solução atual:
{{% /block %}}

```math
x' = x + \epsilon
```

```math
\epsilon \sim \mathcal{N}(0,\sigma^2)
```

Onde:
- $\epsilon$: perturbação aleatória.
- $\sigma$: desvio padrão, que controla a magnitude da perturbação.

---

## Aceitação de soluções

Diferentemente de uma busca local tradicional, o Simulated Annealing pode aceitar soluções que apresentam um custo maior.

- **Melhores soluções:** sempre são aceitas.
- **Piores soluções:** podem ser aceitas com determinada probabilidade.
- **Temperatura elevada:** maior probabilidade de aceitar soluções piores.
- **Temperatura baixa:** menor probabilidade de aceitar soluções piores.

---

## Probabilidade de aceitação

A probabilidade de aceitar uma solução pior é calculada por:


```math
P(\text{aceitar}) = e^{-\frac{\Delta E}{T}}
```


---

## Probabilidade de aceitação

Onde:
- $\Delta E$: aumento do custo da solução ($\Delta E > 0$).
- $T$: temperatura atual.
- $e$: constante de Euler.
- Quanto maior a temperatura, maior a probabilidade de aceitar soluções piores.
- Quanto maior o aumento do custo, menor a probabilidade de aceitação.

___

# Parâmetros
<table style="font-size: 0.5em;">
  <thead>
    <tr>
      <th>Parâmetro</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>T₀</code></td>
      <td>Temperatura inicial do algoritmo.</td>
    </tr>
    <tr>
      <td><code>Tmin</code></td>
      <td>Temperatura mínima utilizada como critério de parada.</td>
    </tr>
    <tr>
      <td><code>α</code></td>
      <td>Taxa de resfriamento, utilizada para reduzir a temperatura.</td>
    </tr>
    <tr>
      <td><code>k</code></td>
      <td>Iteração atual do algoritmo.</td>
    </tr>
    <tr>
      <td><code>x₀</code></td>
      <td>Solução inicial do algoritmo.</td>
    </tr>
    <tr>
      <td><code>E(x)</code></td>
      <td>Função objetivo que avalia o custo de uma solução.</td>
    </tr>
    <tr>
      <td><code>ΔE</code></td>
      <td>Variação do custo entre a solução candidata e a solução atual.</td>
    </tr>
    <tr>
      <td><code>ε</code></td>
      <td>Perturbação aleatória utilizada para gerar vizinhos em problemas contínuos.</td>
    </tr>
    <tr>
      <td><code>σ</code></td>
      <td>Desvio padrão da distribuição normal, controla a intensidade da perturbação.</td>
    </tr>
    <tr>
      <td><code>iterMax</code></td>
      <td>Número máximo de iterações.</td>
    </tr>
    <tr>
      <td><code>iterSemMelhoria</code></td>
      <td>Limite de iterações consecutivas sem melhoria na melhor solução.</td>
    </tr>
    <tr>
      <td><code>tempoMax</code></td>
      <td>Tempo máximo de execução do algoritmo.</td>
    </tr>
  </tbody>
</table>

---

## Pseudocódigo

<pre>
<b>x</b> ← solução inicial
<b>E</b> ← custo(x)
<b>T</b> ← temperatura inicial

<b>enquanto</b> critério de parada não for atingido <b>faça</b>
    T ← atualizar temperatura(T)

    x' ← gerar vizinho(x)
    E' ← custo(x')

    ΔE ← E' - E

    <b>se</b> ΔE < 0 <b>ou</b> aleatório(0,1) < exp(-ΔE/T) <b>então</b>
        x ← x'
        E ← E'
    <b>fim se</b>
<b>fim enquanto</b>

<b>retornar</b> x
</pre>

___ 

{{% slide-contracapa %}}

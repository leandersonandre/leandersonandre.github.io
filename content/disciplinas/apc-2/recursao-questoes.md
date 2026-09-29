---
title: "Questões sobre Recursão"
description: "Questões sobre recursão em Python"
slug: recursao-questoes
tags:
- python
- recursao
- questões
---

{{< lista-questoes >}}

{{< questao >}}
O que é uma <b>função recursiva</b> em Python?

{{< alternativa >}} Uma função que chama a si mesma durante sua execução. {{< /alternativa >}}
{{< alternativa >}} Uma função que pode ser chamada apenas uma vez. {{< /alternativa >}}
{{< alternativa >}} Uma função que não possui parâmetros. {{< /alternativa >}}
{{< alternativa >}} Uma função que sempre retorna uma String. {{< /alternativa >}}
{{< solucao letra="A" >}}
Uma função recursiva é uma função que realiza uma chamada para ela mesma durante sua execução.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a principal característica de uma função recursiva?

{{< alternativa >}} Ela chama outra função obrigatoriamente. {{< /alternativa >}}
{{< alternativa >}} Ela chama a si mesma. {{< /alternativa >}}
{{< alternativa >}} Ela não pode possuir parâmetros. {{< /alternativa >}}
{{< alternativa >}} Ela não pode utilizar `return`. {{< /alternativa >}}
{{< solucao letra="B" >}}
A característica fundamental da recursão é que uma função realiza uma chamada para ela mesma.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. Qual é a característica que torna essa função recursiva?

{{< code >}}
def contar(n):
    if n == 0:
        return
    print(n)
    contar(n - 1)
{{< /code >}}

{{< alternativa >}} A função possui um parâmetro. {{< /alternativa >}}
{{< alternativa >}} A função utiliza um `if`. {{< /alternativa >}}
{{< alternativa >}} A função chama `contar` dentro de seu próprio corpo. {{< /alternativa >}}
{{< alternativa >}} A função utiliza `print`. {{< /alternativa >}}
{{< solucao letra="C" >}}
A função é recursiva porque `contar` realiza uma chamada para a própria função dentro de seu corpo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Uma função recursiva normalmente precisa de uma condição que determine quando a recursão deve parar. Essa condição é chamada de:

{{< alternativa >}} Caso inicial. {{< /alternativa >}}
{{< alternativa >}} Caso base. {{< /alternativa >}}
{{< alternativa >}} Caso final. {{< /alternativa >}}
{{< alternativa >}} Caso padrão. {{< /alternativa >}}
{{< solucao letra="B" >}}
O caso base é a condição que interrompe a sequência de chamadas recursivas.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. Qual parte representa o <b>caso base</b>?

{{< code >}}
def contar(n):
    if n == 0:
        return
    print(n)
    contar(n - 1)
{{< /code >}}

{{< alternativa >}} `print(n)` {{< /alternativa >}}
{{< alternativa >}} `contar(n - 1)` {{< /alternativa >}}
{{< alternativa >}} `if n == 0:` {{< /alternativa >}}
{{< alternativa >}} `def contar(n):` {{< /alternativa >}}
{{< solucao letra="C" >}}
A condição `if n == 0` define o caso base. Quando ela é verdadeira, a função executa `return` e encerra a recursão.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. O que será impresso?

{{< code >}}
def contar(n):
    if n == 0:
        return
    print(n)
    contar(n - 1)

contar(3)
{{< /code >}}

{{< alternativa >}} 1, 2, 3 {{< /alternativa >}}
{{< alternativa >}} 3, 2, 1 {{< /alternativa >}}
{{< alternativa >}} 3, 2, 1, 0 {{< /alternativa >}}
{{< alternativa >}} 0, 1, 2, 3 {{< /alternativa >}}
{{< solucao letra="B" >}}
A função imprime `3`, depois chama `contar(2)`, imprime `2` e depois `contar(1)`. Por fim, imprime `1` e chega ao caso base.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. Quantas vezes a função `contar` é chamada?

{{< code >}}
def contar(n):
    if n == 0:
        return
    print(n)
    contar(n - 1)

contar(3)
{{< /code >}}

{{< alternativa >}} 2 vezes. {{< /alternativa >}}
{{< alternativa >}} 3 vezes. {{< /alternativa >}}
{{< alternativa >}} 4 vezes. {{< /alternativa >}}
{{< alternativa >}} 5 vezes. {{< /alternativa >}}
{{< solucao letra="C" >}}
A função é chamada com `3`, depois com `2`, depois com `1` e finalmente com `0`, totalizando 4 chamadas.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. O que acontece quando `n` é igual a `0`?

{{< code >}}
def contar(n):
    if n == 0:
        return
    print(n)
    contar(n - 1)
{{< /code >}}

{{< alternativa >}} A função chama `contar(-1)`. {{< /alternativa >}}
{{< alternativa >}} A função é encerrada pelo `return`. {{< /alternativa >}}
{{< alternativa >}} A função imprime `0`. {{< /alternativa >}}
{{< alternativa >}} A função começa novamente com `n = 3`. {{< /alternativa >}}
{{< solucao letra="B" >}}
Quando `n` é `0`, a condição do caso base é verdadeira e o `return` encerra a função.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
O que pode acontecer se uma função recursiva não possuir uma condição adequada para interromper as chamadas?

{{< alternativa >}} A função será executada apenas uma vez. {{< /alternativa >}}
{{< alternativa >}} A função poderá realizar chamadas recursivas indefinidamente. {{< /alternativa >}}
{{< alternativa >}} O Python transforma automaticamente a função em um laço. {{< /alternativa >}}
{{< alternativa >}} A função sempre retornará `None`. {{< /alternativa >}}
{{< solucao letra="B" >}}
Sem uma condição adequada para interromper a recursão, novas chamadas podem continuar sendo realizadas indefinidamente.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo. Qual valor será retornado?

{{< code >}}
def fatorial(n):
    if n == 0:
        return 1
    return n * fatorial(n - 1)

print(fatorial(3))
{{< /code >}}

{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 6 {{< /alternativa >}}
{{< alternativa >}} 9 {{< /alternativa >}}
{{< alternativa >}} 12 {{< /alternativa >}}
{{< solucao letra="B" >}}
A função calcula `3 * 2 * 1 * 1`, resultando em `6`.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
No código abaixo, qual é o <b>caso base</b> da função `fatorial`?

{{< code >}}
def fatorial(n):
    if n == 0:
        return 1
    return n * fatorial(n - 1)
{{< /code >}}

{{< alternativa >}} `return n` {{< /alternativa >}}
{{< alternativa >}} `return n * fatorial(n - 1)` {{< /alternativa >}}
{{< alternativa >}} `if n == 0:` {{< /alternativa >}}
{{< alternativa >}} `fatorial(n - 1)` {{< /alternativa >}}
{{< solucao letra="C" >}}
A condição `if n == 0` define o caso base. Quando `n` é `0`, a função retorna `1` sem realizar outra chamada recursiva.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. Qual é a chamada recursiva?

{{< code >}}
def fatorial(n):
    if n == 0:
        return 1
    return n * fatorial(n - 1)
{{< /code >}}

{{< alternativa >}} `fatorial(n)` {{< /alternativa >}}
{{< alternativa >}} `fatorial(n - 1)` {{< /alternativa >}}
{{< alternativa >}} `return 1` {{< /alternativa >}}
{{< alternativa >}} `if n == 0` {{< /alternativa >}}
{{< solucao letra="B" >}}
A chamada `fatorial(n - 1)` é recursiva porque chama novamente a própria função `fatorial`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. Qual será a primeira chamada realizada pela função?

{{< code >}}
def fatorial(n):
    if n == 0:
        return 1
    return n * fatorial(n - 1)

print(fatorial(4))
{{< /code >}}

{{< alternativa >}} `fatorial(0)` {{< /alternativa >}}
{{< alternativa >}} `fatorial(1)` {{< /alternativa >}}
{{< alternativa >}} `fatorial(3)` {{< /alternativa >}}
{{< alternativa >}} `fatorial(4)` {{< /alternativa >}}
{{< solucao letra="D" >}}
A chamada inicial é `fatorial(4)`. Dentro dela, será realizada posteriormente a chamada recursiva com `fatorial(3)`.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Analise o código abaixo. Qual será a sequência de chamadas até chegar ao caso base?

{{< code >}}
def contar(n):
    if n == 0:
        return
    contar(n - 1)

contar(3)
{{< /code >}}

{{< alternativa >}} `3 → 2 → 1 → 0` {{< /alternativa >}}
{{< alternativa >}} `3 → 1 → 0` {{< /alternativa >}}
{{< alternativa >}} `0 → 1 → 2 → 3` {{< /alternativa >}}
{{< alternativa >}} `3 → 2 → 0` {{< /alternativa >}}
{{< solucao letra="A" >}}
A chamada começa com `3`. A cada chamada, `n` é reduzido em 1, produzindo `3 → 2 → 1 → 0`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. O que será impresso?

{{< code >}}
def contar(n):
    if n == 0:
        return
    print(n)
    contar(n - 1)

contar(5)
{{< /code >}}

{{< alternativa >}} 5, 4, 3, 2, 1 {{< /alternativa >}}
{{< alternativa >}} 1, 2, 3, 4, 5 {{< /alternativa >}}
{{< alternativa >}} 5, 4, 3, 2, 1, 0 {{< /alternativa >}}
{{< alternativa >}} 0, 1, 2, 3, 4, 5 {{< /alternativa >}}
{{< solucao letra="A" >}}
A função imprime o valor atual antes de realizar a chamada recursiva. Assim, a saída é `5, 4, 3, 2, 1`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. O que será impresso?

{{< code >}}
def contar(n):
    if n == 0:
        return
    contar(n - 1)
    print(n)

contar(3)
{{< /code >}}

{{< alternativa >}} 3, 2, 1 {{< /alternativa >}}
{{< alternativa >}} 1, 2, 3 {{< /alternativa >}}
{{< alternativa >}} 3, 1, 2 {{< /alternativa >}}
{{< alternativa >}} 0, 1, 2, 3 {{< /alternativa >}}
{{< solucao letra="B" >}}
A chamada recursiva ocorre antes do `print`. A função chega até `0` e, no retorno das chamadas, imprime `1`, `2` e `3`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. Qual será o resultado?

{{< code >}}
def soma(n):
    if n == 0:
        return 0
    return n + soma(n - 1)

print(soma(4))
{{< /code >}}

{{< alternativa >}} 4 {{< /alternativa >}}
{{< alternativa >}} 6 {{< /alternativa >}}
{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 16 {{< /alternativa >}}
{{< solucao letra="C" >}}
A função calcula `4 + 3 + 2 + 1 + 0`, resultando em `10`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
No código abaixo, qual valor é retornado pelo <b>caso base</b>?

{{< code >}}
def soma(n):
    if n == 0:
        return 0
    return n + soma(n - 1)
{{< /code >}}

{{< alternativa >}} `0` {{< /alternativa >}}
{{< alternativa >}} `1` {{< /alternativa >}}
{{< alternativa >}} `n` {{< /alternativa >}}
{{< alternativa >}} `n - 1` {{< /alternativa >}}
{{< solucao letra="A" >}}
Quando `n` é `0`, a condição do caso base é satisfeita e a função retorna `0`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. Quantas chamadas recursivas são realizadas durante a execução de `soma(4)`?

{{< code >}}
def soma(n):
    if n == 0:
        return 0
    return n + soma(n - 1)

print(soma(4))
{{< /code >}}

{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< solucao letra="C" >}}
A chamada inicial é `soma(4)`. Ela realiza chamadas para `soma(3)`, `soma(2)`, `soma(1)` e `soma(0)`, totalizando 4 chamadas recursivas.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. Qual afirmação está correta?

{{< code >}}
def dobro(n):
    if n == 0:
        return 0
    return 2 + dobro(n - 1)
{{< /code >}}

{{< alternativa >}} A função não é recursiva porque possui um `return`. {{< /alternativa >}}
{{< alternativa >}} A função é recursiva porque chama `dobro` dentro de seu próprio corpo. {{< /alternativa >}}
{{< alternativa >}} A função é recursiva somente quando `n` é negativo. {{< /alternativa >}}
{{< alternativa >}} A função não possui caso base. {{< /alternativa >}}
{{< solucao letra="B" >}}
A função é recursiva porque realiza uma chamada para `dobro` dentro da própria definição.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. Qual será o valor retornado?

{{< code >}}
def dobro(n):
    if n == 0:
        return 0
    return 2 + dobro(n - 1)

print(dobro(3))
{{< /code >}}

{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 6 {{< /alternativa >}}
{{< solucao letra="D" >}}
A função calcula `2 + 2 + 2 + 0`, resultando em `6`.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Qual dos códigos abaixo apresenta corretamente uma função recursiva com um caso base?

{{< alternativa >}}
{{< code >}}
def contar(n):
    if n == 0:
        return
    contar(n - 1)
{{< /code >}}
{{< /alternativa >}}
{{< alternativa >}}
{{< code >}}
def contar(n):
    contar(n - 1)
{{< /code >}}
{{< /alternativa >}}
{{< alternativa >}}
{{< code >}}
    def contar(n):
        print(n)
{{< /code >}}
{{< /alternativa >}}
{{< alternativa >}}
{{< code >}}
    def contar(n):
        return n
{{< /code >}}
{{< /alternativa >}}


{{< solucao letra="A" >}}
    A primeira alternativa possui uma chamada recursiva e uma condição que interrompe a recursão quando n chega a 0.
{{< /solucao >}}

{{< /questao >}}


{{< questao >}}
    Analise o código abaixo. O que será impresso?
    {{< code >}}
    def fatorial(n):
      if n == 1:
        return 1
      return n * fatorial(n - 1)
    print(fatorial(4))
    {{< /code >}}
    {{< alternativa >}} 4 {{< /alternativa >}}
    {{< alternativa >}} 10 {{< /alternativa >}}
    {{< alternativa >}} 16 {{< /alternativa >}}
    {{< alternativa >}} 24 {{< /alternativa >}}
    {{< solucao letra="D" >}}
    A função calcula 4 * 3 * 2 * 1, resultando em 24.
    {{< /solucao >}}
    {{< /questao >}}

    {{< questao >}}
        Considere a execução de fatorial(3):
        {{< code >}}
        def fatorial(n):
           if n == 1:
             return 1
           return n * fatorial(n - 1)
        {{< /code >}}
        Qual sequência representa corretamente as chamadas realizadas?
        {{< alternativa >}} fatorial(3) → fatorial(2) → fatorial(1) {{< /alternativa >}}
        {{< alternativa >}} fatorial(3) → fatorial(1) → fatorial(2) {{< /alternativa >}}
        {{< alternativa >}} fatorial(1) → fatorial(2) → fatorial(3) {{< /alternativa >}}
        {{< alternativa >}} fatorial(3) → fatorial(0) → fatorial(1) {{< /alternativa >}}
        {{< solucao letra="A" >}}
        A chamada começa com fatorial(3) e, a cada chamada, o argumento é reduzido em 1 até chegar ao caso base fatorial(1).
        {{< /solucao >}}
        {{< /questao >}}

{{< questao >}}
    Em uma função recursiva, qual é a função do <b>caso base</b>?
    {{< alternativa >}} Realizar a primeira chamada da função. {{< /alternativa >}}
    {{< alternativa >}} Aumentar o valor do parâmetro a cada chamada. {{< /alternativa >}}
    {{< alternativa >}} Determinar uma condição para interromper a recursão. {{< /alternativa >}}
    {{< alternativa >}} Fazer a função chamar outra função. {{< /alternativa >}}
    {{< solucao letra="C" >}}
    O caso base estabelece uma condição na qual a função não realiza uma nova chamada recursiva, interrompendo a recursão.
    {{< /solucao >}}
    {{< /questao >}}


    {{< questao >}}
        Analise o código abaixo. Qual será o resultado?
        {{< code >}}
        def potencia(base, expoente):
           if expoente == 0:
             return 1
           return base * potencia(base, expoente - 1)
        print(potencia(2, 3))
        {{< /code >}}
        {{< alternativa >}} 5 {{< /alternativa >}}
        {{< alternativa >}} 6 {{< /alternativa >}}
        {{< alternativa >}} 8 {{< /alternativa >}}
        {{< alternativa >}} 9 {{< /alternativa >}}
        {{< solucao letra="C" >}}
        A função calcula 2 * 2 * 2 * 1, resultando em 8.
        {{< /solucao >}}
        {{< /questao >}}


        {{< questao >}}
            No código abaixo, o que acontece quando expoente chega a 0?
            {{< code >}}
            def potencia(base, expoente):
                if expoente == 0:
                    return 1
                return base * potencia(base, expoente - 1)
            {{< /code >}}
            {{< alternativa >}} Uma nova chamada é realizada com expoente = -1. {{< /alternativa >}}
            {{< alternativa >}} A função retorna 1 e não realiza outra chamada recursiva. {{< /alternativa >}}
            {{< alternativa >}} A função retorna 0. {{< /alternativa >}}
            {{< alternativa >}} A função reinicia com o valor original do expoente. {{< /alternativa >}}
            {{< solucao letra="B" >}}
            Quando expoente é 0, o caso base é alcançado. A função retorna 1 e encerra a sequência de chamadas.
            {{< /solucao >}}
            {{< /questao >}}
            
{{< /lista-questoes >}}

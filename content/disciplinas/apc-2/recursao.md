---
title: "Recursão"
description: "Técnica em que uma função chama a si mesma para resolver um problema"
slug: recursao
tags:
 - funções
 - recursão
 - python
 - programação
---

A **recursão** é uma técnica de programação na qual uma função chama a **si mesma** para resolver um problema.

Uma função recursiva normalmente divide um problema em problemas menores do mesmo tipo, até atingir uma situação em que a solução pode ser obtida diretamente.

Por exemplo:

```python
def contar(n):
    if n == 0:
        return

    print(n)

    contar(n - 1)
````

Podemos chamar a função:

```python
contar(5)
```

Resultado:

```text
5
4
3
2
1
```

A função `contar()` chama a si mesma com um valor menor:

```python
contar(n - 1)
```

Esse processo continua até que `n` seja igual a `0`.

## Estrutura de uma função recursiva

Uma função recursiva normalmente possui duas partes principais:

* **caso base**;
* **caso recursivo**.

O **caso base** determina quando a função deve parar.

O **caso recursivo** é responsável por realizar uma nova chamada da própria função.

Por exemplo:

```python
def contar(n):

    # caso base
    if n == 0:
        return

    # caso recursivo
    print(n)
    contar(n - 1)
```

Nesse exemplo:

```python
if n == 0:
    return
```

é o **caso base**.

Já:

```python
contar(n - 1)
```

é o **caso recursivo**.

O caso base é fundamental para evitar que a função continue chamando a si mesma indefinidamente.

## Caso base

O **caso base** é a condição que interrompe a recursão.

Considere:

```python
def contar(n):

    if n == 0:
        return

    print(n)
    contar(n - 1)
```

Quando `n` chega a `0`, a função executa:

```python
return
```

e não realiza uma nova chamada.

Podemos visualizar as chamadas:

```text
contar(5)
    contar(4)
        contar(3)
            contar(2)
                contar(1)
                    contar(0)
```

Quando `contar(0)` é executada, o caso base é atingido e a sequência de chamadas é interrompida.

## Caso recursivo

O **caso recursivo** é a parte da função responsável por realizar uma nova chamada da própria função.

Por exemplo:

```python
def contar(n):

    if n == 0:
        return

    print(n)

    contar(n - 1)
```

A instrução:

```python
contar(n - 1)
```

faz com que a função seja chamada novamente.

A cada chamada, o valor de `n` diminui:

```text
contar(5)
contar(4)
contar(3)
contar(2)
contar(1)
contar(0)
```

Quando `n` chega a `0`, o caso base é executado.

## Recursão e funções

Uma função recursiva é uma função comum que possui uma característica adicional: ela pode realizar uma chamada para si mesma.

Por exemplo:

```python
def exemplo(n):

    if n == 0:
        return

    print(n)

    exemplo(n - 1)
```

A chamada:

```python
exemplo(3)
```

produz:

```text
3
2
1
```

As chamadas realizadas são:

```text
exemplo(3)
    exemplo(2)
        exemplo(1)
            exemplo(0)
```

## Contagem crescente

Também podemos utilizar recursão para realizar uma contagem crescente.

Por exemplo:

```python
def contar(n):

    if n > 5:
        return

    print(n)

    contar(n + 1)
```

A chamada:

```python
contar(1)
```

produz:

```text
1
2
3
4
5
```

Nesse caso, o valor utilizado na chamada recursiva aumenta:

```python
contar(n + 1)
```

O caso base é atingido quando `n` fica maior que `5`.

## Fatorial

Um exemplo clássico de recursão é o cálculo do **fatorial**.

O fatorial de um número inteiro positivo `n` é definido como:

```text
n! = n × (n - 1) × (n - 2) × ... × 1
```

Por exemplo:

```text
5! = 5 × 4 × 3 × 2 × 1
```

Portanto:

```text
5! = 120
```

O fatorial também pode ser definido recursivamente:

```text
n! = n × (n - 1)!
```

O caso base é:

```text
0! = 1
```

Podemos transformar essa definição em uma função:

```python
def fatorial(n):

    if n == 0:
        return 1

    return n * fatorial(n - 1)
```

Podemos calcular:

```python
print(fatorial(5))
```

Resultado:

```text
120
```

## Funcionamento do fatorial

Quando executamos:

```python
fatorial(5)
```

a função realiza:

```text
fatorial(5)
5 * fatorial(4)
5 * 4 * fatorial(3)
5 * 4 * 3 * fatorial(2)
5 * 4 * 3 * 2 * fatorial(1)
5 * 4 * 3 * 2 * 1 * fatorial(0)
```

Quando `fatorial(0)` é executado, o caso base retorna `1`.

Assim:

```text
5 * 4 * 3 * 2 * 1 * 1
```

O resultado é:

```text
120
```

Podemos representar o processo da seguinte maneira:

```text
fatorial(5)
    |
    +-- 5 * fatorial(4)
                |
                +-- 4 * fatorial(3)
                            |
                            +-- 3 * fatorial(2)
                                        |
                                        +-- 2 * fatorial(1)
                                                    |
                                                    +-- 1 * fatorial(0)
                                                                |
                                                                +-- 1
```

Depois que o caso base é atingido, os resultados retornam pelas chamadas anteriores.

## Recursão e `return`

Em muitas funções recursivas, o `return` é utilizado tanto para definir o caso base quanto para retornar o resultado da chamada recursiva.

Por exemplo:

```python
def fatorial(n):

    if n == 0:
        return 1

    return n * fatorial(n - 1)
```

Observe que:

```python
return n * fatorial(n - 1)
```

realiza uma chamada recursiva e utiliza o valor retornado por ela.

## Soma dos números

Podemos utilizar recursão para calcular a soma dos números de `1` até `n`.

Por exemplo:

```text
1 + 2 + 3 + 4 + 5 = 15
```

Uma definição recursiva pode ser:

```text
soma(n) = n + soma(n - 1)
```

com o caso base:

```text
soma(0) = 0
```

Em Python:

```python
def soma(n):

    if n == 0:
        return 0

    return n + soma(n - 1)
```

Podemos chamar:

```python
print(soma(5))
```

Resultado:

```text
15
```

As chamadas realizadas são:

```text
soma(5)
5 + soma(4)
5 + 4 + soma(3)
5 + 4 + 3 + soma(2)
5 + 4 + 3 + 2 + soma(1)
5 + 4 + 3 + 2 + 1 + soma(0)
```

Como `soma(0)` retorna `0`, o resultado final é:

```text
15
```

## Potência

A potenciação também pode ser definida de forma recursiva.

Por exemplo:

```text
2⁵ = 2 × 2 × 2 × 2 × 2
```

Podemos observar que:

```text
2⁵ = 2 × 2⁴
```

e:

```text
2⁴ = 2 × 2³
```

Assim, podemos criar:

```python
def potencia(base, expoente):

    if expoente == 0:
        return 1

    return base * potencia(base, expoente - 1)
```

Podemos utilizar:

```python
print(potencia(2, 5))
```

Resultado:

```text
32
```

## Fibonacci

A sequência de **Fibonacci** é outro exemplo clássico de aplicação da recursão.

A sequência começa com:

```text
0, 1, 1, 2, 3, 5, 8, 13, 21, ...
```

Cada termo, a partir do terceiro, é obtido pela soma dos dois termos anteriores:

```text
F(n) = F(n - 1) + F(n - 2)
```

Os casos base podem ser definidos como:

```text
F(0) = 0
F(1) = 1
```

Uma implementação recursiva é:

```python
def fibonacci(n):

    if n == 0:
        return 0

    if n == 1:
        return 1

    return fibonacci(n - 1) + fibonacci(n - 2)
```

Podemos chamar:

```python
print(fibonacci(6))
```

Resultado:

```text
8
```

Isso ocorre porque:

```text
F(6) = F(5) + F(4)
```

e:

```text
F(5) = 5
F(4) = 3
```

Portanto:

```text
F(6) = 5 + 3
F(6) = 8
```

## Recursão em listas

A recursão também pode ser utilizada para processar estruturas como listas.

Por exemplo, podemos criar uma função para imprimir os elementos de uma lista:

```python
def imprimir(lista, indice):

    if indice == len(lista):
        return

    print(lista[indice])

    imprimir(lista, indice + 1)
```

Podemos utilizar:

```python
numeros = [10, 20, 30, 40]

imprimir(numeros, 0)
```

Resultado:

```text
10
20
30
40
```

Nesse caso, o parâmetro `indice` controla qual elemento será processado.

O caso base ocorre quando:

```python
indice == len(lista)
```

Isso significa que todos os elementos já foram processados.

## Soma dos elementos de uma lista

Também podemos calcular recursivamente a soma dos elementos de uma lista.

```python
def soma_lista(lista, indice):

    if indice == len(lista):
        return 0

    return lista[indice] + soma_lista(lista, indice + 1)
```

Podemos utilizar:

```python
numeros = [10, 20, 30, 40]

resultado = soma_lista(numeros, 0)

print(resultado)
```

Resultado:

```text
100
```

O funcionamento pode ser representado como:

```text
soma_lista([10, 20, 30, 40], 0)

10 + soma_lista(..., 1)

10 + 20 + soma_lista(..., 2)

10 + 20 + 30 + soma_lista(..., 3)

10 + 20 + 30 + 40 + soma_lista(..., 4)

10 + 20 + 30 + 40 + 0
```

Resultado:

```text
100
```

## Recursão direta

A **recursão direta** ocorre quando uma função chama diretamente a si mesma.

Por exemplo:

```python
def contar(n):

    if n == 0:
        return

    print(n)

    contar(n - 1)
```

A função `contar()` chama diretamente `contar()`:

```python
contar(n - 1)
```

Esse é o tipo mais comum de recursão apresentado nos exemplos.

## Recursão indireta

Também é possível que uma função chame outra função que, posteriormente, chama a primeira.

Por exemplo:

```python
def funcao_a(n):

    if n <= 0:
        return

    print("A")

    funcao_b(n - 1)


def funcao_b(n):

    if n <= 0:
        return

    print("B")

    funcao_a(n - 1)
```

Podemos chamar:

```python
funcao_a(4)
```

A execução envolve chamadas alternadas:

```text
funcao_a(4)
    funcao_b(3)
        funcao_a(2)
            funcao_b(1)
                funcao_a(0)
```

Nesse caso, a recursão ocorre de forma indireta.

## Pilha de chamadas

Cada chamada de função utiliza uma área de memória chamada **pilha de chamadas** (*call stack*).

Quando uma função chama outra função, uma nova chamada é adicionada à pilha.

Considere:

```python
def contar(n):

    if n == 0:
        return

    print(n)

    contar(n - 1)
```

Ao executar:

```python
contar(3)
```

as chamadas podem ser visualizadas como:

```text
contar(3)
contar(2)
contar(1)
contar(0)
```

Enquanto `contar(0)` está sendo executada, as chamadas anteriores ainda estão aguardando seu retorno.

Quando `contar(0)` termina, a execução retorna para `contar(1)`.

Depois:

```text
contar(0) termina
      ↓
contar(1) continua
      ↓
contar(2) continua
      ↓
contar(3) continua
```

Esse comportamento é importante para compreender como funções recursivas são executadas.

## Recursão sem caso base

Uma função recursiva precisa possuir uma condição que permita interromper as chamadas.

O código abaixo possui um problema:

```python
def contar(n):

    print(n)

    contar(n - 1)
```

Não existe um caso base.

A função continuará realizando chamadas:

```text
contar(5)
contar(4)
contar(3)
contar(2)
contar(1)
contar(0)
contar(-1)
contar(-2)
...
```

Em algum momento, a capacidade da pilha de chamadas será excedida.

Em Python, isso normalmente resulta em uma exceção `RecursionError`.

Por isso, uma função recursiva deve possuir uma condição adequada para interromper a recursão.

## Recursão infinita

Também podemos criar uma recursão que nunca atinge seu caso base.

Por exemplo:

```python
def contar(n):

    if n == 0:
        return

    contar(n + 1)
```

Se chamarmos:

```python
contar(5)
```

o valor aumenta:

```text
5
6
7
8
9
...
```

O valor nunca chegará a `0`.

Consequentemente, a função continuará realizando chamadas até ocorrer um erro de recursão.

O caso recursivo deve, portanto, aproximar o problema de uma condição que permita atingir o caso base.

## Recursão versus repetição

Muitos problemas que podem ser resolvidos com recursão também podem ser resolvidos utilizando estruturas de repetição.

Por exemplo, podemos calcular a soma de `1` até `n` utilizando `for`:

```python
def soma(n):

    resultado = 0

    for i in range(1, n + 1):
        resultado += i

    return resultado
```

Ou utilizando recursão:

```python
def soma(n):

    if n == 0:
        return 0

    return n + soma(n - 1)
```

As duas funções podem produzir o mesmo resultado:

```python
print(soma(5))
```

Resultado:

```text
15
```

A solução iterativa utiliza repetição explícita, enquanto a solução recursiva utiliza chamadas da própria função.

## Quando utilizar recursão

A recursão é especialmente útil quando um problema pode ser naturalmente dividido em **problemas menores do mesmo tipo**.

Alguns exemplos são:

* cálculo de fatoriais;
* sequência de Fibonacci;
* percorrer estruturas hierárquicas;
* percorrer árvores;
* algoritmos de busca;
* algoritmos de ordenação;
* problemas que possuem uma definição naturalmente recursiva.

Entretanto, nem todo problema precisa ser resolvido utilizando recursão.

Quando uma solução iterativa é mais simples e adequada, um `for` ou `while` pode ser uma alternativa melhor.

## Cuidados com a recursão

Ao criar uma função recursiva, é importante verificar:

1. Existe um **caso base**?
2. O caso base pode ser alcançado?
3. A cada chamada, o problema está se aproximando do caso base?
4. A quantidade de chamadas recursivas é adequada?
5. Uma solução iterativa seria mais simples?

Por exemplo:

```python
def fatorial(n):

    if n == 0:
        return 1

    return n * fatorial(n - 1)
```

Nesse caso:

* o caso base é `n == 0`;
* o valor de `n` diminui a cada chamada;
* eventualmente `n` chegará a `0`;
* a função então interromperá a recursão.

## Exemplo completo

O exemplo abaixo calcula o fatorial de um número utilizando recursão:

```python
def fatorial(n):

    if n == 0:
        return 1

    return n * fatorial(n - 1)


numero = 5

resultado = fatorial(numero)

print("Fatorial:", resultado)
```

Resultado:

```text
Fatorial: 120
```

Podemos acompanhar as chamadas:

```text
fatorial(5)
    fatorial(4)
        fatorial(3)
            fatorial(2)
                fatorial(1)
                    fatorial(0)
```

Depois que o caso base é atingido, os valores retornam:

```text
fatorial(0) = 1
fatorial(1) = 1 × 1 = 1
fatorial(2) = 2 × 1 = 2
fatorial(3) = 3 × 2 = 6
fatorial(4) = 4 × 6 = 24
fatorial(5) = 5 × 24 = 120
```

## Principais conceitos

| Conceito          | Descrição                                                          |
| ----------------- | ------------------------------------------------------------------ |
| Recursão          | Técnica em que uma função chama a si mesma                         |
| Caso base         | Condição que interrompe a recursão                                 |
| Caso recursivo    | Parte que realiza uma nova chamada                                 |
| Recursão direta   | Função chama diretamente a si mesma                                |
| Recursão indireta | Funções chamam umas às outras de forma recursiva                   |
| Pilha de chamadas | Estrutura utilizada para controlar as chamadas de funções          |
| `RecursionError`  | Exceção gerada quando a profundidade máxima de recursão é excedida |

## Conclusão

A **recursão** é uma técnica em que uma função chama a si mesma para resolver um problema.

Seus principais conceitos são:

* Uma função recursiva chama a si mesma.
* Uma função recursiva normalmente possui um caso base.
* O caso base determina quando a recursão deve parar.
* O caso recursivo realiza uma nova chamada da função.
* Cada chamada recursiva pode trabalhar com um problema menor.
* O problema deve se aproximar do caso base a cada chamada.
* As chamadas de funções são controladas pela pilha de chamadas.
* A ausência de um caso base pode causar recursão infinita.
* Python pode gerar `RecursionError` quando a profundidade máxima de recursão é excedida.
* Muitos problemas recursivos também podem ser resolvidos utilizando estruturas de repetição.
* A recursão é especialmente útil para problemas naturalmente definidos em termos de subproblemas menores.

Compreender recursão é importante para estudar **algoritmos, estruturas de dados, árvores, buscas, ordenação e outros problemas computacionais**.

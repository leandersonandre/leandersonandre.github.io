---
title: "Repetições"
description: "Estrutura de repetições em Python"
tags:
- python
- while-for
- repetições
- contador
- acumulador
---

A linguagem Python suporta duas principais estruturas de repetição: **while** e **for**.

## While

```python
while True:
    None
```

While é recomendado utilizar quando não se conhece o número exato de repetições.

### Controle de repetições

A quantidade de repetições pode ser controlada de diferentes maneiras. Geralmente a estrutura repete um número fixo de vezes, onde é preciso contar manualmente as iterações. Para isso, é utilizada uma variável chamada **contador**, incrementá-lo  e avaliar se a repetição deve continuar.

#### Contador

A quantidade de repetições (iterações ou *loops*) pode ser contada. Para isso, utiliza-se uma variável chamada de **contador**. Esta variável normalmente é nomeada por apenas uma letra, por exemplo: i, j, k, etc.

```python
# a variável i é utilizada para contar/controlar a quantidade de repetições
# inicialização
i = 0
while i < 10:
    print(i)
    i = i + 1
```

#### Incremento

O contador precisa ser incrementado, ou seja, atualizado a cada repetição da estrutura.

```python
# contador
i = 0
while i < 10:
    print(i)
    # incremento
    i = i + 1
```

#### Decisão

Na estrutura **while**, é definida a condição que irá permitir ou não a próxima iteração.

```python
# contador
i = 0
# decisão - repete enquanto i for menor que 10
while i < 10:
    print(i)
    # incremento
    i = i + 1
```

### Contagem regressiva

Também é possível realizar contagens em ordem decrescente, ou seja, do maior para o menor valor.

```python
i = 10
while i >= 0:
    print(i)
    i = i - 1
````

Neste caso:

* O contador inicia em um valor maior (`10`)
* A condição garante que a repetição continue até `0`
* O contador é decrementado (`i = i - 1`) a cada iteração


### Acumulador

Um **acumulador** é uma variável utilizada para armazenar resultados parciais ao longo das repetições de um laço.

A cada iteração, o acumulador é atualizado com um novo valor, geralmente somando, multiplicando ou concatenando dados.

#### Exemplo (soma)

```python
soma = 0  # acumulador
i = 1

while i <= 5:
    soma = soma + i
    i = i + 1

print(soma)  # resultado: 15
````

#### Exemplo (produto)

```python
produto = 1  # acumulador
i = 1

while i <= 4:
    produto = produto * i
    i = i + 1

print(produto)  # resultado: 24
```

#### Resumo

* O acumulador **guarda resultados parciais**
* É **atualizado a cada repetição**
* Normalmente inicia com:

  * `0` para soma
  * `1` para multiplicação


### Loop infinito

Ocorre quando o laço de repetição nunca é encerrado.

```python
while True:
    print("Repetiu")
```

### Quebra de laço

O laço de repetição pode ser interrompido utilizando a palavra reservada **break**.

```python
while True:
    i = int(input("Digite um número: "))
    if i == 0:
        break
```

### Pulo de laço

O laço de repetição pode ser pulado utilizando a palavra reservada **continue**.

```python
i = 0
while i < 10:
    i = i + 1
    if i == 3:
        continue # pula o valor 3
    print(i)
```

### Cláusula else

Quando a condição do while for falsa, o bloco `else` é executado. O bloco `else` só é executado quando o laço não for interrompido com o comando **break**.

```python
i = 0
while i < 10:
    print(i)
    i = i + 1
else:
    print("Fim do while")
```

## For

A estrutura **for** é utilizada para percorrer sequências ou executar um bloco de código um número definido de vezes.

Em Python, é comum utilizar a função **range()** para gerar sequências numéricas. O comportamento do `range()` segue o padrão: [início, fim), ou seja, inclui o início e exclui o fim.

### Range básico

```python
for i in range(5):
    print(i)
````

Neste caso:

* O `range(5)` gera valores de `0` até `4`
* O valor final **não é incluído**

---

### Range com início (start)

```python
for i in range(2, 6):
    print(i)
```

Neste caso:

* Inicia em `2`
* Vai até `5` (o `6` não é incluído)

---

### Range com início e passo (step)

```python
for i in range(0, 10, 2):
    print(i)
```

Neste caso:

* Inicia em `0`
* Vai até `9`
* Incrementa de `2` em `2`

Saída:

```
0 2 4 6 8
```

---

### Range regressivo (passo negativo)

Também é possível fazer contagem regressiva utilizando um passo negativo.

```python
for i in range(10, 0, -1):
    print(i)
```

Neste caso:

* Inicia em `10`
* Vai até `1` (o `0` não é incluído)
* Decrementa de `1` em `1`

---

### Resumo do range()

```python
range(inicio, fim, passo)
```

* `inicio`: valor inicial (opcional, padrão = 0)
* `fim`: valor final (**não incluído**)
* `passo`: incremento/decremento (opcional, padrão = 1)



### Usando reversed()

Outra forma de percorrer valores em ordem decrescente é utilizando a função `reversed()`.

```python
for i in reversed(range(10)):
    print(i)
````

Neste caso:

* O `range(10)` gera valores de `0` até `9`
* O `reversed()` inverte a ordem → `9` até `0`

---

### Comparação com range regressivo

```python id="v8n2qa"
# usando range com passo negativo
for i in range(9, -1, -1):
    print(i)

# usando reversed
for i in reversed(range(10)):
    print(i)
```

Ambos produzem o mesmo resultado.



### Observação

* `reversed()` não altera a sequência original
* Apenas permite iterar sobre ela em ordem inversa



## Laços aninhados

Laços aninhados ocorrem quando uma estrutura de repetição está dentro de outra. Para cada iteração do laço externo, o laço interno é executado completamente.

### Exemplo básico

```python
for i in range(3):
    for j in range(3):
        print(i, j)
````

Neste exemplo, o laço externo controla o valor de `i`. Para cada valor de `i`, o laço interno percorre todos os valores de `j`, gerando todas as combinações possíveis entre eles.

Saída:

```
0 0
0 1
0 2
1 0
1 1
1 2
2 0
2 1
2 2
```


### Exemplo com while

```python
i = 0
while i < 3:
    j = 0
    while j < 3:
        print(i, j)
        j = j + 1
    i = i + 1
```

O funcionamento é o mesmo do exemplo anterior, mas utilizando a estrutura `while`. Note que o contador interno (`j`) é reiniciado a cada nova iteração do laço externo.


### Exemplo prático (tabuada)

```python
for i in range(1, 6):
    print("--- Tabuada de",i,"---")
    for j in range(1, 10):
        print(i, "x", j, "=", i * j)
```

Esse padrão é comum em problemas que envolvem tabelas, matrizes ou combinações. O laço interno sempre será executado completamente antes que o laço externo avance para o próximo valor.

### Observação

Laços aninhados aumentam a quantidade de execuções rapidamente, pois multiplicam o número de iterações. Por isso, devem ser usados com atenção, principalmente em problemas maiores.




## Quando usar cada estrutura?

* **while**: quando não se sabe quantas vezes o laço será executado.
* **for**: quando se sabe o número de repetições ou ao percorrer uma sequência.

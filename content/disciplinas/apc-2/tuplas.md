---

title: "Tuplas"
description: "Estrutura de dados utilizada para representar sequências de objetos que não podem ser modificadas em Python"
slug: tuplas
tags:
  - estruturas-de-dados
  - tuplas
  - python
  - tuple
---

Uma **tupla** (`tuple`) é uma estrutura de dados utilizada para representar uma **sequência de objetos** em Python.

Assim como uma lista, uma tupla mantém a **ordem dos elementos** e permite que um mesmo objeto apareça **mais de uma vez**.

A principal diferença é que uma tupla é **imutável**: depois de criada, não podemos adicionar, remover ou substituir seus elementos.

Por exemplo:

```python
cores = ("vermelho", "verde", "azul")
```

A tupla representa uma sequência em que cada elemento possui uma posição:

```text
Índice:     0          1        2
          ┌──────────┬────────┬────────┐
Tupla:    │ vermelho │ verde  │ azul   │
          └──────────┴────────┴────────┘
```

## Criação de tuplas

Uma tupla pode ser criada utilizando parênteses:

```python
frutas = ("maçã", "banana", "laranja")
```

Também podemos criar uma tupla sem utilizar os parênteses. O que define a tupla é a **vírgula** entre os elementos:

```python
frutas = "maçã", "banana", "laranja"
```

Podemos criar uma tupla vazia:

```python
tupla = ()
```

Ou utilizando o construtor `tuple()`:

```python
tupla = tuple()
```

Também podemos criar uma tupla a partir de outra sequência:

```python
frutas = tuple(["maçã", "banana", "laranja"])
```

## Tupla com um único elemento

Para criar uma tupla com apenas um elemento, é necessário utilizar uma vírgula:

```python
numero = (10,)
```

Sem a vírgula:

```python
numero = (10)
```

isso não cria uma tupla. Nesse caso, `numero` será um `int`.

Podemos verificar:

```python
print(type((10,)))
print(type((10)))
```

Resultado:

```text
<class 'tuple'>
<class 'int'>
```

## Acesso aos elementos

Assim como nas listas, podemos acessar os elementos de uma tupla utilizando índices.

```python
frutas = ("maçã", "banana", "laranja")

print(frutas[0])
print(frutas[1])
print(frutas[2])
```

Resultado:

```text
maçã
banana
laranja
```

Os índices começam em `0`.

Também podemos utilizar índices negativos:

```python
print(frutas[-1])  # laranja
print(frutas[-2])  # banana
```

## Tuplas são imutáveis

A principal característica de uma tupla é sua **imutabilidade**.

Depois que uma tupla é criada, não podemos modificar diretamente seus elementos.

O código abaixo gera um erro:

```python
frutas = ("maçã", "banana", "laranja")

frutas[1] = "uva"
```

Isso acontece porque não podemos substituir um elemento de uma tupla.

Da mesma forma, não existem métodos como `append()`, `remove()` ou `pop()` para modificar diretamente a tupla.

## Tamanho da tupla

A função `len()` retorna a quantidade de elementos:

```python
frutas = ("maçã", "banana", "laranja")

print(len(frutas))
```

Resultado:

```text
3
```

Assim como nas listas, o tamanho é diferente do maior índice.

Em uma tupla com três elementos:

```text
Índices:    0        1         2
Elementos: A        B         C
```

O tamanho é `3`, mas o último índice é `2`.

## Verificar se um elemento existe

Podemos utilizar `in` para verificar se determinado elemento está presente:

```python
frutas = ("maçã", "banana", "laranja")

print("banana" in frutas)
```

Resultado:

```text
True
```

Também podemos utilizar `not in`:

```python
print("uva" not in frutas)
```

Resultado:

```text
True
```

## Percorrer uma tupla

Podemos percorrer seus elementos utilizando um laço `for`:

```python
frutas = ("maçã", "banana", "laranja")

for fruta in frutas:
    print(fruta)
```

Resultado:

```text
maçã
banana
laranja
```

Quando o índice não é necessário, percorrer diretamente os elementos costuma deixar o código mais simples.

Também podemos percorrer utilizando índices:

```python
for i in range(len(frutas)):
    print(frutas[i])
```

## Slicing

Tuplas também permitem utilizar *slicing* para obter uma parte da sequência.

```python
numeros = (10, 20, 30, 40, 50)

print(numeros[1:4])
```

Resultado:

```text
(20, 30, 40)
```

Também podemos utilizar:

```python
print(numeros[:3])   # (10, 20, 30)
print(numeros[2:])   # (30, 40, 50)
print(numeros[:])    # (10, 20, 30, 40, 50)
```

É possível utilizar um passo:

```python
print(numeros[::2])
```

Resultado:

```text
(10, 30, 50)
```

Também podemos inverter uma tupla:

```python
print(numeros[::-1])
```

Resultado:

```text
(50, 40, 30, 20, 10)
```

## Elementos repetidos

Tuplas permitem elementos repetidos:

```python
notas = (10, 8, 10, 7, 10)

print(notas)
```

Resultado:

```text
(10, 8, 10, 7, 10)
```

Cada ocorrência possui sua própria posição.

## Contar elementos

O método `count()` informa quantas vezes determinado elemento aparece:

```python
notas = (10, 8, 10, 7, 10)

print(notas.count(10))
```

Resultado:

```text
3
```

## Localizar elementos

O método `index()` retorna a posição da primeira ocorrência de determinado elemento:

```python
frutas = ("maçã", "banana", "laranja")

print(frutas.index("banana"))
```

Resultado:

```text
1
```

Se o elemento não existir, `index()` gera uma exceção `ValueError`.

## Desempacotamento

Uma característica muito útil das tuplas é o **desempacotamento**.

Podemos atribuir os elementos de uma tupla diretamente a diferentes variáveis:

```python
pessoa = ("Ana", 25)

nome, idade = pessoa

print(nome)
print(idade)
```

Resultado:

```text
Ana
25
```

A quantidade de variáveis deve corresponder à quantidade de elementos:

```python
pessoa = ("Ana", 25, "Joinville")

nome, idade, cidade = pessoa
```

Agora cada variável recebe um elemento da tupla.

## Troca de valores

O desempacotamento também permite trocar os valores de duas variáveis de forma simples:

```python
a = 10
b = 20

a, b = b, a

print(a)
print(b)
```

Resultado:

```text
20
10
```

Python utiliza uma tupla para realizar essa atribuição de forma prática.

## Retorno de múltiplos valores

Tuplas são frequentemente utilizadas para retornar mais de um valor de uma função.

```python
def calcular(a, b):
    soma = a + b
    produto = a * b

    return soma, produto
```

Podemos receber os valores separadamente:

```python
resultado_soma, resultado_produto = calcular(10, 5)

print(resultado_soma)
print(resultado_produto)
```

Resultado:

```text
15
50
```

A função retorna uma tupla contendo os dois valores.

## Tuplas podem conter diferentes tipos

Uma tupla pode armazenar objetos de diferentes tipos:

```python
dados = ("Ana", 25, 1.68, True)
```

Podemos acessar cada elemento normalmente:

```python
print(dados[0])  # Ana
print(dados[1])  # 25
print(dados[2])  # 1.68
print(dados[3])  # True
```

Também podemos ter tuplas contendo outras tuplas:

```python
ponto = (10, 20)

dados = ("A", ponto)

print(dados)
```

Resultado:

```text
("A", (10, 20))
```

## Tupla contendo uma lista

A imutabilidade da tupla merece uma observação importante.

Uma tupla não permite substituir seus próprios elementos, mas ela pode conter objetos que sejam mutáveis, como uma lista.

Por exemplo:

```python
dados = ("Python", [1, 2, 3])

dados[1].append(4)

print(dados)
```

Resultado:

```text
("Python", [1, 2, 3, 4])
```

A tupla continua contendo os mesmos objetos nas mesmas posições. O que foi alterado foi a lista armazenada dentro dela.

## Tupla ou lista?

A escolha entre `list` e `tuple` depende do que estamos representando.

Uma **lista** é adequada quando precisamos de uma coleção que pode ser modificada:

```python
frutas = ["maçã", "banana", "laranja"]

frutas.append("uva")
```

Uma **tupla** é adequada quando queremos representar uma sequência que não deve ser modificada:

```python
data = (27, 8, 2026)
```

A data possui três componentes em posições definidas e podemos representá-la como uma única estrutura.

Outro exemplo é uma coordenada:

```python
ponto = (10, 20)
```

Nesse caso:

```text
ponto[0] → coordenada X
ponto[1] → coordenada Y
```

## Conversão entre lista e tupla

Podemos transformar uma lista em uma tupla utilizando `tuple()`:

```python
frutas = ["maçã", "banana", "laranja"]

frutas = tuple(frutas)

print(frutas)
```

Resultado:

```text
("maçã", "banana", "laranja")
```

Também podemos transformar uma tupla em uma lista utilizando `list()`:

```python
frutas = ("maçã", "banana", "laranja")

frutas = list(frutas)

print(frutas)
```

Resultado:

```text
["maçã", "banana", "laranja"]
```

Isso pode ser útil quando precisamos modificar temporariamente uma coleção que originalmente foi representada como uma tupla.

## Principais métodos

As tuplas possuem menos métodos de alteração que as listas porque são imutáveis.

Os principais métodos são:

| Método    | Função                                                  |
| --------- | ------------------------------------------------------- |
| `count()` | Conta quantas vezes um elemento aparece                 |
| `index()` | Retorna a posição da primeira ocorrência de um elemento |

Também podemos utilizar funções e operadores comuns:

| Operação | Função                                    |
| -------- | ----------------------------------------- |
| `len()`  | Retorna a quantidade de elementos         |
| `in`     | Verifica se um elemento está presente     |
| `not in` | Verifica se um elemento não está presente |
| `[]`     | Acessa um elemento pelo índice            |
| `[:]`    | Obtém uma parte da tupla                  |

## Exemplo completo

O exemplo abaixo demonstra algumas das principais operações realizadas com uma tupla:

```python
pessoa = ("Ana", 25, "Programadora")

print("Dados:")
print(pessoa)

print("\nNome:")
print(pessoa[0])

print("\nIdade:")
print(pessoa[1])

print("\nQuantidade de elementos:")
print(len(pessoa))

print("\nPossui 25?")
print(25 in pessoa)

print("\nPercorrendo:")
for dado in pessoa:
    print(dado)

nome, idade, profissao = pessoa

print("\nDesempacotamento:")
print(nome)
print(idade)
print(profissao)
```

## Conclusão

A `tuple` é uma estrutura de dados utilizada para representar uma **sequência de objetos imutável**.

Suas principais características são:

* Os elementos possuem uma ordem.
* Cada elemento possui uma posição.
* Os índices começam em `0`.
* Elementos podem ser repetidos.
* A tupla não pode ser modificada diretamente depois de criada.
* Pode armazenar objetos de diferentes tipos.
* Permite acesso por índice e *slicing*.
* Possui os métodos `count()` e `index()`.
* Pode ser utilizada para desempacotamento.
* É frequentemente utilizada para representar conjuntos fixos de valores e retornar múltiplos valores de uma função.

A principal diferença em relação à `list` é simples:

```text
list  → sequência que pode ser modificada
tuple → sequência que não pode ser modificada
```

Compreender tuplas é importante para trabalhar com **dados imutáveis, desempacotamento, retorno de múltiplos valores e representação de estruturas fixas** em Python.

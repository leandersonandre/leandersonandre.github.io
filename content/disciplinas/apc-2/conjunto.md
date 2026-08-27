---

title: "Conjuntos"
description: "Estrutura de dados utilizada para representar coleções de objetos distintos em Python"
slug: conjunto
tags:
  - estruturas-de-dados
  - conjuntos
  - python
  - set
---

Um **conjunto** (`set`) é uma estrutura de dados utilizada para representar uma **coleção de objetos distintos** em Python.

Em um conjunto, um mesmo objeto não pode aparecer mais de uma vez.

Por exemplo:

```python
frutas = {"maçã", "banana", "laranja", "banana"}

print(frutas)
```

Resultado:

```text
{"maçã", "banana", "laranja"}
```

Embora `"banana"` tenha sido informado duas vezes, o conjunto mantém apenas uma ocorrência.

Uma característica importante dos conjuntos é que **a ordem dos elementos não faz parte da informação representada**.

Por isso, não devemos utilizar um conjunto quando precisamos representar uma sequência em que a posição dos elementos é importante.

## Criação de conjuntos

Um conjunto pode ser criado utilizando chaves `{}`:

```python
frutas = {"maçã", "banana", "laranja"}
```

Também podemos criar um conjunto vazio utilizando `set()`:

```python
conjunto = set()
```

É importante observar que:

```python
conjunto = {}
```

cria um **dicionário vazio**, e não um conjunto.

Para criar um conjunto a partir de uma sequência, podemos utilizar `set()`:

```python
frutas = set(["maçã", "banana", "laranja"])
```

Também podemos criar um conjunto a partir de uma string:

```python
letras = set("banana")

print(letras)
```

O resultado será um conjunto contendo os caracteres distintos encontrados na string.

## Elementos repetidos

Conjuntos não armazenam elementos repetidos.

```python
numeros = {1, 2, 3, 2, 1, 3}

print(numeros)
```

Resultado:

```text
{1, 2, 3}
```

Essa característica torna os conjuntos úteis quando queremos trabalhar apenas com **valores distintos**.

Por exemplo:

```python
nomes = ["Ana", "Bruno", "Ana", "Carlos", "Bruno"]

nomes_unicos = set(nomes)

print(nomes_unicos)
```

Agora temos apenas os nomes distintos.

## Adicionar elementos

O método `add()` adiciona um elemento ao conjunto:

```python
frutas = {"maçã", "banana"}

frutas.add("laranja")

print(frutas)
```

O conjunto passa a conter `"laranja"`.

Se tentarmos adicionar um elemento que já existe, nada é alterado:

```python
frutas.add("banana")

print(frutas)
```

O conjunto continua contendo apenas uma ocorrência de `"banana"`.

## Adicionar vários elementos

O método `update()` permite adicionar vários elementos de uma vez:

```python
frutas = {"maçã", "banana"}

frutas.update(["laranja", "uva", "abacaxi"])

print(frutas)
```

Os elementos da sequência são adicionados individualmente ao conjunto.

Também podemos utilizar outro conjunto:

```python
frutas.update({"melancia", "mamão"})
```

## Remover elementos

O método `remove()` remove um elemento específico:

```python
frutas = {"maçã", "banana", "laranja"}

frutas.remove("banana")

print(frutas)
```

Se o elemento não existir, `remove()` gera uma exceção `KeyError`.

Quando queremos remover um elemento sem gerar erro caso ele não exista, podemos utilizar `discard()`:

```python
frutas = {"maçã", "banana", "laranja"}

frutas.discard("uva")

print(frutas)
```

Nesse caso, nada acontece porque `"uva"` não pertence ao conjunto.

## Remover um elemento qualquer

O método `pop()` remove e retorna um elemento do conjunto:

```python
frutas = {"maçã", "banana", "laranja"}

fruta = frutas.pop()

print(fruta)
print(frutas)
```

Como conjuntos não possuem uma ordem definida para acesso, não devemos assumir qual elemento será removido por `pop()`.

## Esvaziar um conjunto

O método `clear()` remove todos os elementos:

```python
frutas = {"maçã", "banana", "laranja"}

frutas.clear()

print(frutas)
```

Resultado:

```text
set()
```

## Tamanho do conjunto

A função `len()` retorna a quantidade de elementos do conjunto:

```python
frutas = {"maçã", "banana", "laranja"}

print(len(frutas))
```

Resultado:

```text
3
```

Como elementos repetidos não são armazenados, eles não são contabilizados:

```python
numeros = {10, 20, 10, 30, 20}

print(len(numeros))
```

Resultado:

```text
3
```

## Verificar se um elemento existe

O operador `in` permite verificar se determinado elemento pertence ao conjunto:

```python
frutas = {"maçã", "banana", "laranja"}

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

## Percorrer um conjunto

Podemos percorrer os elementos de um conjunto utilizando `for`:

```python
frutas = {"maçã", "banana", "laranja"}

for fruta in frutas:
    print(fruta)
```

A ordem em que os elementos serão exibidos não deve ser considerada como parte do conjunto.

## União

A **união** combina os elementos de dois conjuntos, mantendo apenas os elementos distintos.

Podemos utilizar o operador `|`:

```python
frutas1 = {"maçã", "banana", "laranja"}
frutas2 = {"banana", "uva", "abacaxi"}

resultado = frutas1 | frutas2

print(resultado)
```

O resultado contém todos os elementos dos dois conjuntos.

Também podemos utilizar o método `union()`:

```python
resultado = frutas1.union(frutas2)
```

## Interseção

A **interseção** retorna apenas os elementos que pertencem aos dois conjuntos.

Podemos utilizar o operador `&`:

```python
frutas1 = {"maçã", "banana", "laranja"}
frutas2 = {"banana", "laranja", "uva"}

resultado = frutas1 & frutas2

print(resultado)
```

Resultado:

```text
{"banana", "laranja"}
```

Também podemos utilizar:

```python
resultado = frutas1.intersection(frutas2)
```

## Diferença

A **diferença** retorna os elementos que pertencem ao primeiro conjunto, mas não ao segundo.

Podemos utilizar o operador `-`:

```python
frutas1 = {"maçã", "banana", "laranja"}
frutas2 = {"banana", "uva"}

resultado = frutas1 - frutas2

print(resultado)
```

Resultado:

```text
{"maçã", "laranja"}
```

Também podemos utilizar:

```python
resultado = frutas1.difference(frutas2)
```

A direção da operação é importante:

```python
frutas1 - frutas2
```

não representa necessariamente o mesmo resultado que:

```python
frutas2 - frutas1
```

## Diferença simétrica

A **diferença simétrica** retorna os elementos que pertencem a apenas um dos conjuntos.

Podemos utilizar o operador `^`:

```python
frutas1 = {"maçã", "banana", "laranja"}
frutas2 = {"banana", "uva", "abacaxi"}

resultado = frutas1 ^ frutas2

print(resultado)
```

O elemento `"banana"` não aparece no resultado porque pertence aos dois conjuntos.

Também podemos utilizar:

```python
resultado = frutas1.symmetric_difference(frutas2)
```

## Subconjunto

Podemos verificar se todos os elementos de um conjunto pertencem a outro utilizando `issubset()` ou o operador `<=`.

```python
frutas = {"maçã", "banana", "laranja"}
algumas_frutas = {"banana", "laranja"}

print(algumas_frutas.issubset(frutas))
```

Resultado:

```text
True
```

Também podemos escrever:

```python
print(algumas_frutas <= frutas)
```

Nesse caso, `algumas_frutas` é um **subconjunto** de `frutas`.

## Superconjunto

O método `issuperset()` verifica se um conjunto contém todos os elementos de outro:

```python
frutas = {"maçã", "banana", "laranja"}
algumas_frutas = {"banana", "laranja"}

print(frutas.issuperset(algumas_frutas))
```

Resultado:

```text
True
```

Também podemos utilizar `>=`:

```python
print(frutas >= algumas_frutas)
```

## Conjuntos não possuem índices

Diferentemente das listas, conjuntos não possuem posições que possam ser acessadas por índices.

O código abaixo não é válido:

```python
frutas = {"maçã", "banana", "laranja"}

print(frutas[0])
```

Um conjunto não deve ser utilizado quando precisamos acessar elementos pela posição.

Se precisarmos transformar um conjunto em uma lista:

```python
frutas = {"maçã", "banana", "laranja"}

lista = list(frutas)

print(lista)
```

Agora temos uma lista e podemos utilizar índices.

## Elementos de um conjunto

Os elementos de um conjunto precisam ser objetos que possam ser utilizados como elementos de um conjunto.

Por exemplo, podemos utilizar números e strings:

```python
dados = {10, 20, 30, "Python"}
```

Também podemos utilizar tuplas:

```python
dados = {(1, 2), (3, 4)}
```

Por outro lado, uma lista não pode ser diretamente armazenada em um conjunto:

```python
dados = {[1, 2], [3, 4]}
```

Esse código gera uma exceção `TypeError`.

## Exemplo completo

O exemplo abaixo demonstra algumas das principais operações realizadas com conjuntos:

```python
frutas = {"maçã", "banana", "laranja"}

print("Conjunto inicial:")
print(frutas)

frutas.add("uva")

print("\nApós adicionar:")
print(frutas)

frutas.discard("banana")

print("\nApós remover:")
print(frutas)

print("\nPossui laranja?")
print("laranja" in frutas)

outras_frutas = {"laranja", "uva", "abacaxi"}

print("\nUnião:")
print(frutas | outras_frutas)

print("\nInterseção:")
print(frutas & outras_frutas)

print("\nDiferença:")
print(frutas - outras_frutas)
```

## Principais operações e métodos

| Operação ou método       | Função                                                |
| ------------------------ | ----------------------------------------------------- |
| `add()`                  | Adiciona um elemento                                  |
| `update()`               | Adiciona vários elementos                             |
| `remove()`               | Remove um elemento e gera erro se ele não existir     |
| `discard()`              | Remove um elemento sem gerar erro caso ele não exista |
| `pop()`                  | Remove e retorna um elemento                          |
| `clear()`                | Remove todos os elementos                             |
| `len()`                  | Retorna a quantidade de elementos                     |
| `in`                     | Verifica se um elemento pertence ao conjunto          |
| `union()`                | Realiza a união                                       |
| `intersection()`         | Realiza a interseção                                  |
| `difference()`           | Realiza a diferença                                   |
| `symmetric_difference()` | Realiza a diferença simétrica                         |
| `issubset()`             | Verifica se é subconjunto                             |
| `issuperset()`           | Verifica se é superconjunto                           |

Também existem operadores específicos para as operações entre conjuntos:

```text
|  → união
&  → interseção
-  → diferença
^  → diferença simétrica
<= → subconjunto
>= → superconjunto
```

## Exemplo prático

Considere duas turmas de estudantes:

```python
turma_a = {"Ana", "Bruno", "Carlos", "Daniel"}
turma_b = {"Carlos", "Daniel", "Eduardo", "Fernanda"}
```

Podemos descobrir quais estudantes estão nas duas turmas:

```python
print(turma_a & turma_b)
```

Quais estudantes estão em pelo menos uma das turmas:

```python
print(turma_a | turma_b)
```

Quais estudantes estão apenas na primeira turma:

```python
print(turma_a - turma_b)
```

E quais estudantes pertencem a apenas uma das turmas:

```python
print(turma_a ^ turma_b)
```

## Conclusão

O `set` é uma estrutura de dados utilizada para representar uma **coleção de objetos distintos**.

Suas principais características são:

* Não permite elementos duplicados.
* Não possui índices.
* A ordem dos elementos não deve ser considerada.
* Permite adicionar e remover elementos.
* Permite verificar rapidamente a existência de um elemento.
* Pode ser utilizado para eliminar valores duplicados.
* Permite realizar operações matemáticas de conjuntos, como união, interseção e diferença.

O conjunto é especialmente útil quando a informação importante é **quais objetos pertencem a uma coleção**, e não a posição em que eles aparecem.

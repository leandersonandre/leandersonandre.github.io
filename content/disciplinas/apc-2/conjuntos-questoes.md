---
title: "Questões sobre Conjuntos"
description: "Questões sobre a estrutura de dados conjunto em Python"
slug: conjuntos-questoes
tags:
- python
- conjuntos
- questões
---

{{< lista-questoes >}}

{{< questao >}}
O que é um conjunto (`set`) em Python?

{{< alternativa >}} Uma estrutura que armazena elementos em uma sequência ordenada e permite repetição. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que armazena elementos únicos, sem permitir elementos repetidos. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que armazena apenas números inteiros. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que armazena elementos obrigatoriamente em ordem crescente. {{< /alternativa >}}
{{< solucao letra="B" >}}
Um conjunto armazena elementos únicos. Caso um mesmo elemento seja inserido mais de uma vez, ele aparecerá apenas uma vez no conjunto.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é uma característica importante de um conjunto em Python?

{{< alternativa >}} Permite elementos repetidos. {{< /alternativa >}}
{{< alternativa >}} Mantém os elementos sempre em ordem de inserção. {{< /alternativa >}}
{{< alternativa >}} Não permite elementos repetidos. {{< /alternativa >}}
{{< alternativa >}} Permite acessar elementos utilizando índices. {{< /alternativa >}}
{{< solucao letra="C" >}}
Conjuntos não permitem elementos duplicados. Ao adicionar um elemento que já existe, o conjunto permanece com um único elemento.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual das alternativas cria corretamente um conjunto contendo os números `1`, `2` e `3`?

{{< alternativa >}} `numeros = [1, 2, 3]` {{< /alternativa >}}
{{< alternativa >}} `numeros = (1, 2, 3)` {{< /alternativa >}}
{{< alternativa >}} `numeros = {1, 2, 3}` {{< /alternativa >}}
{{< alternativa >}} `numeros = <1, 2, 3>` {{< /alternativa >}}
{{< solucao letra="C" >}}
As chaves `{}` podem ser utilizadas para criar um conjunto com elementos, como em `{1, 2, 3}`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Como criar um conjunto vazio em Python?

{{< alternativa >}} `conjunto = {}` {{< /alternativa >}}
{{< alternativa >}} `conjunto = set()` {{< /alternativa >}}
{{< alternativa >}} `conjunto = []` {{< /alternativa >}}
{{< alternativa >}} `conjunto = ()` {{< /alternativa >}}
{{< solucao letra="B" >}}
`{}` cria um dicionário vazio. Para criar um conjunto vazio, deve-se utilizar `set()`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
frutas = {"maçã", "banana", "laranja"}

print(len(frutas))
{{< /code >}}

{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< solucao letra="C" >}}
O conjunto possui três elementos diferentes. Portanto, `len(frutas)` retorna 3.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
frutas = {"maçã", "banana", "laranja"}

frutas.add("abacaxi")

print(len(frutas))
{{< /code >}}

{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< solucao letra="C" >}}
O conjunto inicialmente possui três elementos. O método `add()` adiciona `"abacaxi"`, passando a ter quatro elementos.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que acontece ao executar o programa.

{{< code >}}
frutas = {"maçã", "banana", "laranja"}

frutas.add("banana")

print(len(frutas))
{{< /code >}}

{{< alternativa >}} O conjunto passa a ter 4 elementos. {{< /alternativa >}}
{{< alternativa >}} O conjunto passa a ter 3 elementos. {{< /alternativa >}}
{{< alternativa >}} O conjunto passa a ter 2 elementos. {{< /alternativa >}}
{{< alternativa >}} Ocorre um erro. {{< /alternativa >}}
{{< solucao letra="B" >}}
`"banana"` já pertence ao conjunto. Como conjuntos não permitem elementos repetidos, nada é acrescentado.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método é utilizado para adicionar um elemento a um conjunto?

{{< alternativa >}} `append()` {{< /alternativa >}}
{{< alternativa >}} `add()` {{< /alternativa >}}
{{< alternativa >}} `insert()` {{< /alternativa >}}
{{< alternativa >}} `push()` {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `add()` é utilizado para adicionar um único elemento a um conjunto.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método pode ser utilizado para remover um elemento específico de um conjunto?

{{< alternativa >}} `remove()` {{< /alternativa >}}
{{< alternativa >}} `delete()` {{< /alternativa >}}
{{< alternativa >}} `popitem()` {{< /alternativa >}}
{{< alternativa >}} `erase()` {{< /alternativa >}}
{{< solucao letra="A" >}}
O método `remove()` remove o elemento especificado do conjunto. Caso o elemento não exista, ocorre um erro.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método pode ser utilizado para remover um elemento de um conjunto sem gerar erro caso ele não exista?

{{< alternativa >}} `remove()` {{< /alternativa >}}
{{< alternativa >}} `discard()` {{< /alternativa >}}
{{< alternativa >}} `delete()` {{< /alternativa >}}
{{< alternativa >}} `popitem()` {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `discard()` remove o elemento caso ele exista. Se o elemento não existir, nenhuma exceção é gerada.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = {10, 20, 30}

numeros.remove(20)

print(20 in numeros)
{{< /code >}}

{{< alternativa >}} True {{< /alternativa >}}
{{< alternativa >}} False {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
O elemento 20 é removido pelo método `remove()`. Portanto, a expressão `20 in numeros` resulta em `False`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que o operador `in` pode ser utilizado para verificar em um conjunto?

{{< alternativa >}} Se um elemento pertence ao conjunto. {{< /alternativa >}}
{{< alternativa >}} A posição de um elemento no conjunto. {{< /alternativa >}}
{{< alternativa >}} A quantidade de elementos do conjunto. {{< /alternativa >}}
{{< alternativa >}} A ordem dos elementos do conjunto. {{< /alternativa >}}
{{< solucao letra="A" >}}
O operador `in` verifica se determinado elemento pertence ao conjunto, retornando `True` ou `False`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
frutas = {"maçã", "banana", "laranja"}

print("banana" in frutas)
{{< /code >}}

{{< alternativa >}} True {{< /alternativa >}}
{{< alternativa >}} False {{< /alternativa >}}
{{< alternativa >}} banana {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="A" >}}
A fruta `"banana"` pertence ao conjunto, portanto a expressão resulta em `True`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
frutas = {"maçã", "banana", "laranja"}

print("uva" not in frutas)
{{< /code >}}

{{< alternativa >}} True {{< /alternativa >}}
{{< alternativa >}} False {{< /alternativa >}}
{{< alternativa >}} uva {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="A" >}}
A fruta `"uva"` não pertence ao conjunto. Portanto, `not in` resulta em `True`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = {1, 2, 2, 3, 3, 3}

print(len(numeros))
{{< /code >}}

{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 6 {{< /alternativa >}}
{{< solucao letra="A" >}}
Os elementos repetidos são eliminados no conjunto. O conjunto resultante possui apenas `{1, 2, 3}`, totalizando três elementos.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = {1, 2, 3}

numeros.add(4)
numeros.add(2)

print(len(numeros))
{{< /code >}}

{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 6 {{< /alternativa >}}
{{< solucao letra="B" >}}
O conjunto começa com três elementos. O 4 é adicionado, mas o 2 já existe e não é duplicado. Portanto, ficam quatro elementos.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual operação representa a união de dois conjuntos?

{{< alternativa >}} `&` {{< /alternativa >}}
{{< alternativa >}} `|` {{< /alternativa >}}
{{< alternativa >}} `-` {{< /alternativa >}}
{{< alternativa >}} `*` {{< /alternativa >}}
{{< solucao letra="B" >}}
O operador `|` representa a união de conjuntos, reunindo os elementos dos dois conjuntos sem repetir valores.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
a = {1, 2, 3}
b = {3, 4, 5}

print(a | b)
{{< /code >}}

{{< alternativa >}} {3} {{< /alternativa >}}
{{< alternativa >}} {1, 2} {{< /alternativa >}}
{{< alternativa >}} {1, 2, 3, 4, 5} {{< /alternativa >}}
{{< alternativa >}} {4, 5} {{< /alternativa >}}
{{< solucao letra="C" >}}
A união reúne todos os elementos dos dois conjuntos. O elemento 3 aparece nos dois, mas aparece apenas uma vez no resultado.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual operação representa a interseção de dois conjuntos?

{{< alternativa >}} `|` {{< /alternativa >}}
{{< alternativa >}} `&` {{< /alternativa >}}
{{< alternativa >}} `-` {{< /alternativa >}}
{{< alternativa >}} `+` {{< /alternativa >}}
{{< solucao letra="B" >}}
O operador `&` representa a interseção, retornando os elementos que pertencem aos dois conjuntos.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
a = {1, 2, 3}
b = {3, 4, 5}

print(a & b)
{{< /code >}}

{{< alternativa >}} {1, 2, 3} {{< /alternativa >}}
{{< alternativa >}} {3} {{< /alternativa >}}
{{< alternativa >}} {4, 5} {{< /alternativa >}}
{{< alternativa >}} {} {{< /alternativa >}}
{{< solucao letra="B" >}}
O único elemento que pertence aos dois conjuntos é 3. Portanto, a interseção é `{3}`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual operação retorna os elementos que pertencem ao primeiro conjunto, mas não pertencem ao segundo?

{{< alternativa >}} União. {{< /alternativa >}}
{{< alternativa >}} Interseção. {{< /alternativa >}}
{{< alternativa >}} Diferença. {{< /alternativa >}}
{{< alternativa >}} Igualdade. {{< /alternativa >}}
{{< solucao letra="C" >}}
A diferença entre conjuntos retorna os elementos que estão no primeiro conjunto e não estão no segundo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
a = {1, 2, 3}
b = {3, 4, 5}

print(a - b)
{{< /code >}}

{{< alternativa >}} {1, 2} {{< /alternativa >}}
{{< alternativa >}} {3} {{< /alternativa >}}
{{< alternativa >}} {4, 5} {{< /alternativa >}}
{{< alternativa >}} {1, 2, 3, 4, 5} {{< /alternativa >}}
{{< solucao letra="A" >}}
A diferença `a - b` retorna os elementos que estão em `a` e não estão em `b`. Portanto, o resultado é `{1, 2}`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual operador pode ser utilizado para verificar se dois conjuntos possuem exatamente os mesmos elementos?

{{< alternativa >}} `=` {{< /alternativa >}}
{{< alternativa >}} `==` {{< /alternativa >}}
{{< alternativa >}} `in` {{< /alternativa >}}
{{< alternativa >}} `is` {{< /alternativa >}}
{{< solucao letra="B" >}}
O operador `==` verifica se dois conjuntos possuem os mesmos elementos.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
a = {1, 2, 3}
b = {3, 2, 1}

print(a == b)
{{< /code >}}

{{< alternativa >}} True {{< /alternativa >}}
{{< alternativa >}} False {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="A" >}}
Os dois conjuntos possuem exatamente os mesmos elementos. A ordem em que os elementos aparecem não interfere na igualdade entre conjuntos.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = {1, 2, 3, 4}

for numero in numeros:
    print(numero)
{{< /code >}}

{{< alternativa >}} Os números serão necessariamente impressos em ordem crescente. {{< /alternativa >}}
{{< alternativa >}} Os números serão necessariamente impressos na ordem em que foram adicionados. {{< /alternativa >}}
{{< alternativa >}} Cada elemento do conjunto será percorrido uma vez, mas não se deve depender de uma ordem específica. {{< /alternativa >}}
{{< alternativa >}} Apenas o primeiro elemento será impresso. {{< /alternativa >}}
{{< solucao letra="C" >}}
Conjuntos não devem ser utilizados supondo uma ordem específica dos elementos. O `for` percorre os elementos do conjunto, mas a ordem não deve ser considerada.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Por que não é possível acessar diretamente um elemento de um conjunto utilizando um índice?

{{< alternativa >}} Porque conjuntos armazenam apenas números. {{< /alternativa >}}
{{< alternativa >}} Porque conjuntos não possuem uma ordem de elementos para indexação. {{< /alternativa >}}
{{< alternativa >}} Porque conjuntos possuem índices começando em 1. {{< /alternativa >}}
{{< alternativa >}} Porque conjuntos são Strings. {{< /alternativa >}}
{{< solucao letra="B" >}}
Conjuntos não possuem uma ordem definida para acesso por índice. Por isso, expressões como `conjunto[0]` não são utilizadas para acessar seus elementos.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique o que acontece.

{{< code >}}
frutas = {"maçã", "banana", "laranja"}

print(frutas[0])
{{< /code >}}

{{< alternativa >}} Será impressa a primeira fruta. {{< /alternativa >}}
{{< alternativa >}} Será impressa a última fruta. {{< /alternativa >}}
{{< alternativa >}} Será impressa uma fruta aleatória. {{< /alternativa >}}
{{< alternativa >}} Ocorre um erro. {{< /alternativa >}}
{{< solucao letra="D" >}}
Conjuntos não possuem acesso por índice. Portanto, tentar utilizar `frutas[0]` gera um erro.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método pode ser utilizado para remover todos os elementos de um conjunto?

{{< alternativa >}} `remove()` {{< /alternativa >}}
{{< alternativa >}} `clear()` {{< /alternativa >}}
{{< alternativa >}} `delete()` {{< /alternativa >}}
{{< alternativa >}} `empty()` {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `clear()` remove todos os elementos do conjunto, deixando-o vazio.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = {1, 2, 3}

numeros.clear()

print(len(numeros))
{{< /code >}}

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< solucao letra="A" >}}
`clear()` remove todos os elementos do conjunto. Portanto, sua quantidade de elementos passa a ser 0.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere os conjuntos abaixo:

{{< code >}}
alunos = {"Ana", "Bruno", "Carlos"}
aprovados = {"Ana", "Carlos", "Daniel"}
{{< /code >}}

Qual operação retorna os alunos que estão nos dois conjuntos?

{{< alternativa >}} `alunos | aprovados` {{< /alternativa >}}
{{< alternativa >}} `alunos & aprovados` {{< /alternativa >}}
{{< alternativa >}} `alunos - aprovados` {{< /alternativa >}}
{{< alternativa >}} `aprovados - alunos` {{< /alternativa >}}
{{< solucao letra="B" >}}
A interseção `&` retorna os elementos que pertencem aos dois conjuntos. Nesse caso, o resultado contém `"Ana"` e `"Carlos"`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere os conjuntos abaixo:

{{< code >}}
turma_a = {"Ana", "Bruno", "Carlos"}
turma_b = {"Carlos", "Daniel", "Eduardo"}
{{< /code >}}

Quais alunos estão somente na `turma_a`?

{{< alternativa >}} Ana e Bruno {{< /alternativa >}}
{{< alternativa >}} Carlos {{< /alternativa >}}
{{< alternativa >}} Daniel e Eduardo {{< /alternativa >}}
{{< alternativa >}} Ana, Bruno, Carlos, Daniel e Eduardo {{< /alternativa >}}
{{< solucao letra="A" >}}
A expressão `turma_a - turma_b` retorna os elementos que estão em `turma_a` e não estão em `turma_b`. O resultado contém Ana e Bruno.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere os conjuntos abaixo:

{{< code >}}
a = {1, 2}
b = {1, 2, 3}
{{< /code >}}

Qual afirmação está correta?

{{< alternativa >}} `a` é um subconjunto de `b`. {{< /alternativa >}}
{{< alternativa >}} `b` é um subconjunto de `a`. {{< /alternativa >}}
{{< alternativa >}} Os conjuntos são iguais. {{< /alternativa >}}
{{< alternativa >}} Os conjuntos não possuem elementos em comum. {{< /alternativa >}}
{{< solucao letra="A" >}}
Todos os elementos de `a` também pertencem a `b`. Portanto, `a` é um subconjunto de `b`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método pode ser utilizado para verificar se um conjunto é subconjunto de outro?

{{< alternativa >}} `issubset()` {{< /alternativa >}}
{{< alternativa >}} `issubsetof()` {{< /alternativa >}}
{{< alternativa >}} `subset()` {{< /alternativa >}}
{{< alternativa >}} `contains()` {{< /alternativa >}}
{{< solucao letra="A" >}}
O método `issubset()` verifica se todos os elementos de um conjunto também pertencem a outro conjunto.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
a = {1, 2}
b = {1, 2, 3}

print(a.issubset(b))
{{< /code >}}

{{< alternativa >}} True {{< /alternativa >}}
{{< alternativa >}} False {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< solucao letra="A" >}}
Todos os elementos de `a` também estão presentes em `b`. Portanto, `a.issubset(b)` retorna `True`.
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

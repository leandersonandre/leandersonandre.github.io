---
title: "Questões sobre Tuplas"
description: "Questões sobre a estrutura de dados tupla em Python"
slug: tuplas-questoes
tags:
- python
- tuplas
- questões
---

{{< lista-questoes >}}

{{< questao >}}
O que é uma tupla em Python?

{{< alternativa >}} Uma estrutura que armazena uma sequência de objetos que pode ser alterada livremente. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que armazena uma sequência de objetos que não pode ser alterada após sua criação. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que armazena apenas números. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que não permite elementos repetidos. {{< /alternativa >}}
{{< solucao letra="B" >}}
Uma tupla representa uma sequência de objetos que, após criada, não pode ter seus elementos alterados.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual das alternativas cria uma tupla contendo os números `1`, `2` e `3`?

{{< alternativa >}} `numeros = [1, 2, 3]` {{< /alternativa >}}
{{< alternativa >}} `numeros = {1, 2, 3}` {{< /alternativa >}}
{{< alternativa >}} `numeros = (1, 2, 3)` {{< /alternativa >}}
{{< alternativa >}} `numeros = <1, 2, 3>` {{< /alternativa >}}
{{< solucao letra="C" >}}
Os parênteses podem ser utilizados para criar uma tupla, como em `(1, 2, 3)`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Uma tupla pode possuir elementos repetidos?

{{< alternativa >}} Não, uma tupla aceita apenas elementos diferentes. {{< /alternativa >}}
{{< alternativa >}} Sim, uma tupla pode possuir elementos repetidos. {{< /alternativa >}}
{{< alternativa >}} Apenas quando os elementos são números. {{< /alternativa >}}
{{< alternativa >}} Apenas quando os elementos são Strings. {{< /alternativa >}}
{{< solucao letra="B" >}}
Tuplas podem possuir elementos repetidos. Por exemplo, `(10, 20, 10)` é uma tupla válida.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
frutas = ("maçã", "banana", "laranja")

print(len(frutas))
{{< /code >}}

{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< solucao letra="C" >}}
A tupla possui três elementos. Portanto, `len(frutas)` retorna 3.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = (10, 20, 30, 40)

print(numeros[0])
{{< /code >}}

{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 30 {{< /alternativa >}}
{{< alternativa >}} 40 {{< /alternativa >}}
{{< solucao letra="A" >}}
O índice 0 representa o primeiro elemento da tupla. Portanto, o resultado é 10.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = (10, 20, 30, 40)

print(numeros[-1])
{{< /code >}}

{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 30 {{< /alternativa >}}
{{< alternativa >}} 40 {{< /alternativa >}}
{{< solucao letra="D" >}}
O índice `-1` representa o último elemento da tupla. Portanto, o resultado é 40.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
frutas = ("maçã", "banana", "laranja")

print(frutas[1])
{{< /code >}}

{{< alternativa >}} maçã {{< /alternativa >}}
{{< alternativa >}} banana {{< /alternativa >}}
{{< alternativa >}} laranja {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
Os índices começam em 0. Portanto, o elemento no índice 1 é `"banana"`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = (1, 2, 3, 4, 5)

print(numeros[1:4])
{{< /code >}}

{{< alternativa >}} `(1, 2, 3)` {{< /alternativa >}}
{{< alternativa >}} `(2, 3, 4)` {{< /alternativa >}}
{{< alternativa >}} `(2, 3, 4, 5)` {{< /alternativa >}}
{{< alternativa >}} `(1, 2, 3, 4)` {{< /alternativa >}}
{{< solucao letra="B" >}}
O fatiamento começa no índice 1 e termina antes do índice 4. Portanto, o resultado é `(2, 3, 4)`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = (1, 2, 3, 4, 5)

print(numeros[:3])
{{< /code >}}

{{< alternativa >}} `(1, 2, 3)` {{< /alternativa >}}
{{< alternativa >}} `(2, 3, 4)` {{< /alternativa >}}
{{< alternativa >}} `(1, 2, 3, 4)` {{< /alternativa >}}
{{< alternativa >}} `(3, 4, 5)` {{< /alternativa >}}
{{< solucao letra="A" >}}
Quando o início não é informado, o fatiamento começa no primeiro elemento e termina antes do índice 3.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = (1, 2, 3, 4, 5)

print(numeros[2:])
{{< /code >}}

{{< alternativa >}} `(1, 2)` {{< /alternativa >}}
{{< alternativa >}} `(2, 3, 4, 5)` {{< /alternativa >}}
{{< alternativa >}} `(3, 4, 5)` {{< /alternativa >}}
{{< alternativa >}} `(3, 4)` {{< /alternativa >}}
{{< solucao letra="C" >}}
Quando o final não é informado, o fatiamento continua até o último elemento. O índice 2 corresponde ao número 3.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que acontece ao executar o programa.

{{< code >}}
numeros = (10, 20, 30)

numeros[0] = 100
{{< /code >}}

{{< alternativa >}} O primeiro elemento passa a ser 100. {{< /alternativa >}}
{{< alternativa >}} A tupla passa a ter quatro elementos. {{< /alternativa >}}
{{< alternativa >}} Ocorre um erro. {{< /alternativa >}}
{{< alternativa >}} Nada acontece. {{< /alternativa >}}
{{< solucao letra="C" >}}
Tuplas são imutáveis. Seus elementos não podem ser alterados após a criação, portanto essa atribuição gera um erro.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual alternativa apresenta uma operação que pode ser realizada com uma tupla?

{{< alternativa >}} Alterar um elemento utilizando seu índice. {{< /alternativa >}}
{{< alternativa >}} Remover um elemento específico da tupla. {{< /alternativa >}}
{{< alternativa >}} Acessar um elemento utilizando seu índice. {{< /alternativa >}}
{{< alternativa >}} Utilizar `append()` para adicionar um elemento. {{< /alternativa >}}
{{< solucao letra="C" >}}
Embora seja imutável, uma tupla permite acessar seus elementos por meio de índices.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
cores = ("azul", "verde", "vermelho")

print("verde" in cores)
{{< /code >}}

{{< alternativa >}} True {{< /alternativa >}}
{{< alternativa >}} False {{< /alternativa >}}
{{< alternativa >}} verde {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="A" >}}
O elemento `"verde"` pertence à tupla. Portanto, a expressão `in` retorna `True`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
cores = ("azul", "verde", "vermelho")

print("amarelo" in cores)
{{< /code >}}

{{< alternativa >}} True {{< /alternativa >}}
{{< alternativa >}} False {{< /alternativa >}}
{{< alternativa >}} amarelo {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
O elemento `"amarelo"` não pertence à tupla. Portanto, a expressão `in` retorna `False`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método pode ser utilizado para contar quantas vezes um elemento aparece em uma tupla?

{{< alternativa >}} `count()` {{< /alternativa >}}
{{< alternativa >}} `length()` {{< /alternativa >}}
{{< alternativa >}} `size()` {{< /alternativa >}}
{{< alternativa >}} `find()` {{< /alternativa >}}
{{< solucao letra="A" >}}
O método `count()` retorna a quantidade de vezes que determinado elemento aparece na tupla.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
numeros = (10, 20, 10, 30, 10)

print(numeros.count(10))
{{< /code >}}

{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< solucao letra="C" >}}
O número 10 aparece três vezes na tupla. Portanto, `count(10)` retorna 3.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método retorna o índice da primeira ocorrência de um elemento em uma tupla?

{{< alternativa >}} `index()` {{< /alternativa >}}
{{< alternativa >}} `find()` {{< /alternativa >}}
{{< alternativa >}} `position()` {{< /alternativa >}}
{{< alternativa >}} `search()` {{< /alternativa >}}
{{< solucao letra="A" >}}
O método `index()` retorna o índice da primeira ocorrência do elemento informado.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
frutas = ("maçã", "banana", "laranja", "banana")

print(frutas.index("banana"))
{{< /code >}}

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< solucao letra="B" >}}
`"banana"` aparece nos índices 1 e 3. O método `index()` retorna o índice da primeira ocorrência, que é 1.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
dados = ("Ana", 20, 8.5)

nome, idade, nota = dados

print(nome)
{{< /code >}}

{{< alternativa >}} Ana {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 8.5 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="A" >}}
A tupla possui três elementos e eles são atribuídos, na mesma ordem, às variáveis `nome`, `idade` e `nota`. Portanto, `nome` recebe `"Ana"`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
dados = ("Ana", 20, 8.5)

nome, idade, nota = dados

print(nota)
{{< /code >}}

{{< alternativa >}} Ana {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 8.5 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="C" >}}
A variável `nota` recebe o terceiro elemento da tupla, que é `8.5`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
pessoa = ("João", 25)

nome, idade = pessoa

print(nome, idade)
{{< /code >}}

{{< alternativa >}} João {{< /alternativa >}}
{{< alternativa >}} 25 {{< /alternativa >}}
{{< alternativa >}} João 25 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="C" >}}
Os dois elementos da tupla são atribuídos às duas variáveis na mesma ordem. Portanto, o programa imprime `João 25`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a diferença principal entre uma lista e uma tupla em Python?

{{< alternativa >}} Listas permitem elementos repetidos e tuplas não. {{< /alternativa >}}
{{< alternativa >}} Tuplas permitem elementos repetidos e listas não. {{< /alternativa >}}
{{< alternativa >}} Listas são mutáveis e tuplas são imutáveis. {{< /alternativa >}}
{{< alternativa >}} Tuplas podem armazenar apenas números. {{< /alternativa >}}
{{< solucao letra="C" >}}
A principal diferença é que listas podem ser modificadas após sua criação, enquanto tuplas são imutáveis.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
numeros = (1, 2, 3)

for numero in numeros:
    print(numero)
{{< /code >}}

{{< alternativa >}} Apenas o primeiro elemento será impresso. {{< /alternativa >}}
{{< alternativa >}} Todos os elementos da tupla serão percorridos. {{< /alternativa >}}
{{< alternativa >}} Ocorre um erro porque tuplas não podem ser percorridas. {{< /alternativa >}}
{{< alternativa >}} Apenas o último elemento será impresso. {{< /alternativa >}}
{{< solucao letra="B" >}}
Tuplas são sequências e podem ser percorridas utilizando um `for`. Nesse caso, os três elementos serão percorridos.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
numeros = (1, 2, 3)

print(numeros + (4, 5))
{{< /code >}}

{{< alternativa >}} `(1, 2, 3)` {{< /alternativa >}}
{{< alternativa >}} `(4, 5)` {{< /alternativa >}}
{{< alternativa >}} `(1, 2, 3, 4, 5)` {{< /alternativa >}}
{{< alternativa >}} Ocorre um erro. {{< /alternativa >}}
{{< solucao letra="C" >}}
O operador `+` pode ser utilizado para concatenar tuplas. O resultado é uma nova tupla contendo os elementos das duas tuplas.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
numeros = (1, 2, 3)

print(numeros * 2)
{{< /code >}}

{{< alternativa >}} `(1, 2, 3, 2)` {{< /alternativa >}}
{{< alternativa >}} `(2, 4, 6)` {{< /alternativa >}}
{{< alternativa >}} `(1, 2, 3, 1, 2, 3)` {{< /alternativa >}}
{{< alternativa >}} Ocorre um erro. {{< /alternativa >}}
{{< solucao letra="C" >}}
O operador `*` com um inteiro repete os elementos da tupla. Portanto, a tupla é repetida duas vezes.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a forma correta de criar uma tupla com apenas um elemento?

{{< alternativa >}} `tupla = (10)` {{< /alternativa >}}
{{< alternativa >}} `tupla = [10]` {{< /alternativa >}}
{{< alternativa >}} `tupla = (10,)` {{< /alternativa >}}
{{< alternativa >}} `tupla = {10}` {{< /alternativa >}}
{{< solucao letra="C" >}}
Para criar uma tupla com um único elemento, é necessário utilizar uma vírgula: `(10,)`. Sem a vírgula, `(10)` é apenas uma expressão entre parênteses.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o tipo de dado armazenado na variável.

{{< code >}}
dados = (10)
print(type(dados))
{{< /code >}}

{{< alternativa >}} `tuple` {{< /alternativa >}}
{{< alternativa >}} `list` {{< /alternativa >}}
{{< alternativa >}} `int` {{< /alternativa >}}
{{< alternativa >}} `set` {{< /alternativa >}}
{{< solucao letra="C" >}}
`(10)` não cria uma tupla. Os parênteses apenas agrupam o número, portanto `dados` é um `int`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o tipo de dado armazenado na variável.

{{< code >}}
dados = (10,)
print(type(dados))
{{< /code >}}

{{< alternativa >}} `tuple` {{< /alternativa >}}
{{< alternativa >}} `list` {{< /alternativa >}}
{{< alternativa >}} `int` {{< /alternativa >}}
{{< alternativa >}} `set` {{< /alternativa >}}
{{< solucao letra="A" >}}
A vírgula indica que `(10,)` é uma tupla com um único elemento.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
numeros = (10, 20, 30)

print(numeros[-2])
{{< /code >}}

{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 30 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
O índice `-1` representa o último elemento e `-2` representa o penúltimo. Portanto, o resultado é 20.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que acontece.

{{< code >}}
frutas = ("maçã", "banana", "laranja")

frutas.append("uva")
{{< /code >}}

{{< alternativa >}} `"uva"` é adicionada ao final da tupla. {{< /alternativa >}}
{{< alternativa >}} `"uva"` é adicionada ao início da tupla. {{< /alternativa >}}
{{< alternativa >}} Ocorre um erro. {{< /alternativa >}}
{{< alternativa >}} A tupla é transformada automaticamente em uma lista. {{< /alternativa >}}
{{< solucao letra="C" >}}
Tuplas não possuem o método `append()`. Como são imutáveis, não é possível adicionar elementos diretamente a uma tupla.
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

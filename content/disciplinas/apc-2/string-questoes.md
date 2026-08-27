---
title: "Questões sobre Strings"
description: "Questões sobre Strings e seus principais métodos em Python"
slug: strings-questoes
tags:
- python
- strings
- questões
---

{{< lista-questoes >}}

{{< questao >}}
O que é uma <b>String</b> em Python?

{{< alternativa >}} Uma sequência de caracteres. {{< /alternativa >}}
{{< alternativa >}} Uma sequência que armazena apenas números inteiros. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que armazena vários valores sem ordem. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura utilizada exclusivamente para cálculos matemáticos. {{< /alternativa >}}
{{< solucao letra="A" >}}
Uma String representa uma sequência de caracteres, como textos, palavras e frases.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual das alternativas representa corretamente uma String em Python?

{{< alternativa >}} `nome = João` {{< /alternativa >}}
{{< alternativa >}} `nome = "João"` {{< /alternativa >}}
{{< alternativa >}} `nome = [João]` {{< /alternativa >}}
{{< alternativa >}} `nome = (João)` {{< /alternativa >}}
{{< solucao letra="B" >}}
Strings podem ser delimitadas por aspas simples ou duplas. Nesse caso, `"João"` é uma String.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é o índice do primeiro caractere de uma String em Python?

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} -1 {{< /alternativa >}}
{{< alternativa >}} Depende do tamanho da String. {{< /alternativa >}}
{{< solucao letra="A" >}}
Assim como ocorre com listas, os índices de uma String começam em 0.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "Python"

print(texto[0])
{{< /code >}}

{{< alternativa >}} P {{< /alternativa >}}
{{< alternativa >}} y {{< /alternativa >}}
{{< alternativa >}} n {{< /alternativa >}}
{{< alternativa >}} Python {{< /alternativa >}}
{{< solucao letra="A" >}}
O índice 0 representa o primeiro caractere da String. Portanto, será impresso `P`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "Python"

print(texto[2])
{{< /code >}}

{{< alternativa >}} P {{< /alternativa >}}
{{< alternativa >}} y {{< /alternativa >}}
{{< alternativa >}} t {{< /alternativa >}}
{{< alternativa >}} h {{< /alternativa >}}
{{< solucao letra="C" >}}
Os caracteres possuem os índices `0: P`, `1: y`, `2: t`. Portanto, será impresso `t`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "Python"

print(texto[-1])
{{< /code >}}

{{< alternativa >}} P {{< /alternativa >}}
{{< alternativa >}} n {{< /alternativa >}}
{{< alternativa >}} o {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
O índice `-1` representa o último caractere da String. Portanto, será impresso `n`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que a função `len()` retorna quando utilizada com uma String?

{{< alternativa >}} O primeiro caractere da String. {{< /alternativa >}}
{{< alternativa >}} O último caractere da String. {{< /alternativa >}}
{{< alternativa >}} A quantidade de caracteres da String. {{< /alternativa >}}
{{< alternativa >}} A String convertida para número. {{< /alternativa >}}
{{< solucao letra="C" >}}
A função `len()` retorna a quantidade de caracteres existentes na String.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "Python"

print(len(texto))
{{< /code >}}

{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 6 {{< /alternativa >}}
{{< alternativa >}} 7 {{< /alternativa >}}
{{< alternativa >}} 0 {{< /alternativa >}}
{{< solucao letra="B" >}}
A palavra `"Python"` possui 6 caracteres: P, y, t, h, o e n.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método transforma todos os caracteres de uma String em letras maiúsculas?

{{< alternativa >}} `lower()` {{< /alternativa >}}
{{< alternativa >}} `upper()` {{< /alternativa >}}
{{< alternativa >}} `capitalize()` {{< /alternativa >}}
{{< alternativa >}} `title()` {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `upper()` retorna uma nova String com os caracteres em letras maiúsculas.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "python"

print(texto.upper())
{{< /code >}}

{{< alternativa >}} python {{< /alternativa >}}
{{< alternativa >}} Python {{< /alternativa >}}
{{< alternativa >}} PYTHON {{< /alternativa >}}
{{< alternativa >}} Python. {{< /alternativa >}}
{{< solucao letra="C" >}}
O método `upper()` transforma os caracteres da String em letras maiúsculas.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método transforma todos os caracteres de uma String em letras minúsculas?

{{< alternativa >}} `lower()` {{< /alternativa >}}
{{< alternativa >}} `upper()` {{< /alternativa >}}
{{< alternativa >}} `capitalize()` {{< /alternativa >}}
{{< alternativa >}} `title()` {{< /alternativa >}}
{{< solucao letra="A" >}}
O método `lower()` retorna uma nova String com os caracteres em letras minúsculas.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "PYTHON"

print(texto.lower())
{{< /code >}}

{{< alternativa >}} PYTHON {{< /alternativa >}}
{{< alternativa >}} Python {{< /alternativa >}}
{{< alternativa >}} python {{< /alternativa >}}
{{< alternativa >}} python. {{< /alternativa >}}
{{< solucao letra="C" >}}
O método `lower()` transforma todos os caracteres em letras minúsculas.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método coloca a primeira letra da String em maiúscula e as demais em minúsculas?

{{< alternativa >}} `upper()` {{< /alternativa >}}
{{< alternativa >}} `lower()` {{< /alternativa >}}
{{< alternativa >}} `capitalize()` {{< /alternativa >}}
{{< alternativa >}} `replace()` {{< /alternativa >}}
{{< solucao letra="C" >}}
O método `capitalize()` transforma o primeiro caractere em maiúsculo e os demais em minúsculo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "python"

print(texto.capitalize())
{{< /code >}}

{{< alternativa >}} python {{< /alternativa >}}
{{< alternativa >}} Python {{< /alternativa >}}
{{< alternativa >}} PYTHON {{< /alternativa >}}
{{< alternativa >}} PYthon {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `capitalize()` transforma a primeira letra em maiúscula e as demais em minúsculas.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método pode ser utilizado para substituir uma parte de uma String por outra?

{{< alternativa >}} `split()` {{< /alternativa >}}
{{< alternativa >}} `replace()` {{< /alternativa >}}
{{< alternativa >}} `strip()` {{< /alternativa >}}
{{< alternativa >}} `find()` {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `replace()` permite substituir uma sequência de caracteres por outra.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "Eu gosto de Java"

texto = texto.replace("Java", "Python")

print(texto)
{{< /code >}}

{{< alternativa >}} Eu gosto de Java {{< /alternativa >}}
{{< alternativa >}} Eu gosto de Python {{< /alternativa >}}
{{< alternativa >}} Eu Python de Java {{< /alternativa >}}
{{< alternativa >}} Python {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `replace()` substitui `"Java"` por `"Python"`. Portanto, o resultado será `"Eu gosto de Python"`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método remove espaços em branco no início e no final de uma String?

{{< alternativa >}} `split()` {{< /alternativa >}}
{{< alternativa >}} `strip()` {{< /alternativa >}}
{{< alternativa >}} `replace()` {{< /alternativa >}}
{{< alternativa >}} `find()` {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `strip()` remove espaços em branco no início e no final da String.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "  Python  "

print(texto.strip())
{{< /code >}}

{{< alternativa >}} `"  Python  "` {{< /alternativa >}}
{{< alternativa >}} `"Python"` {{< /alternativa >}}
{{< alternativa >}} `"Python  "` {{< /alternativa >}}
{{< alternativa >}} `"  Python"` {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `strip()` remove os espaços em branco do início e do final da String.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método divide uma String em uma lista de partes?

{{< alternativa >}} `split()` {{< /alternativa >}}
{{< alternativa >}} `join()` {{< /alternativa >}}
{{< alternativa >}} `replace()` {{< /alternativa >}}
{{< alternativa >}} `strip()` {{< /alternativa >}}
{{< solucao letra="A" >}}
O método `split()` divide uma String e retorna uma lista contendo as partes resultantes.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "Python Java C++"

print(texto.split())
{{< /code >}}

{{< alternativa >}} `"Python", "Java", "C++"` {{< /alternativa >}}
{{< alternativa >}} `["Python", "Java", "C++"]` {{< /alternativa >}}
{{< alternativa >}} `["Python Java C++"]` {{< /alternativa >}}
{{< alternativa >}} `Python Java C++` {{< /alternativa >}}
{{< solucao letra="B" >}}
Sem argumentos, `split()` separa a String pelos espaços em branco e retorna uma lista.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "maçã,banana,laranja"

frutas = texto.split(",")

print(frutas)
{{< /code >}}

{{< alternativa >}} ["maçã", "banana", "laranja"] {{< /alternativa >}}
{{< alternativa >}} ["maçã,banana,laranja"] {{< /alternativa >}}
{{< alternativa >}} ["maçã", "banana, laranja"] {{< /alternativa >}}
{{< alternativa >}} maçã banana laranja {{< /alternativa >}}
{{< solucao letra="A" >}}
O argumento `","` informa que a divisão deve ser feita sempre que uma vírgula for encontrada.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método pode ser utilizado para procurar a posição de uma sequência de caracteres dentro de uma String?

{{< alternativa >}} `find()` {{< /alternativa >}}
{{< alternativa >}} `split()` {{< /alternativa >}}
{{< alternativa >}} `strip()` {{< /alternativa >}}
{{< alternativa >}} `join()` {{< /alternativa >}}
{{< solucao letra="A" >}}
O método `find()` retorna o índice da primeira ocorrência da sequência procurada. Caso não encontre, retorna `-1`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "Python"

print(texto.find("t"))
{{< /code >}}

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} -1 {{< /alternativa >}}
{{< solucao letra="C" >}}
O caractere `"t"` está no índice 2 da String `"Python"`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "Python"

print(texto.find("z"))
{{< /code >}}

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} -1 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="C" >}}
Como `"z"` não aparece na String, `find()` retorna `-1`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método pode ser utilizado para verificar se uma String começa com determinado texto?

{{< alternativa >}} `startswith()` {{< /alternativa >}}
{{< alternativa >}} `endswith()` {{< /alternativa >}}
{{< alternativa >}} `find()` {{< /alternativa >}}
{{< alternativa >}} `split()` {{< /alternativa >}}
{{< solucao letra="A" >}}
O método `startswith()` verifica se a String começa com o texto informado e retorna `True` ou `False`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "Python"

print(texto.startswith("Py"))
{{< /code >}}

{{< alternativa >}} True {{< /alternativa >}}
{{< alternativa >}} False {{< /alternativa >}}
{{< alternativa >}} Py {{< /alternativa >}}
{{< alternativa >}} 0 {{< /alternativa >}}
{{< solucao letra="A" >}}
A String `"Python"` começa com `"Py"`, portanto o resultado é `True`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método pode ser utilizado para verificar se uma String termina com determinado texto?

{{< alternativa >}} `startswith()` {{< /alternativa >}}
{{< alternativa >}} `endswith()` {{< /alternativa >}}
{{< alternativa >}} `find()` {{< /alternativa >}}
{{< alternativa >}} `split()` {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `endswith()` verifica se a String termina com o texto informado e retorna `True` ou `False`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "programacao.py"

print(texto.endswith(".py"))
{{< /code >}}

{{< alternativa >}} True {{< /alternativa >}}
{{< alternativa >}} False {{< /alternativa >}}
{{< alternativa >}} ".py" {{< /alternativa >}}
{{< alternativa >}} 0 {{< /alternativa >}}
{{< solucao letra="A" >}}
A String termina com `".py"`, portanto `endswith()` retorna `True`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método junta os elementos de uma lista em uma única String?

{{< alternativa >}} `split()` {{< /alternativa >}}
{{< alternativa >}} `join()` {{< /alternativa >}}
{{< alternativa >}} `replace()` {{< /alternativa >}}
{{< alternativa >}} `strip()` {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `join()` utiliza uma String como separador e junta os elementos de uma sequência em uma única String.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
frutas = ["maçã", "banana", "laranja"]

texto = ", ".join(frutas)

print(texto)
{{< /code >}}

{{< alternativa >}} maçã banana laranja {{< /alternativa >}}
{{< alternativa >}} maçã, banana, laranja {{< /alternativa >}}
{{< alternativa >}} ["maçã", "banana", "laranja"] {{< /alternativa >}}
{{< alternativa >}} maçã,banana,laranja, {{< /alternativa >}}
{{< solucao letra="B" >}}
`join()` utiliza `", "` como separador entre os elementos da lista, produzindo `"maçã, banana, laranja"`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Strings em Python podem ser alteradas diretamente após sua criação?

{{< alternativa >}} Sim, qualquer caractere pode ser alterado pelo seu índice. {{< /alternativa >}}
{{< alternativa >}} Sim, mas apenas o primeiro caractere. {{< /alternativa >}}
{{< alternativa >}} Não, Strings são imutáveis. {{< /alternativa >}}
{{< alternativa >}} Apenas Strings numéricas podem ser alteradas. {{< /alternativa >}}
{{< solucao letra="C" >}}
Strings são imutáveis em Python. Para obter uma String modificada, normalmente é criada uma nova String.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que acontece.

{{< code >}}
texto = "Python"

texto[0] = "J"
{{< /code >}}

{{< alternativa >}} A String passa a ser `"Jython"`. {{< /alternativa >}}
{{< alternativa >}} A String passa a ser `"PythonJ"`. {{< /alternativa >}}
{{< alternativa >}} Nada acontece. {{< /alternativa >}}
{{< alternativa >}} Ocorre um erro. {{< /alternativa >}}
{{< solucao letra="D" >}}
Strings são imutáveis. Portanto, não é possível alterar diretamente um caractere utilizando seu índice.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
nome = "Ana"

print("Olá, " + nome)
{{< /code >}}

{{< alternativa >}} Olá {{< /alternativa >}}
{{< alternativa >}} Ana {{< /alternativa >}}
{{< alternativa >}} Olá, Ana {{< /alternativa >}}
{{< alternativa >}} "Olá, " + "Ana" {{< /alternativa >}}
{{< solucao letra="C" >}}
O operador `+` pode ser utilizado para concatenar Strings. Portanto, o resultado é `Olá, Ana`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
nome = "Maria"
idade = 20

print(f"{nome} tem {idade} anos")
{{< /code >}}

{{< alternativa >}} Maria tem idade anos {{< /alternativa >}}
{{< alternativa >}} nome tem idade anos {{< /alternativa >}}
{{< alternativa >}} Maria tem 20 anos {{< /alternativa >}}
{{< alternativa >}} {nome} tem {idade} anos {{< /alternativa >}}
{{< solucao letra="C" >}}
A letra `f` antes da String permite inserir os valores das variáveis utilizando `{}`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual alternativa verifica corretamente se uma String é igual a `"Python"`?

{{< alternativa >}} `texto = "Python"` {{< /alternativa >}}
{{< alternativa >}} `texto == "Python"` {{< /alternativa >}}
{{< alternativa >}} `texto = "Python"` {{< /alternativa >}}
{{< alternativa >}} `texto === "Python"` {{< /alternativa >}}
{{< solucao letra="B" >}}
O operador `==` é utilizado para comparar valores. Portanto, `texto == "Python"` verifica se o conteúdo da variável é igual a `"Python"`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "Python"

if "P" in texto:
    print("Encontrado")
else:
    print("Não encontrado")
{{< /code >}}

{{< alternativa >}} Encontrado {{< /alternativa >}}
{{< alternativa >}} Não encontrado {{< /alternativa >}}
{{< alternativa >}} P {{< /alternativa >}}
{{< alternativa >}} True {{< /alternativa >}}
{{< solucao letra="A" >}}
O operador `in` verifica se `"P"` está presente na String. Como está, a condição é verdadeira.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é o resultado da expressão abaixo?

{{< code >}}
"Python" in "Eu estudo Python"
{{< /code >}}

{{< alternativa >}} `"Python"` {{< /alternativa >}}
{{< alternativa >}} `True` {{< /alternativa >}}
{{< alternativa >}} `False` {{< /alternativa >}}
{{< alternativa >}} `1` {{< /alternativa >}}
{{< solucao letra="B" >}}
A sequência `"Python"` está presente dentro da String `"Eu estudo Python"`, portanto o resultado é `True`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método verifica se todos os caracteres de uma String são numéricos?

{{< alternativa >}} `isalpha()` {{< /alternativa >}}
{{< alternativa >}} `isdigit()` {{< /alternativa >}}
{{< alternativa >}} `islower()` {{< /alternativa >}}
{{< alternativa >}} `isspace()` {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `isdigit()` retorna `True` quando todos os caracteres da String são dígitos.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "12345"

print(texto.isdigit())
{{< /code >}}

{{< alternativa >}} True {{< /alternativa >}}
{{< alternativa >}} False {{< /alternativa >}}
{{< alternativa >}} 12345 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="A" >}}
Todos os caracteres da String são dígitos, portanto `isdigit()` retorna `True`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método verifica se todos os caracteres de uma String são letras?

{{< alternativa >}} `isdigit()` {{< /alternativa >}}
{{< alternativa >}} `isalpha()` {{< /alternativa >}}
{{< alternativa >}} `isspace()` {{< /alternativa >}}
{{< alternativa >}} `isupper()` {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `isalpha()` retorna `True` quando todos os caracteres da String são letras.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "Python"

print(texto.isalpha())
{{< /code >}}

{{< alternativa >}} True {{< /alternativa >}}
{{< alternativa >}} False {{< /alternativa >}}
{{< alternativa >}} Python {{< /alternativa >}}
{{< alternativa >}} 6 {{< /alternativa >}}
{{< solucao letra="A" >}}
Todos os caracteres de `"Python"` são letras, portanto `isalpha()` retorna `True`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método verifica se uma String contém apenas espaços em branco?

{{< alternativa >}} `isspace()` {{< /alternativa >}}
{{< alternativa >}} `isalpha()` {{< /alternativa >}}
{{< alternativa >}} `isdigit()` {{< /alternativa >}}
{{< alternativa >}} `strip()` {{< /alternativa >}}
{{< solucao letra="A" >}}
O método `isspace()` retorna `True` quando todos os caracteres da String são espaços em branco.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
texto = "   "

print(texto.isspace())
{{< /code >}}

{{< alternativa >}} True {{< /alternativa >}}
{{< alternativa >}} False {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="A" >}}
A String contém apenas espaços em branco, portanto `isspace()` retorna `True`.
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

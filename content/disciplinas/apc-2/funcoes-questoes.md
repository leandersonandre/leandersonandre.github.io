---
title: "Questões sobre Funções"
description: "Questões sobre funções em Python"
slug: funcoes-questoes
tags:
- python
- funcoes
- questões
---

{{< lista-questoes >}}

{{< questao >}}
O que é uma <b>função</b> em Python?

{{< alternativa >}} Uma unidade de código que encapsula uma tarefa ou operação específica. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura utilizada exclusivamente para armazenar números. {{< /alternativa >}}
{{< alternativa >}} Uma variável que pode armazenar apenas textos. {{< /alternativa >}}
{{< alternativa >}} Um comando utilizado exclusivamente para realizar cálculos matemáticos. {{< /alternativa >}}
{{< solucao letra="A" >}}
Uma função é uma unidade de código que encapsula uma tarefa ou operação específica e pode ser reutilizada ao longo de um programa.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual palavra-chave é utilizada para definir uma função em Python?

{{< alternativa >}} `function` {{< /alternativa >}}
{{< alternativa >}} `def` {{< /alternativa >}}
{{< alternativa >}} `func` {{< /alternativa >}}
{{< alternativa >}} `define` {{< /alternativa >}}
{{< solucao letra="B" >}}
A palavra-chave `def` é utilizada para definir uma função em Python.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. Qual é o nome da função?

{{< code >}}
def somar(a, b):
    r = a + b
    return r
{{< /code >}}

{{< alternativa >}} `def` {{< /alternativa >}}
{{< alternativa >}} `somar` {{< /alternativa >}}
{{< alternativa >}} `a` {{< /alternativa >}}
{{< alternativa >}} `r` {{< /alternativa >}}
{{< solucao letra="B" >}}
O nome da função é `somar`. A palavra `def` é a palavra-chave utilizada para definir a função.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
No código abaixo, quais são os <b>parâmetros</b> da função?

{{< code >}}
def somar(a, b):
    r = a + b
    return r
{{< /code >}}

{{< alternativa >}} `def` e `somar` {{< /alternativa >}}
{{< alternativa >}} `a` e `b` {{< /alternativa >}}
{{< alternativa >}} `r` {{< /alternativa >}}
{{< alternativa >}} `a`, `b` e `r` {{< /alternativa >}}
{{< solucao letra="B" >}}
Os parâmetros são `a` e `b`, definidos entre os parênteses após o nome da função.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. O que será impresso?

{{< code >}}
def hello():
    print("Hello Função")

hello()
{{< /code >}}

{{< alternativa >}} Nada será impresso. {{< /alternativa >}}
{{< alternativa >}} `hello` {{< /alternativa >}}
{{< alternativa >}} `Hello Função` {{< /alternativa >}}
{{< alternativa >}} Ocorrerá um erro porque a função não possui parâmetros. {{< /alternativa >}}
{{< solucao letra="C" >}}
A função é definida e depois chamada por meio de `hello()`. Quando chamada, seu corpo é executado e imprime `Hello Função`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
A definição de uma função em Python executa imediatamente o seu corpo?

{{< alternativa >}} Sim, sempre. {{< /alternativa >}}
{{< alternativa >}} Não. O corpo é executado quando a função é chamada. {{< /alternativa >}}
{{< alternativa >}} Somente se a função possuir parâmetros. {{< /alternativa >}}
{{< alternativa >}} Somente se a função possuir `return`. {{< /alternativa >}}
{{< solucao letra="B" >}}
A definição da função não executa seu corpo. As instruções são executadas quando a função é chamada.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. Qual valor será associado ao parâmetro `nome`?

{{< code >}}
def hello(nome):
    print("Olá,", nome)

hello("Pernalonga")
{{< /code >}}

{{< alternativa >}} `hello` {{< /alternativa >}}
{{< alternativa >}} `nome` {{< /alternativa >}}
{{< alternativa >}} `"Pernalonga"` {{< /alternativa >}}
{{< alternativa >}} `"Olá,"` {{< /alternativa >}}
{{< solucao letra="C" >}}
Na chamada `hello("Pernalonga")`, o argumento `"Pernalonga"` é associado ao parâmetro `nome`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
No código abaixo, o que representa o valor `10`?

{{< code >}}
def somar(a, b):
    print(a + b)

somar(10, 20)
{{< /code >}}

{{< alternativa >}} O nome da função. {{< /alternativa >}}
{{< alternativa >}} Um parâmetro. {{< /alternativa >}}
{{< alternativa >}} Um argumento. {{< /alternativa >}}
{{< alternativa >}} O corpo da função. {{< /alternativa >}}
{{< solucao letra="C" >}}
`10` é um argumento fornecido durante a chamada da função. Ele será associado ao parâmetro `a`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. O que será impresso?

{{< code >}}
def somar(a, b):
    r = a + b
    print("Resultado =", r)

somar(4, 5)
{{< /code >}}

{{< alternativa >}} `Resultado = 4` {{< /alternativa >}}
{{< alternativa >}} `Resultado = 5` {{< /alternativa >}}
{{< alternativa >}} `Resultado = 9` {{< /alternativa >}}
{{< alternativa >}} `Resultado = 20` {{< /alternativa >}}
{{< solucao letra="C" >}}
O parâmetro `a` recebe `4` e `b` recebe `5`. Portanto, `r` será `4 + 5`, resultando em `9`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Em uma chamada de função utilizando <b>argumentos posicionais</b>, como os valores são associados aos parâmetros?

{{< alternativa >}} Pelo tipo dos valores. {{< /alternativa >}}
{{< alternativa >}} Pela posição em que os argumentos são informados. {{< /alternativa >}}
{{< alternativa >}} Pelo tamanho dos nomes dos parâmetros. {{< /alternativa >}}
{{< alternativa >}} Pela ordem alfabética dos parâmetros. {{< /alternativa >}}
{{< solucao letra="B" >}}
Nos argumentos posicionais, os valores são associados aos parâmetros pela posição em que aparecem na chamada da função.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. Qual valor será associado ao parâmetro `idade`?

{{< code >}}
def apresentar(nome, idade):
    print("Nome:", nome)
    print("Idade:", idade)

apresentar("Pernalonga", 5)
{{< /code >}}

{{< alternativa >}} `"Pernalonga"` {{< /alternativa >}}
{{< alternativa >}} `5` {{< /alternativa >}}
{{< alternativa >}} `nome` {{< /alternativa >}}
{{< alternativa >}} `idade` {{< /alternativa >}}
{{< solucao letra="B" >}}
Como os argumentos são posicionais, `"Pernalonga"` é associado a `nome` e `5` é associado a `idade`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual chamada utiliza corretamente <b>argumentos nomeados</b> para a função abaixo?

{{< code >}}
def apresentar(nome, idade):
    print("Nome:", nome)
    print("Idade:", idade)
{{< /code >}}

{{< alternativa >}} `apresentar("Pernalonga", 5)` {{< /alternativa >}}
{{< alternativa >}} `apresentar(nome="Pernalonga", idade=5)` {{< /alternativa >}}
{{< alternativa >}} `apresentar(nome, idade)` {{< /alternativa >}}
{{< alternativa >}} `apresentar("nome=Pernalonga", "idade=5")` {{< /alternativa >}}
{{< solucao letra="B" >}}
Na chamada `apresentar(nome="Pernalonga", idade=5)`, os argumentos são associados explicitamente aos parâmetros pelos seus nomes.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. O que será impresso?

{{< code >}}
def apresentar(nome, idade):
    print("Nome:", nome)
    print("Idade:", idade)

apresentar(idade=5, nome="Pernalonga")
{{< /code >}}

{{< alternativa >}} `Nome: 5` e `Idade: Pernalonga` {{< /alternativa >}}
{{< alternativa >}} `Nome: Pernalonga` e `Idade: 5` {{< /alternativa >}}
{{< alternativa >}} `Nome: nome` e `Idade: idade` {{< /alternativa >}}
{{< alternativa >}} Ocorrerá um erro porque a ordem está invertida. {{< /alternativa >}}
{{< solucao letra="B" >}}
Como os argumentos são nomeados, a ordem pode ser alterada. `nome` recebe `"Pernalonga"` e `idade` recebe `5`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere a função:

{{< code >}}
def apresentar(nome, idade=18):
    print("Nome:", nome)
    print("Idade:", idade)
{{< /code >}}

O que será impresso pela chamada abaixo?

{{< code >}}
apresentar("Pernalonga")
{{< /code >}}

{{< alternativa >}} `Nome: Pernalonga` e `Idade: 18` {{< /alternativa >}}
{{< alternativa >}} `Nome: Pernalonga` e `Idade: 0` {{< /alternativa >}}
{{< alternativa >}} `Nome: 18` e `Idade: Pernalonga` {{< /alternativa >}}
{{< alternativa >}} Ocorrerá um erro porque `idade` não foi informada. {{< /alternativa >}}
{{< solucao letra="A" >}}
Como nenhum argumento foi fornecido para `idade`, será utilizado o valor padrão `18`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere a função:

{{< code >}}
def apresentar(nome, idade=18):
    print("Nome:", nome)
    print("Idade:", idade)
{{< /code >}}

O que será impresso pela chamada abaixo?

{{< code >}}
apresentar("Pernalonga", 5)
{{< /code >}}

{{< alternativa >}} `Nome: Pernalonga` e `Idade: 18` {{< /alternativa >}}
{{< alternativa >}} `Nome: Pernalonga` e `Idade: 5` {{< /alternativa >}}
{{< alternativa >}} `Nome: 5` e `Idade: Pernalonga` {{< /alternativa >}}
{{< alternativa >}} Ocorrerá um erro porque existe um valor padrão. {{< /alternativa >}}
{{< solucao letra="B" >}}
Quando um argumento é fornecido, ele substitui o valor padrão. Portanto, `idade` recebe `5`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. Quantos argumentos podem ser fornecidos na chamada da função?

{{< code >}}
def somar(*numeros):
    resultado = 0
    for numero in numeros:
        resultado += numero
    print(resultado)
{{< /code >}}

{{< alternativa >}} Exatamente um. {{< /alternativa >}}
{{< alternativa >}} Exatamente dois. {{< /alternativa >}}
{{< alternativa >}} Uma quantidade variável de argumentos. {{< /alternativa >}}
{{< alternativa >}} Nenhum argumento. {{< /alternativa >}}
{{< solucao letra="C" >}}
O parâmetro precedido por `*` permite que a função receba uma quantidade variável de argumentos.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. Qual é o tipo de estrutura que armazena os valores recebidos por `*numeros`?

{{< code >}}
def somar(*numeros):
    resultado = 0
    for numero in numeros:
        resultado += numero
    print(resultado)
{{< /code >}}

{{< alternativa >}} Lista {{< /alternativa >}}
{{< alternativa >}} Dicionário {{< /alternativa >}}
{{< alternativa >}} Tupla {{< /alternativa >}}
{{< alternativa >}} String {{< /alternativa >}}
{{< solucao letra="C" >}}
Os argumentos recebidos por um parâmetro precedido por `*` são agrupados em uma tupla.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. O que será impresso?

{{< code >}}
def somar(*numeros):
    resultado = 0
    for numero in numeros:
        resultado += numero
    print(resultado)

somar(1, 2, 3)
{{< /code >}}

{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 6 {{< /alternativa >}}
{{< alternativa >}} 123 {{< /alternativa >}}
{{< solucao letra="C" >}}
Os argumentos `1`, `2` e `3` são agrupados em `numeros`. O laço soma os valores, resultando em `6`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a finalidade do parâmetro precedido por <b>**</b> em uma função Python?

{{< alternativa >}} Receber uma quantidade variável de argumentos posicionais. {{< /alternativa >}}
{{< alternativa >}} Receber uma quantidade variável de argumentos nomeados. {{< /alternativa >}}
{{< alternativa >}} Definir um valor padrão. {{< /alternativa >}}
{{< alternativa >}} Impedir que a função receba argumentos. {{< /alternativa >}}
{{< solucao letra="B" >}}
Um parâmetro precedido por `**` permite receber uma quantidade variável de argumentos nomeados.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. Qual é o tipo de estrutura que armazena os argumentos recebidos por `**dados`?

{{< code >}}
def apresentar(**dados):
    for chave, valor in dados.items():
        print(chave, "=", valor)
{{< /code >}}

{{< alternativa >}} Lista {{< /alternativa >}}
{{< alternativa >}} Tupla {{< /alternativa >}}
{{< alternativa >}} String {{< /alternativa >}}
{{< alternativa >}} Dicionário {{< /alternativa >}}
{{< solucao letra="D" >}}
Os argumentos nomeados recebidos por `**dados` são agrupados em um dicionário.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. O que será impresso?

{{< code >}}
def apresentar(**dados):
    for chave, valor in dados.items():
        print(chave, "=", valor)

apresentar(nome="Pernalonga", idade=5)
{{< /code >}}

{{< alternativa >}} `nome = Pernalonga` e `idade = 5` {{< /alternativa >}}
{{< alternativa >}} `Pernalonga = nome` e `5 = idade` {{< /alternativa >}}
{{< alternativa >}} `nome = 5` e `idade = Pernalonga` {{< /alternativa >}}
{{< alternativa >}} Nada será impresso. {{< /alternativa >}}
{{< solucao letra="A" >}}
Os argumentos nomeados são armazenados no dicionário `dados`. O laço percorre as chaves e os valores, imprimindo `nome = Pernalonga` e `idade = 5`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. Qual alternativa apresenta uma chamada válida para a função?

{{< code >}}
def somar_tres(a, b, c):
    r = a + b + c
    print("Resultado =", r)
{{< /code >}}

{{< alternativa >}} `somar_tres(3, 7)` {{< /alternativa >}}
{{< alternativa >}} `somar_tres(3, 7, 8)` {{< /alternativa >}}
{{< alternativa >}} `somar_tres(3)` {{< /alternativa >}}
{{< alternativa >}} `somar_tres()` {{< /alternativa >}}
{{< solucao letra="B" >}}
A função possui três parâmetros obrigatórios: `a`, `b` e `c`. Portanto, a chamada deve fornecer três argumentos.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo. O que será impresso?

{{< code >}}
def somar_tres(a, b, c):
    r = a + b + c
    print("Resultado =", r)

somar_tres(3, 7, 8)
{{< /code >}}

{{< alternativa >}} `Resultado = 15` {{< /alternativa >}}
{{< alternativa >}} `Resultado = 18` {{< /alternativa >}}
{{< alternativa >}} `Resultado = 21` {{< /alternativa >}}
{{< alternativa >}} `Resultado = 24` {{< /alternativa >}}
{{< solucao letra="C" >}}
Os parâmetros recebem `a = 3`, `b = 7` e `c = 8`. Assim, `3 + 7 + 8 = 18`.
{{< /solucao >}}
{{< /questao >}}



{{< /lista-questoes >}}

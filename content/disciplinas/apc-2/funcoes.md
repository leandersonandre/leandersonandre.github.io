---
title: "Funções"
description: "Estrutura utilizada para organizar e reutilizar código em Python"
slug: funcoes
tags:
 - funções
 - python
 - programação
---

Uma **função** é uma unidade de código que encapsula uma tarefa ou operação específica e pode ser reutilizada ao longo de um programa.

As funções permitem **abstração, organização e reutilização de código**.

Por exemplo:

```python
def hello():
    print("Hello Função")
````

A função `hello` pode ser chamada sempre que quisermos executar seu código:

```python
hello()
```

## Definição de uma função

Em Python, uma função é definida utilizando a palavra-chave `def`.

A estrutura básica é:

```python
def nome_da_funcao():
    # corpo da função
```

Por exemplo:

```python
def hello():
    print("Hello Função")
```

Nesse exemplo:

* `def`: palavra-chave utilizada para definir uma função;
* `hello`: nome da função;
* `()`: indica os parâmetros da função;
* `print("Hello Função")`: instrução pertencente ao corpo da função.

A definição da função **não executa** o seu corpo.

Para executar a função, precisamos chamá-la:

```python
hello()
```

## Anatomia de uma função

Uma função pode ser composta por:

* **nome**;
* **parâmetros**;
* **corpo**;
* **retorno**.

Por exemplo:

```python
def somar(a, b):
    r = a + b
    return r
```

Nesse exemplo:

* `somar`: nome da função;
* `a` e `b`: parâmetros;
* `r = a + b`: instrução do corpo da função;
* `return r`: valor retornado pela função.

O nome e o conjunto de parâmetros geralmente definem a **assinatura** de uma função. A definição de assinatura pode variar conforme a linguagem de programação.

## Chamando uma função

Uma função pode ser chamada utilizando seu nome seguido de parênteses.

Primeiro, a função deve ser definida:

```python
def hello():
    print("Hello Função")
```

Depois, podemos chamá-la:

```python
hello()
```

Quando a função não possui parâmetros, não precisamos fornecer argumentos na chamada.

Podemos chamar a mesma função várias vezes:

```python
hello()
hello()
hello()
```

Cada chamada executará o corpo da função.

## Corpo de uma função

O **corpo de uma função** é formado pelo conjunto de instruções que serão executadas quando a função for chamada.

Em Python, o corpo da função é definido pela **indentação**.

Por exemplo:

```python
print("Fora da função")

def minha_funcao(a, b, c):
    print("Inicio da funcao")
    x = 0
    print("x =", x)

print("Fora da função")

minha_funcao(1, 2, 3)
```

As instruções indentadas após `def` pertencem ao corpo da função:

```python
def minha_funcao(a, b, c):
    print("Inicio da funcao")
    x = 0
    print("x =", x)
```

Já as instruções que não estão indentadas pertencem ao código externo à função.

## Parâmetros

Os **parâmetros** são nomes que representam os valores que uma função pode receber como entrada.

Uma função pode possuir nenhum, um ou vários parâmetros.

Por exemplo, uma função sem parâmetros:

```python
def sem_parametro():
    pass
```

Uma função com um parâmetro:

```python
def um_parametro(a):
    pass
```

Uma função com dois parâmetros:

```python
def dois_parametros(a, b):
    pass
```

Uma função com quatro parâmetros:

```python
def quatro_parametros(a, b, c, d):
    pass
```

Os parâmetros são definidos dentro dos parênteses após o nome da função.

## Argumentos

Os **argumentos** são os valores fornecidos para os parâmetros de uma função durante sua chamada.

Considere a função:

```python
def somar(a, b):
    print(a + b)
```

Podemos chamar a função fornecendo dois argumentos:

```python
somar(10, 20)
```

Nesse caso:

* `a` e `b` são **parâmetros**;
* `10` e `20` são **argumentos**;
* `10` é associado ao parâmetro `a`;
* `20` é associado ao parâmetro `b`.

Podemos pensar nos parâmetros como os nomes utilizados dentro da função e nos argumentos como os valores fornecidos durante a chamada.

## Função com um parâmetro

Considere a função:

```python
def hello(nome):
    print("Olá,", nome)
```

A função possui um parâmetro chamado `nome`.

Para chamá-la, devemos fornecer um argumento:

```python
hello("Pernalonga")
```

Nesse caso:

* `nome` é o parâmetro;
* `"Pernalonga"` é o argumento.

O valor fornecido será utilizado dentro da função:

```text
Olá, Pernalonga
```

## Função com vários parâmetros

Uma função pode possuir dois ou mais parâmetros.

Por exemplo:

```python
def somar(a, b):
    r = a + b
    print("Resultado =", r)
```

Podemos chamar a função fornecendo dois argumentos:

```python
somar(4, 5)
```

Nesse caso:

* `a` recebe o valor `4`;
* `b` recebe o valor `5`.

O resultado será:

```text
Resultado = 9
```

Também podemos criar funções com três ou mais parâmetros:

```python
def somar_tres(a, b, c):
    r = a + b + c
    print("Resultado =", r)
```

A chamada pode fornecer três argumentos:

```python
somar_tres(3, 7, 8)
```

Resultado:

```text
Resultado = 18
```

## Argumentos posicionais

Em Python, os argumentos podem ser associados aos parâmetros **pela posição** em que são informados na chamada da função.

Considere:

```python
def apresentar(nome, idade):
    print("Nome:", nome)
    print("Idade:", idade)
```

Podemos chamar a função desta forma:

```python
apresentar("Pernalonga", 5)
```

Nesse caso:

* `"Pernalonga"` é associado ao parâmetro `nome`;
* `5` é associado ao parâmetro `idade`.

A ordem dos argumentos deve corresponder à ordem dos parâmetros.

Por exemplo:

```python
apresentar("Pernalonga", 5)
```

é equivalente a:

```text
nome = "Pernalonga"
idade = 5
```

## Argumentos nomeados

Em Python, os argumentos também podem ser associados aos parâmetros **pelo nome**.

Considere novamente:

```python
def apresentar(nome, idade):
    print("Nome:", nome)
    print("Idade:", idade)
```

Podemos chamar a função utilizando argumentos nomeados:

```python
apresentar(nome="Pernalonga", idade=5)
```

Nesse caso:

* `nome="Pernalonga"` associa o argumento ao parâmetro `nome`;
* `idade=5` associa o argumento ao parâmetro `idade`.

A ordem dos argumentos nomeados pode ser alterada:

```python
apresentar(idade=5, nome="Pernalonga")
```

O resultado continua sendo:

```text
Nome: Pernalonga
Idade: 5
```

## Argumentos posicionais e nomeados

Considere a função:

```python
def apresentar(nome, idade):
    print("Nome:", nome)
    print("Idade:", idade)
```

Podemos utilizar argumentos posicionais:

```python
apresentar("Pernalonga", 5)
```

Ou argumentos nomeados:

```python
apresentar(nome="Pernalonga", idade=5)
```

Com argumentos nomeados, a ordem pode ser alterada:

```python
apresentar(idade=5, nome="Pernalonga")
```

A diferença principal é a forma como os argumentos são associados aos parâmetros:

| Tipo       | Associação             |
| ---------- | ---------------------- |
| Posicional | Pela posição           |
| Nomeado    | Pelo nome do parâmetro |

## Parâmetros com valores padrão

Um parâmetro pode possuir um **valor padrão**.

Esse valor será utilizado quando nenhum argumento for fornecido para esse parâmetro.

Por exemplo:

```python
def apresentar(nome, idade=18):
    print("Nome:", nome)
    print("Idade:", idade)
```

Podemos fornecer o argumento normalmente:

```python
apresentar("Pernalonga", 5)
```

Nesse caso, `idade` recebe o valor `5`.

Também podemos omitir o argumento:

```python
apresentar("Pernalonga")
```

Nesse caso, `idade` recebe o valor padrão `18`.

Resultado:

```text
Nome: Pernalonga
Idade: 18
```

O valor padrão permite que determinados argumentos sejam opcionais durante a chamada da função.

## Retorno de uma função

Uma função pode produzir um valor utilizando a instrução `return`.

Por exemplo:

```python
def somar(a, b):
    r = a + b
    return r
```

Podemos armazenar o valor retornado em uma variável:

```python
resultado = somar(10, 20)

print(resultado)
```

Resultado:

```text
30
```

Nesse caso:

```python
somar(10, 20)
```

produz o valor:

```text
30
```

Esse valor pode ser utilizado em outras expressões:

```python
resultado = somar(10, 20) * 2

print(resultado)
```

Resultado:

```text
60
```

O `return` permite que uma função **devolva um valor** para o código que realizou a chamada.

## Quantidade variável de argumentos

Uma função pode receber uma **quantidade variável de argumentos** utilizando um parâmetro precedido por `*`.

Por exemplo:

```python
def somar(*numeros):
    resultado = 0

    for numero in numeros:
        resultado += numero

    print(resultado)
```

A função pode ser chamada com diferentes quantidades de argumentos:

```python
somar(1, 2)
```

```python
somar(1, 2, 3, 4)
```

```python
somar(10, 20, 30, 40, 50)
```

Os argumentos recebidos por `*numeros` são agrupados em uma **tupla**.

Por exemplo:

```python
def mostrar(*numeros):
    print(numeros)

mostrar(10, 20, 30)
```

Resultado:

```text
(10, 20, 30)
```

Assim, `*numeros` permite que a função receba uma quantidade variável de argumentos posicionais.

## Argumentos nomeados de quantidade variável

Também podemos receber uma quantidade variável de **argumentos nomeados**.

Para isso, utilizamos um parâmetro precedido por `**`.

Por exemplo:

```python
def apresentar(**dados):
    for chave, valor in dados.items():
        print(chave, "=", valor)
```

Podemos chamar a função com diferentes quantidades de argumentos nomeados:

```python
apresentar(nome="Pernalonga", idade=5)
```

Ou:

```python
apresentar(
    nome="Pernalonga",
    idade=5,
    cidade="Joinville"
)
```

Os argumentos recebidos por `**dados` são agrupados em um **dicionário**.

Por exemplo:

```python
def mostrar(**dados):
    print(dados)

mostrar(nome="Pernalonga", idade=5)
```

Resultado:

```text
{'nome': 'Pernalonga', 'idade': 5}
```

Assim, `**dados` permite que a função receba uma quantidade variável de argumentos nomeados.

## `*args` e `**kwargs`

Os nomes `args` e `kwargs` são frequentemente utilizados por convenção para representar esses parâmetros.

Por exemplo:

```python
def exemplo(*args):
    print(args)
```

E:

```python
def exemplo(**kwargs):
    print(kwargs)
```

Os nomes não são obrigatórios. O que define o comportamento especial são os símbolos `*` e `**`.

Por exemplo:

```python
def somar(*numeros):
    print(numeros)
```

funciona da mesma forma que:

```python
def somar(*args):
    print(args)
```

O primeiro exemplo pode ser mais descritivo quando sabemos que os valores representam números.

## Comparação entre os tipos de parâmetros

Podemos resumir os principais tipos apresentados:

| Sintaxe           | Utilização                                    |
| ----------------- | --------------------------------------------- |
| `def f()`         | Sem parâmetros                                |
| `def f(a)`        | Um parâmetro                                  |
| `def f(a, b)`     | Vários parâmetros                             |
| `def f(a=10)`     | Parâmetro com valor padrão                    |
| `def f(*args)`    | Quantidade variável de argumentos posicionais |
| `def f(**kwargs)` | Quantidade variável de argumentos nomeados    |

## Exemplo completo

O exemplo abaixo reúne vários conceitos relacionados a funções:

```python
def apresentar(nome, idade=18):
    print("Nome:", nome)
    print("Idade:", idade)


apresentar("Pernalonga", 5)

apresentar(nome="Pernalonga", idade=5)

apresentar(idade=5, nome="Pernalonga")

apresentar("Pernalonga")
```

Resultado:

```text
Nome: Pernalonga
Idade: 5

Nome: Pernalonga
Idade: 5

Nome: Pernalonga
Idade: 5

Nome: Pernalonga
Idade: 18
```

Outro exemplo utiliza quantidade variável de argumentos:

```python
def somar(*numeros):
    resultado = 0

    for numero in numeros:
        resultado += numero

    return resultado


resultado = somar(10, 20, 30)

print("Resultado:", resultado)
```

Resultado:

```text
Resultado: 60
```

## Principais conceitos

Alguns dos principais conceitos relacionados às funções são:

| Conceito             | Descrição                                             |
| -------------------- | ----------------------------------------------------- |
| `def`                | Define uma função                                     |
| Nome                 | Identifica a função                                   |
| Parâmetro            | Nome que representa um valor recebido                 |
| Argumento            | Valor fornecido durante a chamada                     |
| Corpo                | Conjunto de instruções da função                      |
| `return`             | Retorna um valor                                      |
| Argumento posicional | Associado pela posição                                |
| Argumento nomeado    | Associado pelo nome                                   |
| Valor padrão         | Valor utilizado quando o argumento é omitido          |
| `*`                  | Permite quantidade variável de argumentos posicionais |
| `**`                 | Permite quantidade variável de argumentos nomeados    |

## Conclusão

As **funções** são utilizadas para organizar e reutilizar código em Python.

Seus principais conceitos são:

* Uma função encapsula uma tarefa ou operação específica.
* Uma função é definida utilizando `def`.
* A definição da função não executa automaticamente seu corpo.
* Uma função pode ser chamada utilizando seu nome.
* Parâmetros representam os valores que uma função pode receber.
* Argumentos são os valores fornecidos durante a chamada.
* Argumentos podem ser posicionais ou nomeados.
* Parâmetros podem possuir valores padrão.
* Uma função pode retornar valores utilizando `return`.
* O parâmetro `*` permite receber uma quantidade variável de argumentos posicionais.
* O parâmetro `**` permite receber uma quantidade variável de argumentos nomeados.
* Argumentos recebidos por `*` são agrupados em uma tupla.
* Argumentos recebidos por `**` são agrupados em um dicionário.
* A indentação define o corpo da função em Python.

O uso de funções é fundamental para desenvolver programas mais **organizados, reutilizáveis e fáceis de compreender e manter**.

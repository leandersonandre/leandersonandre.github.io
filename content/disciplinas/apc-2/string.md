---

title: "Strings"
description: "Tipo de dado utilizado para representar sequências de caracteres em Python"
slug: string
tags:
 - tipos-de-dados
 - string
 - python
 - str
---

Uma **string** (`str`) é um tipo de dado utilizado para representar uma **sequência de caracteres** em Python.

Uma string pode conter letras, números, espaços, símbolos e outros caracteres.

Por exemplo:

```python
nome = "Python"
mensagem = "Olá, mundo!"
codigo = "12345"
```

Mesmo que uma string contenha apenas números, ela continua sendo uma string:

```python
codigo = "12345"

print(type(codigo))
```

Resultado:

```text
<class 'str'>
```

## Criação de strings

Strings podem ser criadas utilizando aspas simples:

```python
nome = 'Python'
```

Ou aspas duplas:

```python
nome = "Python"
```

Também podemos utilizar aspas triplas para strings que ocupam várias linhas:

```python
texto = """Primeira linha
Segunda linha
Terceira linha"""
```

É possível utilizar aspas simples dentro de uma string delimitada por aspas duplas:

```python
mensagem = "Ele disse 'Olá!'"
```

E também o contrário:

```python
mensagem = 'Ele disse "Olá!"'
```

## Strings são sequências

Uma string é uma **sequência de caracteres**.

Por exemplo:

```python
palavra = "Python"
```

Podemos visualizar seus caracteres da seguinte forma:

```text
Índice:     0    1    2    3    4    5
           ┌────┬────┬────┬────┬────┬────┐
String:    │ P  │ y  │ t  │ h  │ o  │ n  │
           └────┴────┴────┴────┴────┴────┘
```

Assim como acontece com listas, os índices começam em `0`.

```python
print(palavra[0])  # P
print(palavra[1])  # y
print(palavra[5])  # n
```

Também podemos utilizar índices negativos:

```python
print(palavra[-1])  # n
print(palavra[-2])  # o
```

## Tamanho da string

A função `len()` retorna a quantidade de caracteres:

```python
texto = "Python"

print(len(texto))
```

Resultado:

```text
6
```

Os espaços também são considerados caracteres:

```python
texto = "Olá mundo"

print(len(texto))
```

Resultado:

```text
9
```

## Acesso aos caracteres

Podemos acessar qualquer caractere utilizando seu índice:

```python
nome = "Maria"

print(nome[0])
print(nome[2])
print(nome[4])
```

Resultado:

```text
M
r
a
```

Tentar acessar um índice que não existe gera uma exceção `IndexError`:

```python
print(nome[10])
```

## Slicing

Assim como listas, strings permitem utilizar *slicing* para obter partes da sequência.

A sintaxe básica é:

```python
string[inicio:fim]
```

Por exemplo:

```python
texto = "Python"

print(texto[0:3])
```

Resultado:

```text
Pyt
```

O índice inicial é incluído e o índice final não é incluído.

Também podemos utilizar:

```python
print(texto[:3])   # Pyt
print(texto[2:])   # thon
print(texto[:])    # Python
```

É possível utilizar um passo:

```python
print(texto[::2])
```

Resultado:

```text
Pto
```

Também podemos inverter uma string:

```python
print(texto[::-1])
```

Resultado:

```text
nohtyP
```

## Strings são imutáveis

Strings em Python são **imutáveis**.

Isso significa que não podemos alterar diretamente um caractere de uma string.

O código abaixo gera um erro:

```python
nome = "Maria"

nome[0] = "X"
```

Para modificar uma string, precisamos criar uma nova string:

```python
nome = "Maria"

nome = "X" + nome[1:]

print(nome)
```

Resultado:

```text
Xaria
```

Os métodos de string também não modificam a string original. Eles normalmente retornam uma nova string.

## Converter para maiúsculas

O método `upper()` retorna uma nova string com os caracteres em maiúsculas:

```python
texto = "Python"

print(texto.upper())
```

Resultado:

```text
PYTHON
```

A string original permanece inalterada:

```python
texto = "Python"

texto.upper()

print(texto)
```

Resultado:

```text
Python
```

Para armazenar o resultado:

```python
texto = texto.upper()
```

## Converter para minúsculas

O método `lower()` retorna uma string com os caracteres em minúsculas:

```python
texto = "PYTHON"

print(texto.lower())
```

Resultado:

```text
python
```

## Capitalização

O método `capitalize()` coloca o primeiro caractere em maiúsculo e os demais em minúsculo:

```python
texto = "python É UMA LINGUAGEM"

print(texto.capitalize())
```

Resultado:

```text
Python é uma linguagem
```

O método `title()` coloca a primeira letra de cada palavra em maiúscula:

```python
texto = "linguagem de programação"

print(texto.title())
```

Resultado:

```text
Linguagem De Programação
```

## Remover espaços

O método `strip()` remove espaços no início e no final da string:

```python
texto = "   Python   "

print(texto.strip())
```

Resultado:

```text
Python
```

Também existem:

```python
texto.lstrip()  # remove espaços do início
texto.rstrip()  # remove espaços do final
```

`strip()` é muito utilizado para tratar dados recebidos pelo usuário:

```python
nome = input("Digite seu nome: ")

nome = nome.strip()
```

## Substituir partes da string

O método `replace()` substitui uma parte da string por outra:

```python
texto = "Eu gosto de Java"

texto = texto.replace("Java", "Python")

print(texto)
```

Resultado:

```text
Eu gosto de Python
```

Também podemos limitar a quantidade de substituições:

```python
texto = "banana banana banana"

print(texto.replace("banana", "maçã", 1))
```

Resultado:

```text
maçã banana banana
```

## Verificar se uma string contém outra

O operador `in` verifica se uma sequência de caracteres está presente em outra:

```python
texto = "Python é uma linguagem de programação"

print("Python" in texto)
```

Resultado:

```text
True
```

Também podemos utilizar `not in`:

```python
print("Java" not in texto)
```

Resultado:

```text
True
```

## Encontrar uma substring

O método `find()` retorna o índice da primeira ocorrência de uma substring:

```python
texto = "Python é uma linguagem"

print(texto.find("linguagem"))
```

Resultado:

```text
14
```

Se a substring não for encontrada, `find()` retorna `-1`:

```python
print(texto.find("Java"))
```

Resultado:

```text
-1
```

O método `index()` possui comportamento semelhante, mas gera uma exceção `ValueError` quando a substring não é encontrada:

```python
print(texto.index("linguagem"))
```

## Contar ocorrências

O método `count()` informa quantas vezes uma sequência aparece:

```python
texto = "banana"

print(texto.count("a"))
```

Resultado:

```text
3
```

Também podemos contar palavras:

```python
texto = "Python é simples. Python é poderoso."

print(texto.count("Python"))
```

Resultado:

```text
2
```

## Verificar o início e o final

O método `startswith()` verifica se uma string começa com determinado texto:

```python
arquivo = "relatorio.pdf"

print(arquivo.startswith("relatorio"))
```

Resultado:

```text
True
```

O método `endswith()` verifica se uma string termina com determinado texto:

```python
print(arquivo.endswith(".pdf"))
```

Resultado:

```text
True
```

Esses métodos são úteis para verificar extensões de arquivos, prefixos e outros padrões simples.

## Dividir uma string

O método `split()` divide uma string e retorna uma **lista**.

Por padrão, a divisão é feita pelos espaços:

```python
texto = "Python é muito interessante"

palavras = texto.split()

print(palavras)
```

Resultado:

```text
['Python', 'é', 'muito', 'interessante']
```

Também podemos informar um separador:

```python
data = "27/08/2026"

partes = data.split("/")

print(partes)
```

Resultado:

```text
['27', '08', '2026']
```

## Juntar strings

O método `join()` realiza a operação inversa do `split()`.

Ele utiliza uma string como separador para juntar os elementos de uma sequência:

```python
palavras = ["Python", "é", "legal"]

texto = " ".join(palavras)

print(texto)
```

Resultado:

```text
Python é legal
```

Podemos escolher outro separador:

```python
nomes = ["Ana", "Bruno", "Carlos"]

resultado = ", ".join(nomes)

print(resultado)
```

Resultado:

```text
Ana, Bruno, Carlos
```

## Verificar o tipo de caracteres

Python possui métodos que permitem verificar o conteúdo de uma string.

### `isdigit()`

Verifica se todos os caracteres são dígitos:

```python
texto = "12345"

print(texto.isdigit())
```

Resultado:

```text
True
```

### `isalpha()`

Verifica se todos os caracteres são letras:

```python
texto = "Python"

print(texto.isalpha())
```

Resultado:

```text
True
```

### `isalnum()`

Verifica se todos os caracteres são letras ou números:

```python
texto = "Python123"

print(texto.isalnum())
```

Resultado:

```text
True
```

### `isspace()`

Verifica se todos os caracteres são espaços em branco:

```python
texto = "   "

print(texto.isspace())
```

Resultado:

```text
True
```

Esses métodos retornam `True` ou `False` e são especialmente úteis para validação de dados.

## Formatação de strings

Uma forma bastante utilizada para inserir valores dentro de strings é utilizar **f-strings**.

```python
nome = "Maria"
idade = 25

mensagem = f"Meu nome é {nome} e tenho {idade} anos."

print(mensagem)
```

Resultado:

```text
Meu nome é Maria e tenho 25 anos.
```

Expressões também podem ser utilizadas:

```python
a = 10
b = 20

print(f"A soma é {a + b}")
```

Resultado:

```text
A soma é 30
```

As f-strings são uma forma simples e legível de construir textos utilizando valores de variáveis.

## Percorrer uma string

Como uma string é uma sequência, podemos percorrer seus caracteres utilizando `for`:

```python
palavra = "Python"

for caractere in palavra:
    print(caractere)
```

Resultado:

```text
P
y
t
h
o
n
```

Também podemos utilizar os índices:

```python
for i in range(len(palavra)):
    print(palavra[i])
```

Quando o índice não é necessário, percorrer diretamente os caracteres costuma deixar o código mais simples.

## Comparação de strings

Strings podem ser comparadas utilizando operadores de comparação:

```python
nome1 = "Ana"
nome2 = "Ana"

print(nome1 == nome2)
```

Resultado:

```text
True
```

Também podemos verificar se são diferentes:

```python
print(nome1 != nome2)
```

A comparação diferencia letras maiúsculas e minúsculas:

```python
print("Python" == "python")
```

Resultado:

```text
False
```

Quando queremos comparar textos sem considerar a diferença entre maiúsculas e minúsculas, podemos utilizar `lower()`:

```python
nome1 = "PYTHON"
nome2 = "python"

print(nome1.lower() == nome2.lower())
```

Resultado:

```text
True
```

## Principais métodos

Alguns dos métodos mais utilizados em strings são:

| Método         | Função                               |
| -------------- | ------------------------------------ |
| `upper()`      | Converte para maiúsculas             |
| `lower()`      | Converte para minúsculas             |
| `capitalize()` | Capitaliza a string                  |
| `title()`      | Capitaliza cada palavra              |
| `strip()`      | Remove espaços no início e no final  |
| `replace()`    | Substitui partes da string           |
| `find()`       | Localiza uma substring               |
| `count()`      | Conta ocorrências                    |
| `startswith()` | Verifica o início da string          |
| `endswith()`   | Verifica o final da string           |
| `split()`      | Divide a string em uma lista         |
| `join()`       | Junta elementos de uma sequência     |
| `isdigit()`    | Verifica se contém apenas dígitos    |
| `isalpha()`    | Verifica se contém apenas letras     |
| `isalnum()`    | Verifica se contém letras ou números |
| `isspace()`    | Verifica se contém apenas espaços    |

## Exemplo completo

O exemplo abaixo demonstra algumas das principais operações realizadas com strings:

```python
texto = "  Python é uma linguagem de programação  "

texto = texto.strip()

print("Texto:", texto)
print("Tamanho:", len(texto))

print("Maiúsculo:", texto.upper())
print("Minúsculo:", texto.lower())

print("Contém Python:", "Python" in texto)

print("Quantidade de 'a':", texto.count("a"))

print("Posição de 'linguagem':", texto.find("linguagem"))

palavras = texto.split()

print("Palavras:", palavras)

print("Texto novamente:", " ".join(palavras))
```

## Conclusão

A `str` é o tipo utilizado para representar **sequências de caracteres** em Python.

Suas principais características são:

* Strings representam sequências de caracteres.
* Os índices começam em `0`.
* É possível acessar caracteres individualmente.
* É possível utilizar *slicing*.
* Strings são imutáveis.
* Python fornece diversos métodos para manipulação e validação de textos.
* Métodos como `split()` e `join()` permitem trabalhar com strings e listas.
* O operador `in` permite verificar se determinado texto está presente.
* F-strings facilitam a criação de textos utilizando valores de variáveis.

Compreender strings é fundamental para trabalhar com **textos, entrada de dados, arquivos, validação e processamento de informações** em Python.

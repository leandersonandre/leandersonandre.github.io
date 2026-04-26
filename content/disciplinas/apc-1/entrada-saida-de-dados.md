---
title: "Entrada e Saída de dados"
slug: entrada-saida-de-dados
description: "Entrada e saída de dados em Python"
tags:
- python
- print
- input
---


Em Python, a interação com o usuário ocorre por meio de entrada e saída de dados. Para isso, utilizamos principalmente as funções `input()` e `print()`.

## Saída de dados

A função `print()` é utilizada para exibir informações na tela.

```python
print("Olá mundo")
```

Também é possível imprimir valores armazenados em variáveis.

```python
nome = "Ana"
print(nome)
```

## Múltiplos valores

O `print()` permite exibir vários valores ao mesmo tempo.

```python
nome = "Ana"
idade = 20

print("Nome:", nome, "Idade:", idade)
```

Por padrão, os valores são separados por um espaço.


## Parâmetro end

O parâmetro `end` define o que será exibido ao final da impressão. Por padrão, o `print()` pula para a próxima linha.

```python
print("A", end=" ")
print("B")
```

Saída:
```
A B
```

Outro exemplo:

```python
print("Linha 1", end=" - ")
print("Linha 2")
```

Saída:
```
Linha 1 - Linha 2
```

## Sequências de escape

As sequências de escape são utilizadas para inserir caracteres especiais dentro das strings.

Alguns exemplos:

- `\n` → quebra de linha  
- `\t` → tabulação  
- `\\` → barra invertida  
- `\"` → aspas duplas  

```python
print("Linha 1\nLinha 2")
print("Coluna1\tColuna2")
print("Caminho: C:\\pasta\\arquivo")
print("Ele disse: \"Olá\"")
```


## Entrada de dados

A função `input()` permite ler dados digitados pelo usuário.

```python
nome = input("Digite seu nome: ")
print("Olá,", nome)
```

O valor lido pelo `input()` é sempre do tipo string.


## Conversão de tipos

Para trabalhar com números, é necessário converter o valor da entrada.

```python
idade = int(input("Digite sua idade: "))
print(idade + 1)
```

Outros exemplos:

```python
valor = float(input("Digite um número: "))
```


## Observação

A entrada e saída de dados são fundamentais para tornar programas interativos, permitindo comunicação entre o usuário e o sistema.

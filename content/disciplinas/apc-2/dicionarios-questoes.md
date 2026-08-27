---
title: "Questões sobre Dicionários"
description: "Questões sobre a estrutura de dados dicionário em Python"
slug: dicionarios-questoes
tags:
- python
- dicionários
- questões
---

{{< lista-questoes >}}

{{< questao >}}
O que é um dicionário em Python?

{{< alternativa >}} Uma estrutura que armazena apenas valores numéricos. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que armazena dados na forma de pares de chave e valor. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que não permite alterações após sua criação. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que permite apenas valores repetidos. {{< /alternativa >}}
{{< solucao letra="B" >}}
Um dicionário armazena dados na forma de pares de **chave e valor**, permitindo acessar um valor por meio de sua chave.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual das alternativas cria corretamente um dicionário?

{{< alternativa >}} `aluno = ["João", 20]` {{< /alternativa >}}
{{< alternativa >}} `aluno = ("João", 20)` {{< /alternativa >}}
{{< alternativa >}} `aluno = {"nome": "João", "idade": 20}` {{< /alternativa >}}
{{< alternativa >}} `aluno = {"João", 20}` {{< /alternativa >}}
{{< solucao letra="C" >}}
Um dicionário é criado utilizando chaves e armazenando os dados no formato `chave: valor`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere o seguinte dicionário:

{{< code >}}
aluno = {
    "nome": "Ana",
    "idade": 20,
    "nota": 8.5
}
{{< /code >}}

Quantas chaves existem nesse dicionário?

{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< solucao letra="C" >}}
O dicionário possui as chaves `"nome"`, `"idade"` e `"nota"`. Portanto, existem três chaves.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
aluno = {
    "nome": "Ana",
    "idade": 20
}

print(aluno["nome"])
{{< /code >}}

{{< alternativa >}} Ana {{< /alternativa >}}
{{< alternativa >}} nome {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="A" >}}
A chave `"nome"` está associada ao valor `"Ana"`. Portanto, `aluno["nome"]` retorna `"Ana"`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
aluno = {
    "nome": "Ana",
    "idade": 20
}

print(aluno["idade"])
{{< /code >}}

{{< alternativa >}} Ana {{< /alternativa >}}
{{< alternativa >}} idade {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="C" >}}
A chave `"idade"` está associada ao valor `20`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Como acessar o valor associado a uma chave de um dicionário?

{{< alternativa >}} Utilizando um índice numérico. {{< /alternativa >}}
{{< alternativa >}} Utilizando a chave entre colchetes. {{< /alternativa >}}
{{< alternativa >}} Utilizando a chave entre parênteses. {{< /alternativa >}}
{{< alternativa >}} Utilizando obrigatoriamente o método `get()`. {{< /alternativa >}}
{{< solucao letra="B" >}}
Podemos acessar diretamente um valor utilizando sua chave entre colchetes, como em `aluno["nome"]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
produto = {
    "nome": "Caneta",
    "preco": 5
}

produto["preco"] = 7

print(produto["preco"])
{{< /code >}}

{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 7 {{< /alternativa >}}
{{< alternativa >}} preco {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
A atribuição `produto["preco"] = 7` altera o valor associado à chave `"preco"`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que acontece.

{{< code >}}
aluno = {
    "nome": "Ana",
    "idade": 20
}

aluno["curso"] = "Python"

print(aluno)
{{< /code >}}

{{< alternativa >}} Ocorre um erro porque a chave não existia. {{< /alternativa >}}
{{< alternativa >}} A chave `"curso"` é adicionada ao dicionário. {{< /alternativa >}}
{{< alternativa >}} O dicionário é apagado. {{< /alternativa >}}
{{< alternativa >}} O valor de `"nome"` é alterado. {{< /alternativa >}}
{{< solucao letra="B" >}}
Quando atribuímos um valor a uma chave que ainda não existe, um novo par chave-valor é adicionado ao dicionário.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método pode ser utilizado para adicionar um novo par de chave e valor a um dicionário?

{{< alternativa >}} `append()` {{< /alternativa >}}
{{< alternativa >}} `add()` {{< /alternativa >}}
{{< alternativa >}} Atribuição utilizando a chave. {{< /alternativa >}}
{{< alternativa >}} `insert()` {{< /alternativa >}}
{{< solucao letra="C" >}}
Podemos adicionar um novo item utilizando uma atribuição, como `aluno["curso"] = "Python"`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
aluno = {
    "nome": "Ana",
    "idade": 20
}

print("nome" in aluno)
{{< /code >}}

{{< alternativa >}} True {{< /alternativa >}}
{{< alternativa >}} False {{< /alternativa >}}
{{< alternativa >}} Ana {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="A" >}}
Ao utilizar `in` diretamente em um dicionário, a verificação é feita nas chaves. Como `"nome"` é uma chave do dicionário, o resultado é `True`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
aluno = {
    "nome": "Ana",
    "idade": 20
}

print("Ana" in aluno)
{{< /code >}}

{{< alternativa >}} True {{< /alternativa >}}
{{< alternativa >}} False {{< /alternativa >}}
{{< alternativa >}} Ana {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
O operador `in` verifica as chaves quando utilizado diretamente em um dicionário. `"Ana"` é um valor, e não uma chave.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método retorna todas as chaves de um dicionário?

{{< alternativa >}} `keys()` {{< /alternativa >}}
{{< alternativa >}} `values()` {{< /alternativa >}}
{{< alternativa >}} `items()` {{< /alternativa >}}
{{< alternativa >}} `get()` {{< /alternativa >}}
{{< solucao letra="A" >}}
O método `keys()` retorna uma visão contendo as chaves do dicionário.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método retorna todos os valores de um dicionário?

{{< alternativa >}} `keys()` {{< /alternativa >}}
{{< alternativa >}} `values()` {{< /alternativa >}}
{{< alternativa >}} `items()` {{< /alternativa >}}
{{< alternativa >}} `get()` {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `values()` retorna uma visão contendo os valores do dicionário.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método retorna os pares de chave e valor de um dicionário?

{{< alternativa >}} `keys()` {{< /alternativa >}}
{{< alternativa >}} `values()` {{< /alternativa >}}
{{< alternativa >}} `items()` {{< /alternativa >}}
{{< alternativa >}} `pairs()` {{< /alternativa >}}
{{< solucao letra="C" >}}
O método `items()` retorna os pares de chave e valor do dicionário.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
aluno = {
    "nome": "Ana",
    "idade": 20
}

for chave in aluno:
    print(chave)
{{< /code >}}

{{< alternativa >}} Os valores do dicionário. {{< /alternativa >}}
{{< alternativa >}} As chaves do dicionário. {{< /alternativa >}}
{{< alternativa >}} Apenas a primeira chave. {{< /alternativa >}}
{{< alternativa >}} O dicionário inteiro em cada repetição. {{< /alternativa >}}
{{< solucao letra="B" >}}
Ao percorrer diretamente um dicionário com `for`, cada repetição fornece uma chave.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
aluno = {
    "nome": "Ana",
    "idade": 20
}

for valor in aluno.values():
    print(valor)
{{< /code >}}

{{< alternativa >}} As chaves do dicionário. {{< /alternativa >}}
{{< alternativa >}} Os valores do dicionário. {{< /alternativa >}}
{{< alternativa >}} Os índices do dicionário. {{< /alternativa >}}
{{< alternativa >}} Ocorre um erro. {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `values()` permite percorrer os valores armazenados no dicionário.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
aluno = {
    "nome": "Ana",
    "idade": 20
}

for chave, valor in aluno.items():
    print(chave, valor)
{{< /code >}}

{{< alternativa >}} Apenas as chaves. {{< /alternativa >}}
{{< alternativa >}} Apenas os valores. {{< /alternativa >}}
{{< alternativa >}} As chaves e os valores. {{< /alternativa >}}
{{< alternativa >}} O dicionário será apagado. {{< /alternativa >}}
{{< solucao letra="C" >}}
O método `items()` permite percorrer simultaneamente cada chave e seu respectivo valor.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método pode ser utilizado para obter o valor associado a uma chave sem gerar erro caso a chave não exista?

{{< alternativa >}} `find()` {{< /alternativa >}}
{{< alternativa >}} `get()` {{< /alternativa >}}
{{< alternativa >}} `search()` {{< /alternativa >}}
{{< alternativa >}} `value()` {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `get()` permite acessar um valor pela chave. Caso a chave não exista, retorna `None` por padrão em vez de gerar um erro.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
aluno = {
    "nome": "Ana",
    "idade": 20
}

print(aluno.get("curso"))
{{< /code >}}

{{< alternativa >}} Python {{< /alternativa >}}
{{< alternativa >}} curso {{< /alternativa >}}
{{< alternativa >}} None {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="C" >}}
A chave `"curso"` não existe no dicionário. Como `get()` foi utilizado sem um valor padrão, o resultado será `None`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método pode ser utilizado para remover um elemento de um dicionário informando sua chave?

{{< alternativa >}} `remove()` {{< /alternativa >}}
{{< alternativa >}} `pop()` {{< /alternativa >}}
{{< alternativa >}} `discard()` {{< /alternativa >}}
{{< alternativa >}} `delete()` {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `pop()` remove o item associado à chave informada e retorna o valor removido.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
aluno = {
    "nome": "Ana",
    "idade": 20
}

idade = aluno.pop("idade")

print(idade)
{{< /code >}}

{{< alternativa >}} Ana {{< /alternativa >}}
{{< alternativa >}} idade {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} None {{< /alternativa >}}
{{< solucao letra="C" >}}
`pop("idade")` remove o item `"idade"` e retorna o valor associado a ele, que é `20`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método remove todos os elementos de um dicionário?

{{< alternativa >}} `remove()` {{< /alternativa >}}
{{< alternativa >}} `delete()` {{< /alternativa >}}
{{< alternativa >}} `clear()` {{< /alternativa >}}
{{< alternativa >}} `empty()` {{< /alternativa >}}
{{< solucao letra="C" >}}
O método `clear()` remove todos os elementos do dicionário.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
produto = {
    "nome": "Caneta",
    "preco": 5
}

produto["estoque"] = 10

print(len(produto))
{{< /code >}}

{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< solucao letra="C" >}}
O dicionário começa com duas chaves. A atribuição de `"estoque"` adiciona uma terceira chave.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
aluno = {
    "nome": "Ana",
    "idade": 20,
    "notas": [8, 9, 7]
}

print(aluno["notas"][1])
{{< /code >}}

{{< alternativa >}} 8 {{< /alternativa >}}
{{< alternativa >}} 9 {{< /alternativa >}}
{{< alternativa >}} 7 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
A chave `"notas"` contém uma lista. O índice 1 dessa lista corresponde ao valor `9`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Considere o seguinte dicionário:

{{< code >}}
aluno = {
    "nome": "Ana",
    "notas": {
        "programacao": 9,
        "matematica": 8
    }
}
{{< /code >}}

Qual expressão acessa a nota de programação?

{{< alternativa >}} `aluno["programacao"]` {{< /alternativa >}}
{{< alternativa >}} `aluno["notas"]` {{< /alternativa >}}
{{< alternativa >}} `aluno["notas"]["programacao"]` {{< /alternativa >}}
{{< alternativa >}} `aluno["programacao"]["notas"]` {{< /alternativa >}}
{{< solucao letra="C" >}}
A chave `"notas"` contém outro dicionário. Para acessar `"programacao"`, é necessário acessar os dois níveis: `aluno["notas"]["programacao"]`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
aluno = {
    "nome": "Ana",
    "idade": 20
}

print(aluno.get("idade"))
{{< /code >}}

{{< alternativa >}} Ana {{< /alternativa >}}
{{< alternativa >}} idade {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} None {{< /alternativa >}}
{{< solucao letra="C" >}}
A chave `"idade"` existe e está associada ao valor `20`. Portanto, `get("idade")` retorna `20`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
produto = {
    "nome": "Caneta",
    "preco": 5
}

if "estoque" in produto:
    print("Existe")
else:
    print("Não existe")
{{< /code >}}

{{< alternativa >}} Existe {{< /alternativa >}}
{{< alternativa >}} Não existe {{< /alternativa >}}
{{< alternativa >}} estoque {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
A chave `"estoque"` não existe no dicionário. Portanto, a condição é falsa e o `else` é executado.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
aluno = {
    "nome": "Ana",
    "idade": 20
}

del aluno["idade"]

print(len(aluno))
{{< /code >}}

{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 1 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
A instrução `del aluno["idade"]` remove a chave `"idade"` e seu valor. Resta apenas a chave `"nome"`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual afirmação sobre as chaves de um dicionário está correta?

{{< alternativa >}} Um dicionário pode possuir várias ocorrências da mesma chave. {{< /alternativa >}}
{{< alternativa >}} As chaves são utilizadas para acessar os valores armazenados. {{< /alternativa >}}
{{< alternativa >}} As chaves só podem ser Strings. {{< /alternativa >}}
{{< alternativa >}} As chaves são acessadas obrigatoriamente por índices numéricos. {{< /alternativa >}}
{{< solucao letra="B" >}}
As chaves identificam os valores armazenados no dicionário e são utilizadas para acessá-los.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
aluno = {
    "nome": "Ana",
    "idade": 20
}

aluno["nome"] = "Carlos"

print(aluno["nome"])
{{< /code >}}

{{< alternativa >}} Ana {{< /alternativa >}}
{{< alternativa >}} Carlos {{< /alternativa >}}
{{< alternativa >}} nome {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
A chave `"nome"` já existe. A atribuição altera o valor associado a ela para `"Carlos"`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
aluno = {
    "nome": "Ana",
    "idade": 20
}

for chave in aluno.keys():
    print(chave)
{{< /code >}}

{{< alternativa >}} Os valores do dicionário. {{< /alternativa >}}
{{< alternativa >}} As chaves do dicionário. {{< /alternativa >}}
{{< alternativa >}} Os pares chave e valor. {{< /alternativa >}}
{{< alternativa >}} Os índices do dicionário. {{< /alternativa >}}
{{< solucao letra="B" >}}
O método `keys()` permite percorrer as chaves do dicionário.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o resultado.

{{< code >}}
aluno = {
    "nome": "Ana",
    "idade": 20
}

for chave, valor in aluno.items():
    print(valor)
{{< /code >}}

{{< alternativa >}} nome e idade {{< /alternativa >}}
{{< alternativa >}} Ana e 20 {{< /alternativa >}}
{{< alternativa >}} chave e valor {{< /alternativa >}}
{{< alternativa >}} Ocorre um erro. {{< /alternativa >}}
{{< solucao letra="B" >}}
`items()` fornece cada par de chave e valor. Como o código imprime apenas `valor`, serão impressos `"Ana"` e `20`.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual estrutura é mais adequada para representar informações de uma pessoa utilizando nomes para identificar cada informação?

{{< alternativa >}} Lista. {{< /alternativa >}}
{{< alternativa >}} Tupla. {{< /alternativa >}}
{{< alternativa >}} Conjunto. {{< /alternativa >}}
{{< alternativa >}} Dicionário. {{< /alternativa >}}
{{< solucao letra="D" >}}
Um dicionário é adequado para representar informações associadas a nomes, como `"nome"`, `"idade"` e `"email"`.
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

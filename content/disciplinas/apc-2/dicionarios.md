---

title: "Dicionários"
description: "Estrutura de dados utilizada para representar coleções de pares chave-valor em Python"
slug: dicionarios
tags:
  - estruturas-de-dados
  - dicionários
  - python
  - dict
---

Um **dicionário** (`dict`) é uma estrutura de dados utilizada para representar uma coleção de **pares chave-valor** em Python.

Enquanto uma lista utiliza posições para acessar seus elementos, um dicionário utiliza **chaves**.

Por exemplo:

```python id="2o7b0u"
pessoa = {
    "nome": "Ana",
    "idade": 25,
    "cidade": "Joinville"
}
```

Nesse caso, temos três pares:

```text id="c3x1rt"
"nome"   → "Ana"
"idade"  → 25
"cidade" → "Joinville"
```

A chave identifica o valor que queremos acessar.

## Estrutura

Um dicionário é representado por elementos entre chaves `{}`.

Cada elemento possui uma chave e um valor, separados por `:`:

```python id="0l3n7y"
pessoa = {
    "nome": "Ana",
    "idade": 25
}
```

Podemos representar sua estrutura da seguinte forma:

```text id="5h5yph"
        Dicionário
       ┌──────────────────┐
       │ "nome"  → "Ana"  │
       │ "idade" → 25     │
       └──────────────────┘
```

A chave é utilizada para localizar o valor correspondente.

## Criação de dicionários

Um dicionário pode ser criado utilizando chaves:

```python id="6n9y9p"
pessoa = {
    "nome": "Ana",
    "idade": 25
}
```

Também podemos criar um dicionário vazio:

```python id="h6qz0t"
dados = {}
```

Ou utilizando o construtor `dict()`:

```python id="0l5b9w"
dados = dict()
```

Também podemos criar um dicionário diretamente com `dict()`:

```python id="r2e5hk"
pessoa = dict(nome="Ana", idade=25)

print(pessoa)
```

Resultado:

```text
{'nome': 'Ana', 'idade': 25}
```

## Chaves

Cada chave identifica um valor dentro do dicionário.

Por exemplo:

```python id="7y3q4a"
produto = {
    "nome": "Notebook",
    "preco": 3500,
    "estoque": 10
}
```

Temos as chaves:

```text id="6a8d0s"
nome
preco
estoque
```

E seus respectivos valores:

```text id="xv9w6e"
Notebook
3500
10
```

Uma chave não pode aparecer mais de uma vez no mesmo dicionário.

Se uma chave for informada novamente, seu valor será atualizado:

```python id="1f8j0y"
pessoa = {
    "nome": "Ana",
    "idade": 25
}

pessoa["idade"] = 26

print(pessoa)
```

Resultado:

```text
{'nome': 'Ana', 'idade': 26}
```

## Acesso aos valores

Podemos acessar um valor utilizando sua chave:

```python id="c4m1vy"
pessoa = {
    "nome": "Ana",
    "idade": 25
}

print(pessoa["nome"])
print(pessoa["idade"])
```

Resultado:

```text
Ana
25
```

A expressão:

```python id="3d8xj4"
pessoa["nome"]
```

significa:

> obtenha o valor associado à chave `"nome"`.

Se tentarmos acessar uma chave que não existe, será gerada uma exceção `KeyError`:

```python id="x5f7re"
print(pessoa["cidade"])
```

## Acesso utilizando `get()`

O método `get()` também permite acessar um valor.

```python id="d6q5pj"
pessoa = {
    "nome": "Ana",
    "idade": 25
}

print(pessoa.get("nome"))
```

Resultado:

```text
Ana
```

A principal diferença é o comportamento quando a chave não existe.

Com `[]`:

```python id="v4j1z2"
print(pessoa["cidade"])
```

ocorre um `KeyError`.

Com `get()`:

```python id="8j6f6s"
print(pessoa.get("cidade"))
```

o resultado é:

```text
None
```

Também podemos definir um valor padrão:

```python id="0d7s8w"
print(pessoa.get("cidade", "Não informado"))
```

Resultado:

```text
Não informado
```

## Adicionar elementos

Podemos adicionar um novo par chave-valor utilizando a atribuição:

```python id="v4c8z9"
pessoa = {
    "nome": "Ana",
    "idade": 25
}

pessoa["cidade"] = "Joinville"

print(pessoa)
```

Resultado:

```text
{'nome': 'Ana', 'idade': 25, 'cidade': 'Joinville'}
```

Se a chave já existir, seu valor será atualizado:

```python id="f9v2sa"
pessoa["idade"] = 26
```

Portanto, a mesma sintaxe pode ser utilizada tanto para **adicionar** quanto para **atualizar** um elemento.

## Atualizar elementos

Podemos atualizar diretamente um valor:

```python id="b9k9e3"
produto = {
    "nome": "Notebook",
    "preco": 3500
}

produto["preco"] = 3200

print(produto)
```

Resultado:

```text
{'nome': 'Notebook', 'preco': 3200}
```

Também podemos utilizar `update()` para atualizar vários valores:

```python id="m3k2f4"
produto.update({
    "preco": 3200,
    "estoque": 15
})
```

## Remover elementos

O método `pop()` remove um elemento utilizando sua chave e retorna o valor removido:

```python id="w8r4l5"
pessoa = {
    "nome": "Ana",
    "idade": 25,
    "cidade": "Joinville"
}

cidade = pessoa.pop("cidade")

print(cidade)
print(pessoa)
```

Resultado:

```text
Joinville
{'nome': 'Ana', 'idade': 25}
```

Também podemos utilizar `del`:

```python id="f0j7q3"
del pessoa["idade"]

print(pessoa)
```

Se quisermos remover todos os elementos, podemos utilizar `clear()`:

```python id="x3h2s7"
pessoa.clear()

print(pessoa)
```

Resultado:

```text
{}
```

## Verificar se uma chave existe

O operador `in` verifica se uma chave pertence ao dicionário:

```python id="y6q9k2"
pessoa = {
    "nome": "Ana",
    "idade": 25
}

print("nome" in pessoa)
```

Resultado:

```text
True
```

Também podemos utilizar `not in`:

```python id="w8r5q1"
print("cidade" not in pessoa)
```

Resultado:

```text
True
```

É importante perceber que o `in` verifica as **chaves**, e não os valores:

```python id="s8q2m6"
print("Ana" in pessoa)
```

Resultado:

```text
False
```

## Tamanho do dicionário

A função `len()` retorna a quantidade de pares chave-valor:

```python id="p4r7c2"
pessoa = {
    "nome": "Ana",
    "idade": 25,
    "cidade": "Joinville"
}

print(len(pessoa))
```

Resultado:

```text
3
```

## Obter as chaves

O método `keys()` retorna as chaves do dicionário:

```python id="r7m3w5"
pessoa = {
    "nome": "Ana",
    "idade": 25,
    "cidade": "Joinville"
}

print(pessoa.keys())
```

Podemos percorrer as chaves utilizando `for`:

```python id="d2y8n6"
for chave in pessoa.keys():
    print(chave)
```

Resultado:

```text
nome
idade
cidade
```

Como `keys()` é iterável, também é comum escrever diretamente:

```python id="j3v5x8"
for chave in pessoa:
    print(chave)
```

## Obter os valores

O método `values()` permite acessar os valores:

```python id="k6p2v9"
pessoa = {
    "nome": "Ana",
    "idade": 25,
    "cidade": "Joinville"
}

print(pessoa.values())
```

Também podemos percorrer os valores:

```python id="q4n8z1"
for valor in pessoa.values():
    print(valor)
```

Resultado:

```text
Ana
25
Joinville
```

## Obter chaves e valores

O método `items()` permite percorrer os pares chave-valor:

```python id="u7y2p5"
pessoa = {
    "nome": "Ana",
    "idade": 25,
    "cidade": "Joinville"
}

for chave, valor in pessoa.items():
    print(chave, valor)
```

Resultado:

```text
nome Ana
idade 25
cidade Joinville
```

Essa é uma forma bastante utilizada quando precisamos trabalhar simultaneamente com a chave e o valor.

## Dicionários podem armazenar diferentes tipos

Os valores de um dicionário podem ser de diferentes tipos:

```python id="k9s5d3"
dados = {
    "nome": "Ana",
    "idade": 25,
    "altura": 1.68,
    "ativo": True
}
```

Também podemos armazenar listas:

```python id="x6v3n1"
aluno = {
    "nome": "Ana",
    "notas": [8, 9, 10]
}
```

Nesse caso:

```python id="g5t8w2"
print(aluno["notas"])
```

Resultado:

```text
[8, 9, 10]
```

Podemos acessar diretamente um elemento da lista:

```python id="m2k7q4"
print(aluno["notas"][0])
```

Resultado:

```text
8
```

Também podemos armazenar outros dicionários:

```python id="c8w4n6"
aluno = {
    "nome": "Ana",
    "endereco": {
        "cidade": "Joinville",
        "estado": "SC"
    }
}
```

Para acessar a cidade:

```python id="v9p3s7"
print(aluno["endereco"]["cidade"])
```

Resultado:

```text
Joinville
```

## Dicionários aninhados

Quando um dicionário contém outros dicionários, temos uma estrutura de **dicionários aninhados**.

Por exemplo:

```python id="e5k8r2"
alunos = {
    "001": {
        "nome": "Ana",
        "idade": 20
    },
    "002": {
        "nome": "Bruno",
        "idade": 22
    }
}
```

Podemos acessar os dados de um aluno utilizando as chaves:

```python id="q6m1z9"
print(alunos["001"]["nome"])
```

Resultado:

```text
Ana
```

## Percorrer um dicionário

Podemos percorrer diretamente as chaves:

```python id="a4s7x2"
pessoa = {
    "nome": "Ana",
    "idade": 25,
    "cidade": "Joinville"
}

for chave in pessoa:
    print(chave)
```

Para acessar também os valores:

```python id="n8q3v5"
for chave in pessoa:
    print(chave, pessoa[chave])
```

Ou utilizando `items()`:

```python id="r5k2m8"
for chave, valor in pessoa.items():
    print(chave, valor)
```

## Ordenação

Dicionários preservam a ordem de inserção dos elementos.

Por exemplo:

```python id="h7m4q2"
pessoa = {
    "nome": "Ana",
    "idade": 25,
    "cidade": "Joinville"
}

for chave, valor in pessoa.items():
    print(chave, valor)
```

Os elementos serão percorridos na ordem em que foram inseridos.

É importante, porém, diferenciar isso de uma lista: o acesso aos valores de um dicionário é feito principalmente **por chave**, e não pela posição.

## Exemplo prático

Podemos utilizar um dicionário para representar um produto:

```python id="v4x8n2"
produto = {
    "nome": "Notebook",
    "preco": 3500,
    "estoque": 10
}
```

Podemos consultar o preço:

```python id="f6q3y8"
print(produto["preco"])
```

Atualizar o preço:

```python id="j9w2m5"
produto["preco"] = 3200
```

Adicionar uma nova informação:

```python id="r3k7p1"
produto["categoria"] = "Informática"
```

E percorrer todos os dados:

```python id="t8v4c6"
for chave, valor in produto.items():
    print(f"{chave}: {valor}")
```

Resultado:

```text
nome: Notebook
preco: 3200
estoque: 10
categoria: Informática
```

## Principais métodos

| Método     | Função                               |
| ---------- | ------------------------------------ |
| `get()`    | Obtém um valor a partir de uma chave |
| `keys()`   | Retorna as chaves                    |
| `values()` | Retorna os valores                   |
| `items()`  | Retorna os pares chave-valor         |
| `update()` | Adiciona ou atualiza elementos       |
| `pop()`    | Remove um elemento pela chave        |
| `clear()`  | Remove todos os elementos            |

Também podemos utilizar:

| Operação      | Função                           |
| ------------- | -------------------------------- |
| `dict[chave]` | Acessa ou modifica um valor      |
| `in`          | Verifica se uma chave existe     |
| `not in`      | Verifica se uma chave não existe |
| `len()`       | Retorna a quantidade de pares    |

## Exemplo completo

O exemplo abaixo demonstra algumas das principais operações realizadas com um dicionário:

```python id="s5n8k3"
aluno = {
    "nome": "Ana",
    "idade": 20,
    "curso": "Computação"
}

print("Dados do aluno:")
print(aluno)

print("\nNome:")
print(aluno["nome"])

aluno["idade"] = 21

print("\nApós atualizar a idade:")
print(aluno)

aluno["cidade"] = "Joinville"

print("\nApós adicionar a cidade:")
print(aluno)

print("\nChaves:")
for chave in aluno.keys():
    print(chave)

print("\nValores:")
for valor in aluno.values():
    print(valor)

print("\nDados:")
for chave, valor in aluno.items():
    print(f"{chave}: {valor}")

aluno.pop("cidade")

print("\nApós remover a cidade:")
print(aluno)
```

## Conclusão

O `dict` é uma estrutura de dados utilizada para representar **coleções de pares chave-valor**.

Suas principais características são:

* Os dados são organizados em pares chave-valor.
* As chaves identificam os valores.
* Uma chave não pode aparecer mais de uma vez.
* Uma chave existente pode ter seu valor atualizado.
* É possível adicionar e remover pares.
* O acesso aos valores é realizado utilizando suas chaves.
* Os valores podem ser de diferentes tipos.
* Dicionários podem conter listas e outros dicionários.
* Podemos percorrer chaves, valores ou pares chave-valor.

A principal ideia é:

```text
chave → valor
```

Por exemplo:

```python id="h3q7w9"
aluno = {
    "nome": "Ana",
    "idade": 20
}
```

Nesse caso:

```text
"nome" → "Ana"
"idade" → 20
```

O dicionário é especialmente útil quando queremos representar informações em que cada valor possui uma **identificação** que permite localizá-lo.

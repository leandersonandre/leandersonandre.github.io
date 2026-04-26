---
title: "Questões Formatação de Números"
slug: formatacao-de-numeros-questoes
description: "Questões sobre Formatação de números em Python"
tags:
- python
- format
- round
- questões
---
{{< questao >}}
Qual método é utilizado para formatar números em strings em Python moderno?

{{< alternativa >}} printf {{< /alternativa >}}
{{< alternativa >}} format() {{< /alternativa >}}
{{< alternativa >}} f-string {{< /alternativa >}}
{{< alternativa >}} Ambas B e C {{< /alternativa >}}
{{< solucao letra="D" >}}
Tanto format() quanto f-strings são utilizados para formatação de números.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será a saída de:
{{< code >}}
 x = 10
 print(f"{x}")
{{< /code >}}

{{< alternativa >}} x {{< /alternativa >}}
{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} {x} {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
O valor da variável x é inserido na string.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será a saída de:
{{< code >}}
 x = 3.14159
 print(f"{x:.2f}")
{{< /code >}}

{{< alternativa >}} 3.14 {{< /alternativa >}}
{{< alternativa >}} 3.14159 {{< /alternativa >}}
{{< alternativa >}} 3.1 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< solucao letra="A" >}}
:.2f formata o número com duas casas decimais.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que significa o formato ".2f"?

{{< alternativa >}} Número inteiro com 2 dígitos {{< /alternativa >}}
{{< alternativa >}} Número com 2 casas decimais {{< /alternativa >}}
{{< alternativa >}} Número multiplicado por 2 {{< /alternativa >}}
{{< alternativa >}} Número dividido por 2 {{< /alternativa >}}
{{< solucao letra="B" >}}
Indica duas casas decimais no formato float.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será a saída de:
{{< code >}}
 x = 5
 print(f"{x:03}")
{{< /code >}}

{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 005 {{< /alternativa >}}
{{< alternativa >}} 500 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
O número é preenchido com zeros à esquerda.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será a saída de:
{{< code >}}
 x = 42
 print(f"{x:5}")
{{< /code >}}

{{< alternativa >}} "42" {{< /alternativa >}}
{{< alternativa >}} "   42" {{< /alternativa >}}
{{< alternativa >}} "42   " {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
O número é alinhado à direita em um campo de largura 5.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual formatação alinha o número à esquerda?

{{< alternativa >}} {:>5} {{< /alternativa >}}
{{< alternativa >}} {:<5} {{< /alternativa >}}
{{< alternativa >}} {:^5} {{< /alternativa >}}
{{< alternativa >}} {:05} {{< /alternativa >}}
{{< solucao letra="B" >}}
:< alinha à esquerda.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual formatação centraliza o número?

{{< alternativa >}} {:>5} {{< /alternativa >}}
{{< alternativa >}} {:<5} {{< /alternativa >}}
{{< alternativa >}} {:^5} {{< /alternativa >}}
{{< alternativa >}} {:05} {{< /alternativa >}}
{{< solucao letra="C" >}}
:^ centraliza o valor.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será a saída de:
{{< code >}}
 x = 1234
 print(f"{x:,}")
{{< /code >}}

{{< alternativa >}} 1234 {{< /alternativa >}}
{{< alternativa >}} 1,234 {{< /alternativa >}}
{{< alternativa >}} 1.234 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="B" >}}
A vírgula separa milhares no padrão internacional.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será a saída de:
{{< code >}}
 x = 0.75
 print(f"{x:.0%}")
{{< /code >}}

{{< alternativa >}} 0.75% {{< /alternativa >}}
{{< alternativa >}} 75% {{< /alternativa >}}
{{< alternativa >}} 0% {{< /alternativa >}}
{{< alternativa >}} 750% {{< /alternativa >}}
{{< solucao letra="B" >}}
O valor é convertido para porcentagem.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será a saída de:
{{< code >}}
 x = 0.756
 print(f"{x:.1%}")
{{< /code >}}

{{< alternativa >}} 75.6% {{< /alternativa >}}
{{< alternativa >}} 0.7% {{< /alternativa >}}
{{< alternativa >}} 76% {{< /alternativa >}}
{{< alternativa >}} 7.5% {{< /alternativa >}}
{{< solucao letra="A" >}}
Multiplica por 100 e mantém uma casa decimal.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será a saída de:
{{< code >}}
 x = 10
 y = 3
 print(f"{x/y:.2f}")
{{< /code >}}

{{< alternativa >}} 3.33 {{< /alternativa >}}
{{< alternativa >}} 3.3 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 3.3333 {{< /alternativa >}}
{{< solucao letra="A" >}}
Resultado da divisão formatado com duas casas decimais.
{{< /solucao >}}
{{< /questao >}}

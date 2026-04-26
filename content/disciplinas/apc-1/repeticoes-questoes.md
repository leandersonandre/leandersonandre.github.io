---
title: "Questões sobre Repetições"
description: "Questões sobre Estrutura de repetições em Python"
slug: repeticoes-questoes
tags:
- python
- while-for
- repetições
- questões
---

{{< lista-questoes >}}

{{< questao >}}
O que é uma estrutura de repetição?
{{< alternativa >}} Uma estrutura para controlar o fluxo de execução do código. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura para repetir a execução de um trecho de código. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura para a execução sequencial do código. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que permite reutilizar um trecho de código. {{< /alternativa >}}
{{< solucao letra="B" >}}
Uma estrutura que permite repetir de maneira controlada um determinado trecho de código.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso no terminal.

{{< code >}}
for i in range(5):
  print(i)
{{< /code >}}

{{< alternativa >}} 0 1 2 3 4 {{< /alternativa >}}
{{< alternativa >}} 1 2 3 4 5 {{< /alternativa >}}
{{< alternativa >}} i i i i i {{< /alternativa >}}
{{< alternativa >}} 5 5 5 5 5 {{< /alternativa >}}
{{< solucao letra="A" >}}
Irá imprimir no terminal os número 0 até 4.
{{< /solucao >}}
{{< /questao >}}




{{< questao >}}
Qual estrutura de repetição é mais indicada quando não se sabe o número exato de repetições?
{{< alternativa >}} for {{< /alternativa >}}
{{< alternativa >}} while {{< /alternativa >}}
{{< alternativa >}} if {{< /alternativa >}}
{{< alternativa >}} else {{< /alternativa >}}
{{< solucao letra="B" >}}
A estrutura while é utilizada quando não se sabe previamente quantas vezes o laço será executado.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso no terminal.

{{< code >}}
i = 0
while i < 3:
  print(i)
  i = i + 1
{{< /code >}}

{{< alternativa >}} 0 1 2 {{< /alternativa >}}
{{< alternativa >}} 1 2 3 {{< /alternativa >}}
{{< alternativa >}} 0 1 2 3 {{< /alternativa >}}
{{< alternativa >}} Loop infinito {{< /alternativa >}}
{{< solucao letra="A" >}}
O laço inicia em 0 e executa enquanto i < 3, imprimindo 0, 1 e 2.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a função do comando break em um laço?
{{< alternativa >}} Reiniciar o laço {{< /alternativa >}}
{{< alternativa >}} Pular uma iteração {{< /alternativa >}}
{{< alternativa >}} Encerrar o laço imediatamente {{< /alternativa >}}
{{< alternativa >}} Repetir o laço infinitamente {{< /alternativa >}}
{{< solucao letra="C" >}}
O break interrompe a execução do laço imediatamente.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso no terminal.

{{< code >}}
for i in range(2, 6):
  print(i)
{{< /code >}}

{{< alternativa >}} 2 3 4 5 {{< /alternativa >}}
{{< alternativa >}} 2 3 4 5 6 {{< /alternativa >}}
{{< alternativa >}} 1 2 3 4 5 {{< /alternativa >}}
{{< alternativa >}} 2 4 6 {{< /alternativa >}}
{{< solucao letra="A" >}}
O range(2, 6) gera valores de 2 até 5.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será a saída do código abaixo?

{{< code >}}
for i in range(0, 5, 2):
  print(i)
{{< /code >}}

{{< alternativa >}} 0 1 2 3 4 {{< /alternativa >}}
{{< alternativa >}} 0 2 4 {{< /alternativa >}}
{{< alternativa >}} 1 3 5 {{< /alternativa >}}
{{< alternativa >}} 0 2 4 6 {{< /alternativa >}}
{{< solucao letra="B" >}}
O passo é 2, então os valores gerados são 0, 2 e 4.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual será a saída do código abaixo?

{{< code >}}
for i in range(5, 0, -1):
  print(i)
{{< /code >}}

{{< alternativa >}} 5 4 3 2 1 {{< /alternativa >}}
{{< alternativa >}} 5 4 3 2 1 0 {{< /alternativa >}}
{{< alternativa >}} 0 1 2 3 4 5 {{< /alternativa >}}
{{< alternativa >}} Loop infinito {{< /alternativa >}}
{{< solucao letra="A" >}}
O range inicia em 5 e decrementa até 1 (0 não é incluído).
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a função do comando continue em um laço?
{{< alternativa >}} Encerrar o laço {{< /alternativa >}}
{{< alternativa >}} Pular a iteração atual {{< /alternativa >}}
{{< alternativa >}} Reiniciar o laço {{< /alternativa >}}
{{< alternativa >}} Parar o programa {{< /alternativa >}}
{{< solucao letra="B" >}}
O continue pula a iteração atual e continua para a próxima.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso.

{{< code >}}
soma = 0
for i in range(1, 4):
  soma = soma + i
print(soma)
{{< /code >}}

{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 6 {{< /alternativa >}}
{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 0 {{< /alternativa >}}
{{< solucao letra="B" >}}
O acumulador soma os valores 1 + 2 + 3, resultando em 6.
{{< /solucao >}}
{{< /questao >}}



{{< questao >}}
Analise o código e identifique o que será impresso no terminal.

{{< code >}}
soma = 0
for i in range(1, 6):
  soma = soma + i
print(soma)
{{< /code >}}

{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 15 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< solucao letra="B" >}}
O acumulador soma os valores de 1 até 5: 1 + 2 + 3 + 4 + 5 = 15.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso no terminal.

{{< code >}}
for i in range(5):
  if i == 2:
    continue
  print(i)
{{< /code >}}

{{< alternativa >}} 0 1 2 3 4 {{< /alternativa >}}
{{< alternativa >}} 0 1 3 4 {{< /alternativa >}}
{{< alternativa >}} 2 3 4 {{< /alternativa >}}
{{< alternativa >}} 0 1 2 {{< /alternativa >}}
{{< solucao letra="B" >}}
O valor 2 é pulado por causa do continue.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso no terminal.

{{< code >}}
for i in range(3):
  print(i, end=" ")
{{< /code >}}

O que será exibido?
{{< alternativa >}} 0 1 2 {{< /alternativa >}}
{{< alternativa >}} 0 1 2 (em linhas separadas) {{< /alternativa >}}
{{< alternativa >}} 1 2 3 {{< /alternativa >}}
{{< alternativa >}} Erro {{< /alternativa >}}
{{< solucao letra="A" >}}
O parâmetro end=" " impede a quebra de linha.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso no terminal.

{{< code >}}
for i in range(3):
  print(i)
else:
  print("Fim")
{{< /code >}}

{{< alternativa >}} 0 1 2 {{< /alternativa >}}
{{< alternativa >}} 0 1 2 Fim {{< /alternativa >}}
{{< alternativa >}} Fim {{< /alternativa >}}
{{< alternativa >}} Loop infinito {{< /alternativa >}}
{{< solucao letra="B" >}}
O else é executado porque o laço termina normalmente.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso no terminal.

{{< code >}}
for i in range(3):
  if i == 1:
    break
  print(i)
else:
  print("Fim")
{{< /code >}}

{{< alternativa >}} 0 1 Fim {{< /alternativa >}}
{{< alternativa >}} 0 Fim {{< /alternativa >}}
{{< alternativa >}} 0 {{< /alternativa >}}
{{< alternativa >}} 0 1 {{< /alternativa >}}
{{< solucao letra="C" >}}
O break impede a execução do else.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso no terminal.

{{< code >}}
for i in range(5, 0, -2):
  print(i)
{{< /code >}}

{{< alternativa >}} 5 3 1 {{< /alternativa >}}
{{< alternativa >}} 5 4 3 2 1 {{< /alternativa >}}
{{< alternativa >}} 0 2 4 {{< /alternativa >}}
{{< alternativa >}} 5 3 {{< /alternativa >}}
{{< solucao letra="A" >}}
O passo é -2, então os valores são 5, 3 e 1.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso no terminal.

{{< code >}}
for i in range(2):
  for j in range(2):
    print(i, j)
{{< /code >}}

Quantas linhas serão impressas?
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} 3 {{< /alternativa >}}
{{< alternativa >}} 4 {{< /alternativa >}}
{{< alternativa >}} 5 {{< /alternativa >}}
{{< solucao letra="C" >}}
O laço interno executa 2 vezes para cada iteração do externo: 2 x 2 = 4.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso no terminal.

{{< code >}}
for i in range(5):
  if i % 2 == 0:
    print(i)
{{< /code >}}

{{< alternativa >}} 1 3 5 {{< /alternativa >}}
{{< alternativa >}} 0 2 4 {{< /alternativa >}}
{{< alternativa >}} 2 4 {{< /alternativa >}}
{{< alternativa >}} 0 1 2 3 4 {{< /alternativa >}}
{{< solucao letra="B" >}}
A condição imprime apenas números pares.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código e identifique o que será impresso no terminal.

{{< code >}}
soma = 0
for i in range(1, 6):
  if i % 2 == 0:
    soma = soma + i
print(soma)
{{< /code >}}

{{< alternativa >}} 6 {{< /alternativa >}}
{{< alternativa >}} 9 {{< /alternativa >}}
{{< alternativa >}} 15 {{< /alternativa >}}
{{< alternativa >}} 10 {{< /alternativa >}}
{{< solucao letra="A" >}}
Somente os pares são somados: 2 + 4 = 6.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique em qual linha ocorre erro.

{{< code >}}
1 total = 0
2 for i in range(5)
3     total += i
4 print(total)
{{< /code >}}

{{< alternativa >}} Linha 1 {{< /alternativa >}}
{{< alternativa >}} Linha 2 {{< /alternativa >}}
{{< alternativa >}} Linha 3 {{< /alternativa >}}
{{< alternativa >}} Linha 4 {{< /alternativa >}}
{{< solucao letra="B" >}}
Falta o “:” no final do for.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique em qual linha ocorre erro.

{{< code >}}
1 for i in range(3):
2 print(i)
3   print("fim")
{{< /code >}}

{{< alternativa >}} Linha 1 {{< /alternativa >}}
{{< alternativa >}} Linha 2 {{< /alternativa >}}
{{< alternativa >}} Linha 3 {{< /alternativa >}}
{{< alternativa >}} Não há erro {{< /alternativa >}}
{{< solucao letra="B" >}}
A linha 2 deveria estar indentada dentro do for.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique em qual linha ocorre erro.

{{< code >}}
1 soma = 0
2 for i in range(1, 6):
3     soma = soma + i
4 print(soma
{{< /code >}}

{{< alternativa >}} Linha 1 {{< /alternativa >}}
{{< alternativa >}} Linha 2 {{< /alternativa >}}
{{< alternativa >}} Linha 3 {{< /alternativa >}}
{{< alternativa >}} Linha 4 {{< /alternativa >}}
{{< solucao letra="D" >}}
Falta fechar o parêntese no print.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique em qual linha ocorre erro.

{{< code >}}
1 for i in range(5):
2     if i == 3
3         continue
4     print(i)
{{< /code >}}

{{< alternativa >}} Linha 1 {{< /alternativa >}}
{{< alternativa >}} Linha 2 {{< /alternativa >}}
{{< alternativa >}} Linha 3 {{< /alternativa >}}
{{< alternativa >}} Linha 4 {{< /alternativa >}}
{{< solucao letra="B" >}}
Falta “:” no if.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique em qual linha ocorre erro.

{{< code >}}
1 for i in range(5, 0, 1):
2     print(i)
{{< /code >}}

{{< alternativa >}} Linha 1 {{< /alternativa >}}
{{< alternativa >}} Linha 2 {{< /alternativa >}}
{{< alternativa >}} Não há erro de sintaxe {{< /alternativa >}}
{{< alternativa >}} Ambas {{< /alternativa >}}
{{< solucao letra="C" >}}
Não há erro de sintaxe, mas o step está incorreto para regressivo (deveria ser negativo).
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo e identifique em qual linha ocorre erro.

{{< code >}}
1 i = 0
2 while i < 3:
3     print(i)
4 else:
5     print("fim")
6     i += 1
{{< /code >}}

{{< alternativa >}} Linha 2 {{< /alternativa >}}
{{< alternativa >}} Linha 3 {{< /alternativa >}}
{{< alternativa >}} Linha 6 {{< /alternativa >}}
{{< alternativa >}} Não há erro {{< /alternativa >}}
{{< solucao letra="C" >}}
O incremento deveria estar dentro do while, senão gera loop infinito.
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

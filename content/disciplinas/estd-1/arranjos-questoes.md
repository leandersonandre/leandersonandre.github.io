---
title: "Questões sobre Arranjos (Arrays)"
description: "Questões sobre  arranjos na linguagem Java"
slug: arranjos-questoes
tags:
- java
- arrays
- questões
---


{{< questao >}}
O que é um array em Java?
{{< alternativa >}} Uma estrutura que armazena apenas um único valor. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que armazena múltiplos valores do mesmo tipo em uma única variável. {{< /alternativa >}}
{{< alternativa >}} Uma estrutura que executa repetições automaticamente. {{< /alternativa >}}
{{< alternativa >}} Uma classe que substitui todos os tipos primitivos. {{< /alternativa >}}
{{< solucao letra="B" >}}
Um array em Java é uma estrutura que armazena múltiplos valores do mesmo tipo em uma única variável, acessados por índice.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Como os elementos de um array são acessados em Java?
{{< alternativa >}} Pelo nome da variável e tipo do dado. {{< /alternativa >}}
{{< alternativa >}} Pelo índice, começando em 1. {{< /alternativa >}}
{{< alternativa >}} Pelo índice, começando em 0. {{< /alternativa >}}
{{< alternativa >}} Pelo valor armazenado no array. {{< /alternativa >}}
{{< solucao letra="C" >}}
Em Java, os arrays são indexados a partir de 0, ou seja, o primeiro elemento está na posição 0.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Qual é a forma correta de declarar um array de inteiros em Java?
{{< alternativa >}} int array = new int[5]; {{< /alternativa >}}
{{< alternativa >}} int[] array = new int[5]; {{< /alternativa >}}
{{< alternativa >}} array int[] = new int(5); {{< /alternativa >}}
{{< alternativa >}} int array[5] = new int[]; {{< /alternativa >}}
{{< solucao letra="B" >}}
A forma correta em Java é usar colchetes após o tipo: int[] array = new int[5];
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que será exibido no console ao executar o código abaixo?

{{< code >}}
int[] numeros = {10, 20, 30};
System.out.println(numeros[1]);
{{< /code >}}

{{< alternativa >}} 10 {{< /alternativa >}}
{{< alternativa >}} 20 {{< /alternativa >}}
{{< alternativa >}} 30 {{< /alternativa >}}
{{< alternativa >}} Erro de compilação {{< /alternativa >}}
{{< solucao letra="B" >}}
O índice 1 acessa o segundo elemento do array, que é 20.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Qual estrutura é mais adequada para percorrer todos os elementos de um array em Java?
{{< alternativa >}} if-else {{< /alternativa >}}
{{< alternativa >}} switch {{< /alternativa >}}
{{< alternativa >}} for ou for-each {{< /alternativa >}}
{{< alternativa >}} try-catch {{< /alternativa >}}
{{< solucao letra="C" >}}
As estruturas for tradicional ou for-each são as mais usadas para percorrer arrays em Java.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Em Java, o tamanho de um array é:
{{< alternativa >}} Dinâmico e pode ser alterado a qualquer momento {{< /alternativa >}}
{{< alternativa >}} Fixo após a criação do array {{< /alternativa >}}
{{< alternativa >}} Sempre infinito {{< /alternativa >}}
{{< alternativa >}} Definido automaticamente pelo compilador em tempo de execução {{< /alternativa >}}
{{< solucao letra="B" >}}
Em Java, o tamanho de um array é fixo após sua criação e não pode ser alterado posteriormente.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
É possível aumentar ou diminuir o tamanho de um array em Java após sua criação?
{{< alternativa >}} Sim, usando o operador new {{< /alternativa >}}
{{< alternativa >}} Sim, com qualquer estrutura de repetição {{< /alternativa >}}
{{< alternativa >}} Não, arrays possuem tamanho fixo {{< /alternativa >}}
{{< alternativa >}} Sim, automaticamente quando necessário {{< /alternativa >}}
{{< solucao letra="C" >}}
Não é possível alterar o tamanho de um array em Java após sua criação, pois ele possui tamanho fixo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Um array em Java pode armazenar diferentes tipos de dados ao mesmo tempo?
{{< alternativa >}} Sim, qualquer tipo pode ser armazenado livremente {{< /alternativa >}}
{{< alternativa >}} Sim, desde que use Object {{< /alternativa >}}
{{< alternativa >}} Não, ele armazena apenas elementos do mesmo tipo {{< /alternativa >}}
{{< alternativa >}} Sim, mas apenas tipos primitivos {{< /alternativa >}}
{{< solucao letra="C" >}}
Arrays em Java são homogêneos, ou seja, armazenam apenas elementos do mesmo tipo definido na sua declaração.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Como podemos obter o tamanho de um array em Java?
{{< alternativa >}} Usando o método size() {{< /alternativa >}}
{{< alternativa >}} Usando a propriedade length {{< /alternativa >}}
{{< alternativa >}} Usando o método length() {{< /alternativa >}}
{{< alternativa >}} Usando o método getSize() {{< /alternativa >}}
{{< solucao letra="B" >}}
O tamanho de um array em Java é obtido pela propriedade length, por exemplo: array.length.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece se tentarmos acessar um índice fora do tamanho do array?
{{< alternativa >}} O programa ignora o erro {{< /alternativa >}}
{{< alternativa >}} O valor null é retornado {{< /alternativa >}}
{{< alternativa >}} O array é automaticamente expandido {{< /alternativa >}}
{{< alternativa >}} Ocorre uma exceção em tempo de execução {{< /alternativa >}}
{{< solucao letra="D" >}}
Acesso a índices inválidos em um array gera a exceção ArrayIndexOutOfBoundsException em tempo de execução.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
O que acontece ao tentar acessar um índice negativo em um array em Java?
{{< alternativa >}} O programa retorna null {{< /alternativa >}}
{{< alternativa >}} O índice é automaticamente convertido para positivo {{< /alternativa >}}
{{< alternativa >}} Ocorre uma exceção em tempo de execução {{< /alternativa >}}
{{< alternativa >}} O array é redimensionado automaticamente {{< /alternativa >}}
{{< solucao letra="C" >}}
Em Java, não existem índices negativos em arrays. Ao tentar acessar um índice negativo, ocorre a exceção ArrayIndexOutOfBoundsException.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que será exibido ao executar o código abaixo?

{{< code >}}
int[] numeros = {5, 10, 15};
System.out.println(numeros[-1]);
{{< /code >}}

{{< alternativa >}} 5 {{< /alternativa >}}
{{< alternativa >}} 15 {{< /alternativa >}}
{{< alternativa >}} null {{< /alternativa >}}
{{< alternativa >}} Erro em tempo de execução {{< /alternativa >}}
{{< solucao letra="D" >}}
Acesso a índice negativo não é permitido em Java e gera ArrayIndexOutOfBoundsException em tempo de execução.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece ao acessar um índice maior ou igual ao tamanho do array?
{{< alternativa >}} O valor 0 é retornado {{< /alternativa >}}
{{< alternativa >}} O último elemento é retornado {{< /alternativa >}}
{{< alternativa >}} O array cresce automaticamente {{< /alternativa >}}
{{< alternativa >}} Ocorre uma exceção em tempo de execução {{< /alternativa >}}
{{< solucao letra="D" >}}
Em Java, acessar um índice maior ou igual ao tamanho do array causa ArrayIndexOutOfBoundsException.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que será impresso no console ao executar o código abaixo?

{{< code >}}
int[] valores = {2, 4, 6};
valores[1] = 99;
System.out.println(valores[1]);
{{< /code >}}

{{< alternativa >}} 4 {{< /alternativa >}}
{{< alternativa >}} 99 {{< /alternativa >}}
{{< alternativa >}} 2 {{< /alternativa >}}
{{< alternativa >}} Erro de compilação {{< /alternativa >}}
{{< solucao letra="B" >}}
O índice 1 é atualizado com o valor 99, então esse será o valor impresso.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual operação está sendo realizada no código abaixo?

{{< code >}}
int[] notas = {7, 8, 9};
notas[2] = 10;
{{< /code >}}

{{< alternativa >}} Criação de um novo array {{< /alternativa >}}
{{< alternativa >}} Leitura de um elemento do array {{< /alternativa >}}
{{< alternativa >}} Atualização de um elemento do array {{< /alternativa >}}
{{< alternativa >}} Exclusão de um elemento do array {{< /alternativa >}}
{{< solucao letra="C" >}}
O código altera o valor da posição 2 do array, ou seja, atualiza um elemento existente.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Em Java, como os elementos de um array são armazenados na memória?
{{< alternativa >}} Em posições aleatórias e independentes da memória {{< /alternativa >}}
{{< alternativa >}} Em um bloco contínuo de memória {{< /alternativa >}}
{{< alternativa >}} Em diferentes partes da memória, sem padrão definido {{< /alternativa >}}
{{< alternativa >}} Em memória secundária (HD) diretamente {{< /alternativa >}}
{{< solucao letra="B" >}}
Em Java, os elementos de um array são armazenados em um bloco contínuo de memória, permitindo acesso direto por índice.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é uma consequência do fato de um array ser armazenado em um bloco contínuo de memória?
{{< alternativa >}} Não é possível acessar elementos por índice {{< /alternativa >}}
{{< alternativa >}} O acesso aos elementos é mais rápido e direto {{< /alternativa >}}
{{< alternativa >}} O array pode ter tamanhos diferentes em cada posição {{< /alternativa >}}
{{< alternativa >}} Os dados são sempre armazenados no disco {{< /alternativa >}}
{{< solucao letra="B" >}}
Como o array ocupa um bloco contínuo de memória, o acesso por índice é direto e mais eficiente.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Um array em Java pode ser considerado como:
{{< alternativa >}} Uma estrutura espalhada pela memória sem organização {{< /alternativa >}}
{{< alternativa >}} Uma lista encadeada de elementos {{< /alternativa >}}
{{< alternativa >}} Um bloco contínuo de memória com elementos do mesmo tipo {{< /alternativa >}}
{{< alternativa >}} Um conjunto de variáveis independentes sem relação entre si {{< /alternativa >}}
{{< solucao letra="C" >}}
Um array é um bloco contínuo de memória que armazena elementos do mesmo tipo, permitindo acesso indexado.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Por que o array em Java não é considerado uma estrutura “espalhada” na memória?
{{< alternativa >}} Porque ele usa ponteiros para diferentes locais da memória {{< /alternativa >}}
{{< alternativa >}} Porque seus elementos são armazenados de forma sequencial na memória {{< /alternativa >}}
{{< alternativa >}} Porque cada elemento é um objeto independente {{< /alternativa >}}
{{< alternativa >}} Porque ele só existe na memória cache do processador {{< /alternativa >}}
{{< solucao letra="B" >}}
Arrays em Java armazenam seus elementos de forma sequencial (contígua) na memória, não espalhada.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que melhor descreve a estrutura de memória de um array em Java?
{{< alternativa >}} Elementos armazenados em locais aleatórios da memória {{< /alternativa >}}
{{< alternativa >}} Elementos armazenados em estrutura hierárquica {{< /alternativa >}}
{{< alternativa >}} Elementos armazenados em bloco contínuo e sequencial {{< /alternativa >}}
{{< alternativa >}} Elementos armazenados apenas no heap de forma fragmentada {{< /alternativa >}}
{{< solucao letra="C" >}}
A estrutura de um array em Java é um bloco contínuo e sequencial de memória.
{{< /solucao >}}
{{< /questao >}}

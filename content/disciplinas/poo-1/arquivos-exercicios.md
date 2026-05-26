---
title: "Exercícios sobre manipulação de arquivos"
slug: "arquivos-exercicios"
description: "Exercícios sobre manipulação de arquivos"
tags:
- exercicios
- arquivos
- json
- serializacao
---


{{< lista-questoes >}}


{{< questao >}}
<p>
Desenvolva um programa para realizar o cadastro de clientes em um arquivo no formato CSV
(<em>Comma-Separated Values</em>). Cada cliente deve ser armazenado em uma única linha
do arquivo, e os campos devem ser separados pelo caractere <code>;</code>.
</p>

<p>
Para cada cliente, devem ser registradas as seguintes informações:
</p>

<ul>
    <li>Identificador único;</li>
    <li>Nome completo;</li>
    <li>E-mail;</li>
    <li>Telefone.</li>
</ul>

<p>
Ao final da execução, o programa deve gerar um arquivo contendo todos os clientes
cadastrados no seguinte formato:
</p>

<pre>
1;João da Silva;joao@email.com;(47) 99999-1111
2;Maria Souza;maria@email.com;(47) 99999-2222
3;Pedro Santos;pedro@email.com;(47) 99999-3333
</pre>

<p>
Utilize a API NIO do Java para realizar a escrita do arquivo.
</p>
{{< /questao >}}

{{< questao >}}
<p>
Desenvolva um programa capaz de realizar a leitura de um arquivo no formato CSV
contendo informações de clientes. Cada linha do arquivo representa um cliente e
os campos são separados pelo caractere <code>;</code>.
</p>

<p>
Cada registro do arquivo possui as seguintes informações:
</p>

<ul>
    <li>Identificador único;</li>
    <li>Nome completo;</li>
    <li>E-mail;</li>
    <li>Telefone.</li>
</ul>

<p>
O programa deve ler todas as linhas do arquivo, converter os dados para objetos
da classe <code>Client</code> e armazená-los em uma coleção.
</p>

<p>
Considere que o arquivo possui o seguinte formato:
</p>

<pre>
1;João da Silva;joao@email.com;(47) 99999-1111
2;Maria Souza;maria@email.com;(47) 99999-2222
3;Pedro Santos;pedro@email.com;(47) 99999-3333
</pre>

<p>
Ao final da leitura, o programa deve exibir as informações dos clientes no console
ou disponibilizá-las para processamento posterior pela aplicação.
</p>

<p>
Utilize a API NIO do Java para realizar a leitura do arquivo e a API de Streams
para converter cada linha em um objeto <code>Client</code>.
</p>
{{< /questao >}}

{{< questao >}}
<p>
Desenvolva um programa capaz de gerenciar as informações de clientes armazenadas
em um arquivo CSV. O programa deve realizar a leitura dos dados do arquivo,
permitir a atualização das informações de um cliente e persistir as alterações
novamente no arquivo.
</p>

<p>
Cada linha do arquivo representa um cliente e os campos são separados pelo
caractere <code>;</code>.
</p>

<p>
As informações armazenadas para cada cliente são:
</p>

<ul>
    <li>Identificador único;</li>
    <li>Nome completo;</li>
    <li>E-mail;</li>
    <li>Telefone.</li>
</ul>

<p>
O programa deve localizar um cliente a partir de seu identificador único,
atualizar uma ou mais informações e, em seguida, sobrescrever o arquivo com
os dados atualizados.
</p>

<p>
Considere o seguinte conteúdo inicial para o arquivo:
</p>

<pre>
1;João da Silva;joao@email.com;(47) 99999-1111
2;Maria Souza;maria@email.com;(47) 99999-2222
3;Pedro Santos;pedro@email.com;(47) 99999-3333
</pre>

<p>
Após atualizar o e-mail e o telefone da cliente de identificador <code>2</code>,
o arquivo deverá conter:
</p>

<pre>
1;João da Silva;joao@email.com;(47) 99999-1111
2;Maria Souza;maria.souza@email.com;(47) 98888-2222
3;Pedro Santos;pedro@email.com;(47) 99999-3333
</pre>

<p>
Utilize a API NIO do Java para realizar a leitura e a escrita do arquivo.
Após modificar os dados em memória, o programa deve regravar todo o conteúdo
do arquivo com as informações atualizadas.
</p>
{{< /questao >}}

{{< questao >}}

<p>
Desenvolva um programa capaz de verificar se uma determinada palavra pertence ao
vocabulário da língua portuguesa. Para isso, utilize uma lista de palavras
armazenada em um arquivo texto, contendo uma palavra por linha.
</p>

<p>
O programa deve solicitar ao usuário uma palavra e informar se ela foi encontrada
ou não no dicionário.
</p>

<p>
A busca não deve diferenciar letras maiúsculas e minúsculas. Por exemplo,
as palavras <code>Casa</code>, <code>CASA</code> e <code>casa</code> devem ser
consideradas equivalentes.
</p>

<p>
Exemplos:
</p>

<pre>
Digite uma palavra: computador
Palavra encontrada no dicionário.
</pre>

<pre>
Digite uma palavra: xablauzito
Palavra não encontrada no dicionário.
</pre>

<p>
Utilize como base os arquivos disponibilizados pelo Instituto de Matemática e
Estatística da USP, que contêm listas de palavras do português brasileiro.
A versão recomendada para este exercício é o arquivo em UTF-8:
</p>

<p>
<a href="https://www.ime.usp.br/~pf/dicios/br-utf8.txt">
https://www.ime.usp.br/~pf/dicios/br-utf8.txt
</a>
</p>

<p>
O conjunto de arquivos disponibilizado pela USP contém centenas de milhares de
palavras do português brasileiro e pode ser utilizado para validar a existência
de palavras em aplicações de processamento de texto. O arquivo
<code>br-utf8.txt</code> possui uma palavra por linha e utiliza codificação UTF-8.
</p>

{{< /questao >}}

{{< questao >}}

<p>
Desenvolva um jogo de adivinhação no qual o jogador deve descobrir o nome de um
país sorteado aleatoriamente pelo programa.
</p>

<p>
A lista de países deve ser armazenada em um arquivo no formato JSON. Durante a
execução, o programa deve carregar os dados do arquivo, selecionar um país de
forma aleatória e solicitar que o usuário tente adivinhar seu nome.
</p>

<p>
O jogador terá no máximo <strong>3 tentativas</strong> para acertar o país
sorteado.
</p>

<p>
Após cada tentativa incorreta, o programa deve informar que a resposta está
errada e exibir a quantidade de tentativas restantes.
</p>

<p>
Se o jogador acertar o nome do país dentro do limite de tentativas, uma mensagem
de parabéns deve ser exibida. Caso contrário, o programa deve informar que o
jogador perdeu e revelar o país sorteado.
</p>

<p>
Exemplo de arquivo JSON:
</p>

<pre>
[
  "Brasil",
  "Argentina",
  "Chile",
  "Canadá",
  "Japão",
  "Portugal",
  "Austrália"
]
</pre>

<p>
Exemplo de execução com vitória:
</p>

<pre>
Tentativa 1 de 3
Digite o nome do país: Brasil
Resposta incorreta.

Tentativa 2 de 3
Digite o nome do país: Japão

Parabéns! Você acertou o país sorteado.
</pre>

<p>
Exemplo de execução com derrota:
</p>

<pre>
Tentativa 1 de 3
Digite o nome do país: Brasil
Resposta incorreta.

Tentativa 2 de 3
Digite o nome do país: Argentina
Resposta incorreta.

Tentativa 3 de 3
Digite o nome do país: Chile
Resposta incorreta.

Você perdeu!
O país sorteado era: Canadá
</pre>

<p>
Utilize a biblioteca Jackson para realizar a leitura do arquivo JSON e a classe
<code>Random</code> para selecionar o país sorteado.
</p>

{{< /questao >}}


{{< /lista-questoes >}}

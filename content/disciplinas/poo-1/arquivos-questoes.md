---
title: "Questões sobre manipulação de arquivos"
slug: "arquivos-questoes"
description: "Questões sobre manipulação de arquivos"
tags:
- questoes
- arquivos
---


{{< lista-questoes >}}

{{< questao >}}
O que é um arquivo?

{{< alternativa >}} Uma estrutura utilizada apenas para armazenar objetos Java. {{< /alternativa >}}
{{< alternativa >}} Uma unidade de armazenamento permanente de dados. {{< /alternativa >}}
{{< alternativa >}} Um diretório que contém outros diretórios. {{< /alternativa >}}
{{< alternativa >}} Uma variável armazenada na memória RAM. {{< /alternativa >}}

{{< solucao letra="B" >}}
Um arquivo é uma unidade de armazenamento utilizada para guardar dados de forma permanente.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual classe representa um caminho para um arquivo na API NIO?

{{< alternativa >}} FileReader {{< /alternativa >}}
{{< alternativa >}} Files {{< /alternativa >}}
{{< alternativa >}} Path {{< /alternativa >}}
{{< alternativa >}} Stream {{< /alternativa >}}

{{< solucao letra="C" >}}
A interface <code>Path</code> representa um caminho dentro do sistema de arquivos.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método cria um objeto Path a partir de uma String?

{{< alternativa >}} Files.path() {{< /alternativa >}}
{{< alternativa >}} Path.create() {{< /alternativa >}}
{{< alternativa >}} Paths.get() {{< /alternativa >}}
{{< alternativa >}} Files.getPath() {{< /alternativa >}}

{{< solucao letra="C" >}}
O método <code>Paths.get()</code> cria um objeto do tipo <code>Path</code>.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que o método <code>Files.readAllLines()</code> retorna?

{{< alternativa >}} Uma String contendo todo o arquivo. {{< /alternativa >}}
{{< alternativa >}} Um List&lt;String&gt; contendo as linhas do arquivo. {{< /alternativa >}}
{{< alternativa >}} Um Stream&lt;String&gt;. {{< /alternativa >}}
{{< alternativa >}} Um array de bytes. {{< /alternativa >}}

{{< solucao letra="B" >}}
Cada elemento da lista corresponde a uma linha do arquivo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual é a principal desvantagem de utilizar <code>Files.readAllLines()</code> em arquivos muito grandes?

{{< alternativa >}} O método não suporta arquivos de texto. {{< /alternativa >}}
{{< alternativa >}} O método carrega todo o conteúdo na memória. {{< /alternativa >}}
{{< alternativa >}} O método só funciona em sistemas Linux. {{< /alternativa >}}
{{< alternativa >}} O método retorna bytes em vez de texto. {{< /alternativa >}}

{{< solucao letra="B" >}}
Todo o conteúdo é carregado na memória antes do processamento.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método é mais adequado para processar arquivos grandes?

{{< alternativa >}} Files.readAllLines() {{< /alternativa >}}
{{< alternativa >}} Files.readString() {{< /alternativa >}}
{{< alternativa >}} Files.lines() {{< /alternativa >}}
{{< alternativa >}} Files.readAllBytes() {{< /alternativa >}}

{{< solucao letra="C" >}}
O método <code>Files.lines()</code> retorna um Stream e processa os dados sob demanda.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual opção permite adicionar conteúdo ao final de um arquivo existente?

{{< alternativa >}} StandardOpenOption.REPLACE {{< /alternativa >}}
{{< alternativa >}} StandardOpenOption.APPEND {{< /alternativa >}}
{{< alternativa >}} StandardOpenOption.OVERWRITE {{< /alternativa >}}
{{< alternativa >}} StandardOpenOption.UPDATE {{< /alternativa >}}

{{< solucao letra="B" >}}
A opção <code>APPEND</code> adiciona dados ao final do arquivo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que acontece quando <code>Files.write(path, linhas)</code> é chamado e o arquivo já existe?

{{< alternativa >}} O conteúdo é acrescentado ao final. {{< /alternativa >}}
{{< alternativa >}} O conteúdo é substituído. {{< /alternativa >}}
{{< alternativa >}} Uma exceção é lançada obrigatoriamente. {{< /alternativa >}}
{{< alternativa >}} Nada acontece. {{< /alternativa >}}

{{< solucao letra="B" >}}
O conteúdo anterior é substituído pelo novo conteúdo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual método permite escrever diretamente uma String em um arquivo?

{{< alternativa >}} Files.writeText() {{< /alternativa >}}
{{< alternativa >}} Files.writeString() {{< /alternativa >}}
{{< alternativa >}} Files.saveString() {{< /alternativa >}}
{{< alternativa >}} Files.appendString() {{< /alternativa >}}

{{< solucao letra="B" >}}
O método <code>Files.writeString()</code> grava uma String em um arquivo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual combinação de opções cria o arquivo caso ele não exista e adiciona conteúdo caso exista?

{{< alternativa >}} CREATE e APPEND {{< /alternativa >}}
{{< alternativa >}} CREATE e DELETE {{< /alternativa >}}
{{< alternativa >}} WRITE e DELETE {{< /alternativa >}}
{{< alternativa >}} APPEND e REMOVE {{< /alternativa >}}

{{< solucao letra="A" >}}
A combinação CREATE + APPEND é muito utilizada para logs.
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

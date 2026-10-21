---
title: "Questões ENADE Sistemas de Informação sobre POO"
description: "Questões do enade sobre"
slug: enade-questoes
tags:
- enade
- orientacao-objetos
- questões
---

{{< lista-questoes >}}


{{< questao >}}

Uma fundação municipal de arte e cultura oferece cursos para crianças e adolescentes de até 16 anos.
Os registros de matrículas são realizados em uma planilha eletrônica ilustrada a seguir, o que dificulta bastante
o controle dos dados frente ao número expressivo de estudantes, muitos dos quais solicitam matrícula em mais
de um curso. A administração da fundação, então, solicitou o desenvolvimento de um programa para facilitar
o registro e a consulta desses dados, incluindo-se a data de efetivação de cada matrícula, para fins de controles
específicos da secretaria.
<br>
<table border="1" cellpadding="8" cellspacing="0" style="border-collapse: collapse; width: 100%; font-family: Arial, sans-serif;">
    <thead>
        <tr style="background-color: #f2f2f2; text-align: center;">
            <th>NÚMERO</th>
            <th>NOME ESTUDANTE</th>
            <th>DATA NASC.</th>
            <th>NOME RESPONSÁVEL</th>
            <th>CONTATOS</th>
            <th>CURSO</th>
            <th>HORÁRIO</th>
            <th>PROFESSOR(A)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td style="text-align: center;">10</td>
            <td>Ada Lovelace</td>
            <td style="text-align: center;">10/12/2009</td>
            <td>Charles Babbage</td>
            <td>(99)99999-0101<br>charles@babbage.com</td>
            <td>Violão Básico<br>Desenho</td>
            <td>9h - 10h (ter - qui)<br>10h - 11h (seg - qua)</td>
            <td>Dennis Ritchie<br>John Backus</td>
        </tr>
        <tr>
            <td style="text-align: center;">11</td>
            <td>Ole-Johan Dahl</td>
            <td style="text-align: center;">12/10/2008</td>
            <td>Kristen Nygaard</td>
            <td style="text-align: center;">-</td>
            <td>Desenho</td>
            <td>9h - 10h (seg - qua)</td>
            <td>Mary Keller</td>
        </tr>
        <tr>
            <td style="text-align: center;">12</td>
            <td>Grace Hopper</td>
            <td style="text-align: center;">09/12/2010</td>
            <td>Howard Aiken</td>
            <td>(99)99999-0091<br>(99)99999-0095</td>
            <td>Balé</td>
            <td>8h - 10h (sex)</td>
            <td>Hedy Lamarr</td>
        </tr>
        <tr>
            <td style="text-align: center;">13</td>
            <td>Alan Turing</td>
            <td style="text-align: center;">23/06/2009</td>
            <td>Joan Clarke</td>
            <td>(99)99999-0231</td>
            <td>Desenho<br>Violão Básico</td>
            <td>9h - 10h (seg - qua)<br>9h - 10h (ter - qui)</td>
            <td>Mary Keller<br>Dennis Ritchie</td>
        </tr>
        <tr>
            <td style="text-align: center;">14</td>
            <td>Dorothy Vaughan</td>
            <td style="text-align: center;">20/09/2009</td>
            <td>Katherine Johnson</td>
            <td>(99)99999-0201</td>
            <td>Balé</td>
            <td>8h - 10h (sex)</td>
            <td>Hedy Lamarr</td>
        </tr>
        <tr>
            <td style="text-align: center;">...</td>
            <td style="text-align: center;">...</td>
            <td style="text-align: center;">...</td>
            <td style="text-align: center;">...</td>
            <td style="text-align: center;">...</td>
            <td style="text-align: center;">...</td>
            <td style="text-align: center;">...</td>
            <td style="text-align: center;">...</td>
        </tr>
    </tbody>
</table>
A equipe de desenvolvimento de softwares da prefeitura, após uma breve entrevista com a administração
da fundação e de posse da planilha eletrônica, modelou um Diagrama de Classes como parte da
especificação dos requisitos do sistema. Considerando o cenário descrito, assinale a opção a seguir que exibe o Diagrama de Classes modelado
corretamente pela equipe de desenvolvimento.

<img src="/images/a.png">
<img src="/images/b.png">
<img src="/images/c.png">

{{< solucao letra="B" >}}
Fonte: ENADE 2021, Tecnologia em Análise e Desenvolvimento de Sistemas, Questão 15.


{{< /solucao >}}

{{< /questao >}}

{{< questao >}}
Um analista de requisitos identificou as seguintes histórias de usuários para um sistema web de reserva
de passagens de uma empresa aérea:
<br><br>
HST 01: COMO cliente, GOSTARIA de me cadastrar no site da empresa informando meu e-mail, nome, CPF,
telefone e endereço PARA poder usar os serviços web da empresa.
<br><br>
HST 02: COMO cliente, GOSTARIA de pesquisar por preços das passagens aéreas informando data, hora,
cidade e aeroporto de ida e de volta PARA poder escolher uma opção de reserva que me interessa.
<br><br>
HST 03: COMO cliente, GOSTARIA de confirmar uma reserva de passagem aérea selecionada, escolhendo
uma das formas de pagamento disponibilizada pela empresa PARA poder viajar para o local escolhido
na reserva.
<br><br>
HST 04: COMO cliente, GOSTARIA de fazer o check-in online da reserva PARA poder realizar meu embarque.
<br><br>
Tendo por base essas histórias de usuários, elabore um diagrama de classes da UML (Unified Modeling
Language) para o sistema, identificando as classes (máximo seis), atributos e associações entre as classes
com as respectivas multiplicidades. Deverão ser representadas as reservas de ida e de volta como classes
de uma associação do tipo generalização (herança) e também ser identificados pelo menos três métodos
para a classe Reserva. Para as demais classes não é necessário identificar os métodos. Também não há
necessidade de identificar a multiplicidade dos atributos nas classes. (valor: 10,0 pontos).

{{< solucao letra="E" >}}
Fonte: ENADE 2021, Tecnologia em Análise e Desenvolvimento de Sistemas, Questão Discursiva 04.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
A orientação a objetos é uma forma abstrata de pensar um problema utilizando-se conceitos do mundo real e não, apenas, conceitos computacionais. Nessa perspectiva, a adoção do paradigma orientado a objetos implica necessariamente que

{{< alternativa >}} os usuários utilizem as aplicações de forma mais simples. {{< /alternativa >}}
{{< alternativa >}} os sistemas sejam encapsulados por outros sistemas. {{< /alternativa >}}
{{< alternativa >}} os programadores de aplicações sejam mais especializados. {{< /alternativa >}}
{{< alternativa >}} os objetos sejam implementados de maneira eficiente e simples. {{< /alternativa >}}
{{< alternativa >}} a computação seja acionada por troca de mensagens entre objetos. {{< /alternativa >}}
{{< solucao letra="E" >}}
Fonte: ENADE 2005, Bacharel em Sistema de Informação, Questão 20.


<ul>
  <li><strong>A. Falsa.</strong> A orientação a objetos não implica necessariamente que os usuários utilizem as aplicações de forma mais simples.</li>
  <li><strong>B. Falsa.</strong> O encapsulamento consiste em agrupar dados e comportamentos em uma unidade, ocultando detalhes internos de implementação, e não em encapsular sistemas por outros sistemas.</li>
  <li><strong>C. Falsa.</strong> A adoção da orientação a objetos não exige necessariamente que os programadores sejam mais especializados.</li>
  <li><strong>D. Falsa.</strong> A orientação a objetos não garante que os objetos sejam implementados de maneira eficiente e simples.</li>
  <li><strong>E. Verdadeira.</strong> A troca de mensagens entre objetos é um dos princípios fundamentais da orientação a objetos, permitindo a comunicação e a colaboração entre eles.</li>
</ul>

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Um Padrão de Projeto nomeia, abstrai e identifica os aspectos-chave de uma estrutura de projeto comum para torná-la útil para a criação de um projeto orientado a objetos reutilizáveis.
<br>
GAMMA, E.; HELM, R.; JOHNSON, R.; VLISSIDES, J. <b>Padrões de Projeto: Soluções Reutilizáveis de Software Orientado a Objetos.</b> Porto Alegre: Bookman, 2000.
<br><br>
Em relação a Padrões de Projeto, analise as afirmações a seguir.
<br><br>
I. Prototype é um tipo de padrão estrutural.
<br>
II. Singleton tem por objetivos garantir que uma classe tenha ao menos uma instância e fornecer um ponto global de acesso para ela.
<br>
III. Template Method tem por objetivo definir o esqueleto de um algoritmo em uma operação, postergando a definição de alguns passos para subclasses.
<br>
IV. Iterator fornece uma maneira de acessar sequencialmente os elementos de um objeto agregado sem expor sua representação subjacente.
<br><br>
É correto apenas o que se afirma em
<br><br>
{{< alternativa >}} I. {{< /alternativa >}}
{{< alternativa >}} II. {{< /alternativa >}}
{{< alternativa >}} I e IV. {{< /alternativa >}}
{{< alternativa >}} II e III. {{< /alternativa >}}
{{< alternativa >}} III e IV. {{< /alternativa >}}
{{< solucao letra="E" >}}
Fonte: ENADE 2011, Bacharel em Sistema de Informação, Questão 25.


<ul>
  <li><strong>I. Falsa.</strong> <code>Prototype</code> é um padrão criacional, pois permite criar objetos por meio da clonagem de instâncias existentes.</li>
  <li><strong>II. Falsa.</strong> O <code>Singleton</code> garante que uma classe tenha uma única instância, e não “ao menos uma instância”, além de fornecer um ponto global de acesso a ela. A redação da afirmação não corresponde à definição clássica do padrão.</li>
  <li><strong>III. Verdadeira.</strong> <code>Template Method</code> define o esqueleto de um algoritmo e deixa alguns passos para serem implementados pelas subclasses.</li>
  <li><strong>IV. Verdadeira.</strong> <code>Iterator</code> permite percorrer sequencialmente os elementos de um objeto agregado sem expor sua representação interna.</li>
</ul>

{{< /solucao >}}
{{< /questao >}}


{{< questao >}}

Uma empresa deseja lançar um sistema de comércio eletrónico para vender os seus produtos. Essa empresa vende produtos de diversas categorias, como roupas, perfumes e eletrónicos, e aceita diversas formas de pagamento, como cartão de crédito e boleto bancário. No sistema de vendas implementado, cada produto deve ser cadastrado com a sua descrição, preço de venda, quantidade em stock e respetiva categoria. Cada cliente que deseja realizar compras tem de se cadastrar no sistema indicando o seu nome, endereço e <i>e-mail</i>. Se o cliente for corporativo, deve cadastrar o seu CNPJ e, se for individual, o seu CPF. O cliente cadastrado pode realizar um pedido de compra dos produtos em stock na quantidade que desejar. O cliente escolhe uma forma de pagamento disponível e recebe, por <i>e-mail</i>, o número do pedido e informações do <i>status</i> do pedido. Após a confirmação do pagamento, a loja realiza a entrega dos itens solicitados no endereço do cliente e envia, por <i>e-mail</i>, a nota fiscal eletrónica. Tendo em vista que os preços dos produtos podem ser atualizados a qualquer momento, o sistema tem de ser capaz de reemitir uma nota fiscal de um pedido de compra de qualquer produto e respetivo preço na data da compra realizada pelo cliente.
<br><br>
Considerando esse cenário, proponha um Diagrama de Classes, segundo a UML (<i>Unified Modeling Language</i>), indicando o nome de cada classe, respetivos atributos e relacionamentos entre as classes com as respetivas cardinalidades. Na sua proposta, identifique, pelo menos, um relacionamento de generalização e um relacionamento de composição, não sendo necessário indicar as operações de cada classe. (valor: 10,0 pontos)
{{< solucao letra=" " >}}

Fonte: ENADE 2014, Bacharel em Sistema de Informação, Questão Discursiva 5.
{{< /solucao >}}
{{< /questao >}}




{{< questao >}}

Durante as Olimpíadas de 2016, foram disputadas nove competições masculinas e seis competições femininas de tiro desportivo. Para os Jogos Olímpicos de 2020, propõe-se o desenvolvimento de um sistema de agendamento de competições de tiro desportivo, com base nas competições realizadas nos últimos jogos.
<br><br>
No tiro desportivo, cada competição é composta por eventos, que podem ser a fase classificatória, a fase final ou a cerimónia de entrega de medalhas. Para cada evento, é preciso saber a data de realização, o horário de início, o horário estimado de término e o local, que pode ser uma das diversas salas de tiro ou o campo de tiro externo, destinado às competições de fossa olímpica e <i>skeet</i>. As competições diferenciam em função de três características:

<ul>
    <li> o equipamento utilizado, que pode ser pistola, carabina ou espingarda;</li>
    <li> o tipo de alvo e a distância, que pode ser um alvo fixo em distâncias de 10 m, 25 m ou 50 m ou pratos lançados que devem ser atingidos no ar;</li>
    <li> a posição do atirador ao disparar, que pode ser deitado, ajoelhado ou em pé.</li>
</ul>

As competições de tiro desportivo realizadas nos últimos Jogos Olímpicos de 2016 estão apresentadas no quadro a seguir.

<table>
  <thead>
    <tr>
      <th>Competições masculinas</th>
      <th>Competições femininas</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Pistola de ar 10 m</td>
      <td>Pistola de ar 10 m</td>
    </tr>
    <tr>
      <td>Carabina de ar 10 m</td>
      <td>Carabina de ar 10 m</td>
    </tr>
    <tr>
      <td>Pistola rápida 25 m</td>
      <td>Pistola 25 m</td>
    </tr>
    <tr>
      <td>Pistola 50 m</td>
      <td>Carabina três posições 50 m</td>
    </tr>
    <tr>
      <td>Carabina deitado 50 m</td>
      <td>Skeet</td>
    </tr>
    <tr>
      <td>Carabina três posições 50 m</td>
      <td>Fossa olímpica</td>
    </tr>
    <tr>
      <td>Skeet</td>
      <td></td>
    </tr>
    <tr>
      <td>Fossa olímpica</td>
      <td></td>
    </tr>
    <tr>
      <td>Fossa olímpica dupla</td>
      <td></td>
    </tr>
  </tbody>
</table>


As competições dessa modalidade contam com atletas de diversos países, sendo que cada atleta pode participar de uma ou mais competições, desde que esteja devidamente classificado. Para cada atleta, é preciso registrar o nome, o país e o comité olímpico nacional que representa, além das competições que irá disputar.
<br><br>
Considerando o domínio apresentado no texto, elabore um diagrama de classe da UML para esse sistema, identificando as classes (no máximo seis), os atributos e os relacionamentos. (valor: 10,0 pontos)

{{< solucao letra="E" >}}

Fonte: ENADE 2017, Bacharel em Sistema de Informação, Questão Discursiva 5.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}

Uma loja pretende desenvolver um sistema cujo processo de modelagem utilizará UML (Unified Modeling Language). Essa empresa tem dois tipos de colaboradores, o atendente e o gerente. A principal atividade a ser automatizada pelo sistema é o processamento de vendas, cuja execução é altamente complexa. Dessa forma, a modelagem deve ser realizada de maneira estruturada e organizada, tendo como foco a sua reutilização em diferentes contextos. As vendas são realizadas quase integralmente por atendentes, entretanto, caso haja grande quantidade de clientes, os gerentes também podem processar vendas, por exemplo. O processamento de vendas pode ser realizado considerando duas modalidades de pagamento: a prazo ou à vista, todavia, independentemente da forma de pagamento, há um conjunto comum de ações que sempre são realizadas. As compras a prazo englobam dois modos de pagamento (via cartão de crédito e via boleto) que possuem ações comuns, mas que se diferem nas ações finais. Para algumas formas de processamento de vendas é aplicado um desconto sobre o valor total. O desconto deve ser aplicado sempre que o pagamento for realizado à vista ou quando o pagamento for realizado via boleto com parcelamento em até seis vezes. Entanto, a loja oferece como forma de pagamento boleto com parcelamento em até doze vezes. No processamento de vendas, após a confirmação do pagamento, é necessário emitir a nota fiscal dos produtos. Apenas em circunstâncias em que algum dos produtos vendidos não possa ser retirado na loja, deve ser possível solicitar a entrega pelo sistema.
<br><br>
Considerando a situação apresentada no texto, faça o que se pede nos itens a seguir:
<ol>
    <li>Indique o tipo de relacionamento que, de acordo com a linguagem UML, permite representar o fato de atendentes e gerentes poderem realizar as mesmas atividades.</li>
    
    <li>Elabore um diagrama de caso de uso completo da UML para esse sistema, identificando os atores, os casos de uso e os relacionamentos.</li>
</ol>

{{< solucao letra="E" >}}

Fonte: ENADE 2021, Bacharel em Sistema de Informação, Questão Discursiva 5.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}

O gestor de uma instituição seguradora solicitou ao desenvolvedor de software o projeto de uma solução computacional para a instituição. Após executar a análise de requisitos, esse desenvolvedor esboçou o diagrama UML (<i>Unified Modeling Language</i>), contendo os elementos apresentados na figura a seguir.

{{< plantuml >}}

class Segurado {
}

class Seguro {
}

class Residencial {
}

class Automotivo {
}

class Vida {
}

Segurado "1..1" -- "0..n" Seguro 

Seguro <|-- Residencial
Seguro <|-- Automotivo
Seguro <|-- Vida

{{< /plantuml >}}


<br>
Em relação ao que é proposto no diagrama, avalie as afirmações a seguir:   
<br><br>
I. A classe Seguro é a superclasse de uma hierarquia de herança múltipla.
<br>
II. O mecanismo de ligação entre as classes Segurado e Seguro é a associação.
<br>
III. As subclasses Residencial, Automotivo e Vida devem ser implementadas como classes abstratas.
<br>
IV. É permitido que um Segurado possa adquirir várias apólices de Seguro.
<br><br>

{{< alternativa >}} I e III. {{< /alternativa >}}
{{< alternativa >}} II e III. {{< /alternativa >}}
{{< alternativa >}} II e IV. {{< /alternativa >}}
{{< alternativa >}} I, II e IV. {{< /alternativa >}}
{{< alternativa >}} I, III e IV. {{< /alternativa >}}

{{< solucao letra="C" >}}

Fonte: ENADE 2021, Bacharel em Sistema de Informação, Questão 9.


<ul>
  <li><strong>I. Falsa.</strong> A classe <code>Seguro</code> é a superclasse de uma hierarquia de herança, mas não de herança múltipla, pois cada subclasse apresentada possui apenas uma superclasse direta.</li>
  <li><strong>II. Verdadeira.</strong> O relacionamento entre <code>Segurado</code> e <code>Seguro</code> é uma associação, representada por uma linha contínua no diagrama UML.</li>
  <li><strong>III. Falsa.</strong> O diagrama não indica que as subclasses <code>Residencial</code>, <code>Automotivo</code> e <code>Vida</code> devam ser abstratas. Elas podem ser classes concretas.</li>
  <li><strong>IV. Verdadeira.</strong> A multiplicidade <code>0..n</code> no lado de <code>Seguro</code> indica que um <code>Segurado</code> pode estar associado a nenhum ou a vários seguros.</li>
</ul>
{{< /solucao >}}
{{< /questao >}}



{{< /lista-questoes >}}

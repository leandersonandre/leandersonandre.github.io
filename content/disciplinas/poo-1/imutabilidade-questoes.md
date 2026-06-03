---
title: "Questões sobre Imutabilidade"
slug: "imutabilidade-questoes"
description: "Questões sobre imutabilidade"
tags:
- imutabilidade
- record
- questoes
---

{{< lista-questoes >}}

{{< questao >}}
O que caracteriza um objeto imutável?

{{< alternativa >}} Seus atributos podem ser alterados a qualquer momento. {{< /alternativa >}}
{{< alternativa >}} Seu estado não pode ser alterado após a criação. {{< /alternativa >}}
{{< alternativa >}} Possui obrigatoriamente métodos setters. {{< /alternativa >}}
{{< alternativa >}} Pode ter apenas atributos públicos. {{< /alternativa >}}

{{< solucao letra="B" >}}
Um objeto imutável não permite alterações em seu estado após sua criação.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual palavra reservada do Java é frequentemente utilizada para implementar imutabilidade em atributos?

{{< alternativa >}} static {{< /alternativa >}}
{{< alternativa >}} abstract {{< /alternativa >}}
{{< alternativa >}} final {{< /alternativa >}}
{{< alternativa >}} protected {{< /alternativa >}}

{{< solucao letra="C" >}}
A palavra reservada <code>final</code> impede a reatribuição do atributo após sua inicialização.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual das práticas abaixo é recomendada para criar uma classe imutável?

{{< alternativa >}} Declarar atributos como public. {{< /alternativa >}}
{{< alternativa >}} Fornecer métodos setters para todos os atributos. {{< /alternativa >}}
{{< alternativa >}} Declarar atributos como private e final. {{< /alternativa >}}
{{< alternativa >}} Permitir acesso direto aos atributos. {{< /alternativa >}}

{{< solucao letra="C" >}}
Atributos privados e finais ajudam a impedir modificações externas.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Uma classe possui apenas atributos <code>private final</code>, mas também possui métodos setters. Ela pode ser considerada imutável?

{{< alternativa >}} Sim, porque os atributos são final. {{< /alternativa >}}
{{< alternativa >}} Não, pois métodos setters permitem alterar o estado. {{< /alternativa >}}
{{< alternativa >}} Sim, desde que utilize construtor. {{< /alternativa >}}
{{< alternativa >}} Sim, porque final garante imutabilidade completa. {{< /alternativa >}}

{{< solucao letra="B" >}}
Uma classe imutável não deve fornecer métodos que alterem seus atributos.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo.

{{< code >}}
class Person {
    private final String name;

    public Person(String name) {
        this.name = name;
    }

    public String name() {
        return name;
    }
}
{{< /code >}}

Qual característica torna essa classe imutável?

{{< alternativa >}} O método name() retorna String. {{< /alternativa >}}
{{< alternativa >}} O atributo é final e não existe setter. {{< /alternativa >}}
{{< alternativa >}} O atributo é privado. {{< /alternativa >}}
{{< alternativa >}} O construtor recebe parâmetros. {{< /alternativa >}}

{{< solucao letra="B" >}}
O atributo é final e não há métodos para modificá-lo após a criação do objeto.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Qual afirmação sobre atributos final é correta?

{{< alternativa >}} Impedem qualquer alteração no estado interno dos objetos referenciados. {{< /alternativa >}}
{{< alternativa >}} Impedem a reatribuição da variável após a inicialização. {{< /alternativa >}}
{{< alternativa >}} Tornam automaticamente a classe imutável. {{< /alternativa >}}
{{< alternativa >}} Permitem alterar o valor apenas uma vez por método. {{< /alternativa >}}

{{< solucao letra="B" >}}
O modificador <code>final</code> impede apenas a reatribuição da referência ou valor.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Analise o código abaixo.

{{< code >}}
class Team {
    private final List<String> members = new ArrayList<>();

    public List<String> getMembers() {
        return members;
    }
}
{{< /code >}}

Qual afirmação é correta?

{{< alternativa >}} A lista não pode receber novos elementos. {{< /alternativa >}}
{{< alternativa >}} O atributo members pode apontar para outra lista. {{< /alternativa >}}
{{< alternativa >}} A referência é final, mas os elementos da lista podem ser alterados. {{< /alternativa >}}
{{< alternativa >}} A classe é obrigatoriamente imutável. {{< /alternativa >}}

{{< solucao letra="C" >}}
O atributo não pode referenciar outra lista, mas a lista continua mutável.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Como objetos imutáveis normalmente realizam modificações em seus dados?

{{< alternativa >}} Alterando diretamente os atributos privados. {{< /alternativa >}}
{{< alternativa >}} Utilizando métodos setters. {{< /alternativa >}}
{{< alternativa >}} Criando uma nova instância com os dados modificados. {{< /alternativa >}}
{{< alternativa >}} Tornando os atributos públicos temporariamente. {{< /alternativa >}}

{{< solucao letra="C" >}}
Objetos imutáveis preservam a instância original e criam uma nova versão com os dados alterados.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
O que é um record em Java?

{{< alternativa >}} Um tipo especial para representar objetos de dados imutáveis. {{< /alternativa >}}
{{< alternativa >}} Uma interface para armazenar registros em arquivos. {{< /alternativa >}}
{{< alternativa >}} Um tipo de coleção da API Collections. {{< /alternativa >}}
{{< alternativa >}} Um substituto para classes abstratas. {{< /alternativa >}}

{{< solucao letra="A" >}}
Records foram criados para representar objetos cujo principal objetivo é armazenar dados.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Ao declarar um record, quais elementos são gerados automaticamente pelo compilador?

{{< alternativa >}} Apenas os atributos. {{< /alternativa >}}
{{< alternativa >}} Apenas os getters. {{< /alternativa >}}
{{< alternativa >}} Construtor, métodos de acesso, equals, hashCode e toString. {{< /alternativa >}}
{{< alternativa >}} Apenas equals e hashCode. {{< /alternativa >}}

{{< solucao letra="C" >}}
O compilador gera automaticamente diversos métodos úteis para records.
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

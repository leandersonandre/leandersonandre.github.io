---
title: "Questões sobre Modelagem de Domínio"
slug: modelagem-de-dominio-questoes
description: "Lista de questões sobre modelagem de domínio"
tags:
- modelagem
- questões
---

{{< lista-questoes >}}

{{< questao >}}
Em um sistema acadêmico, deseja-se representar alunos de uma instituição de ensino. Cada aluno deve possuir nome, matrícula e idade, sendo esses dados protegidos contra acesso direto externo. Além disso, o sistema deve permitir apenas leitura e atualização controlada desses dados por meio de métodos apropriados. Modele a classe Aluno em UML, incluindo atributos, métodos de acesso e justificando a escolha da visibilidade.
{{< solucao letra="A">}}
{{< plantuml >}}
class Aluno {
  -nome: String
  -matricula: String
  -idade: int
  +getNome(): String
  +setNome(nome: String): void
  +getMatricula(): String
  +setMatricula(matricula: String): void
  +getIdade(): int
  +setIdade(idade: int): void
}
{{< /plantuml >}}

A visibilidade privada dos atributos garante encapsulamento, impedindo acesso direto e protegendo o estado interno do objeto. Os métodos públicos (getters e setters) controlam a leitura e modificação dos dados, permitindo validações futuras sem comprometer a integridade da classe.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Em um sistema escolar, um professor pode ministrar várias disciplinas, e cada disciplina pode ser ministrada por apenas um professor responsável. Modele essa relação em UML, indicando corretamente a multiplicidade entre as classes e justificando a escolha do relacionamento.
{{< solucao letra="B">}}
{{< plantuml >}}
class Professor {
  -nome: String
}

class Disciplina {
  -nome: String
}

Professor "1" -- "0..*" Disciplina
{{< /plantuml >}}

A multiplicidade indica que um professor pode estar associado a várias disciplinas (0..*), enquanto cada disciplina está vinculada a um único professor (1). Isso caracteriza uma associação estruturada com cardinalidade bem definida.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Em um sistema de e-commerce, um carrinho de compras contém produtos adicionados pelo usuário. Esses produtos podem existir independentemente do carrinho e podem ser reutilizados em diferentes compras. Modele essa estrutura em UML e justifique o tipo de relacionamento utilizado.
{{< solucao letra="C">}}
{{< plantuml >}}
class Carrinho {
  -id: int
}

class Produto {
  -nome: String
  -preco: double
}

Carrinho "1" o-- "0..*" Produto
{{< /plantuml >}}

O relacionamento é uma agregação, pois os produtos possuem existência independente do carrinho. O carrinho apenas agrupa produtos temporariamente sem ser responsável por seu ciclo de vida.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Em um sistema bancário, uma conta corrente deve permitir operações de depósito, saque e consulta de saldo. O saldo não pode ser acessado diretamente, apenas modificado ou consultado por métodos específicos. Modele essa classe em UML e justifique o encapsulamento aplicado.
{{< solucao letra="D">}}
{{< plantuml >}}
class ContaBancaria {
  -saldo: double
  +depositar(valor: double): void
  +sacar(valor: double): void
  +getSaldo(): double
}
{{< /plantuml >}}

O atributo saldo é privado para evitar alterações diretas e inconsistentes. As operações públicas garantem regras de negócio, como validação de saque e atualização controlada do estado da conta.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Em um sistema de modelagem residencial, uma casa é composta por cômodos como quartos, cozinha e banheiro. Esses cômodos não fazem sentido existir fora do contexto da casa. Modele essa estrutura em UML e justifique o tipo de relacionamento escolhido.
{{< solucao letra="E">}}
{{< plantuml >}}
class Casa {
  -endereco: String
}

class Comodo {
  -nome: String
}

Casa *-- "1..*" Comodo
{{< /plantuml >}}

O relacionamento é composição, pois os cômodos dependem totalmente da casa para existir. Se a casa for destruída, seus cômodos deixam de existir no modelo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Em um sistema de transporte, veículos possuem características comuns como marca, modelo e ano de fabricação. Carros e motos são tipos específicos de veículos com comportamentos próprios, mas compartilham essas características. Modele essa hierarquia em UML e justifique o uso de herança.
{{< solucao letra="F">}}
{{< plantuml >}}
class Veiculo {
  -marca: String
  -modelo: String
  -ano: int
}

class Carro
class Moto

Veiculo <|-- Carro
Veiculo <|-- Moto
{{< /plantuml >}}

A herança é utilizada porque Carro e Moto são especializações de Veiculo. Isso permite reutilização de atributos comuns e facilita a aplicação de polimorfismo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Em um sistema de biblioteca, um livro pode ser escrito por um ou mais autores, e um autor pode escrever vários livros ao longo do tempo. Modele essa relação em UML e justifique a multiplicidade adotada.
{{< solucao letra="G">}}
{{< plantuml >}}
class Livro {
  -titulo: String
}

class Autor {
  -nome: String
}

Livro "0..*" -- "0..*" Autor
{{< /plantuml >}}

A relação é muitos para muitos, pois não há limitação de quantidade de livros por autor nem de autores por livro, refletindo uma associação com multiplicidade N:N.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Em um sistema de pedidos, a classe Pedido utiliza a classe Pagamento apenas no momento de finalização da compra, sem manter referência permanente a ela. Modele essa situação em UML e justifique o tipo de relacionamento.
{{< solucao letra="H">}}
{{< plantuml >}}
class Pedido {
  +finalizar(): void
}

class Pagamento {
  +processar(): void
}

Pedido ..> Pagamento
{{< /plantuml >}}

Esse relacionamento é dependência, pois a classe Pedido apenas utiliza Pagamento temporariamente dentro de um método, sem armazená-lo como atributo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Em uma empresa, cada departamento possui vários funcionários vinculados a ele. No entanto, esses funcionários podem ser transferidos para outros departamentos ou até mesmo existir sem estarem alocados temporariamente. Modele essa estrutura em UML e justifique o relacionamento.
{{< solucao letra="I">}}
{{< plantuml >}}
class Funcionario {
  -nome: String
}

class Departamento {
  -nome: String
}

Departamento "1" o-- "0..*" Funcionario
{{< /plantuml >}}

O relacionamento é agregação, pois os funcionários não dependem do departamento para existir e podem ser realocados, caracterizando um vínculo fraco.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Em um sistema escolar, uma escola possui várias turmas, e cada turma possui vários alunos matriculados. Modele essa estrutura em UML e justifique o uso de multiplicidade e tipo de relacionamento entre as classes.
{{< solucao letra="J">}}
{{< plantuml >}}
class Escola {
  -nome: String
}

class Turma {
  -codigo: String
}

class Aluno {
  -nome: String
}

Escola "1" -- "0..*" Turma
Turma "1" o-- "0..*" Aluno
{{< /plantuml >}}

A escola mantém uma associação com turmas, enquanto a relação entre turma e aluno é uma agregação, pois alunos podem existir independentemente da turma e podem ser remanejados entre elas.
{{< /solucao >}}
{{< /questao >}}


{{< questao >}}
Um sistema de transporte precisa representar diferentes tipos de veículos, como carro, moto e caminhão. Todos compartilham características comuns, como placa e ano, mas cada tipo possui comportamentos específicos. Modele esse cenário utilizando herança e justifique sua decisão de projeto.
{{< solucao letra=" ">}}
{{< plantuml >}}
class Veiculo {
  -placa: String
  -ano: int
}

class Carro {
  -quantidadePortas: int
}

class Moto {
  -cilindradas: int
}

class Caminhao {
  -capacidadeCarga: double
}

Veiculo <|-- Carro
Veiculo <|-- Moto
Veiculo <|-- Caminhao
{{< /plantuml >}}

A herança foi utilizada porque existe uma generalização clara entre os veículos. Todos compartilham atributos comuns (placa e ano), que são centralizados na classe base Veiculo. Isso evita duplicação de código e facilita manutenção. As subclasses representam especializações com características próprias, como cilindradas ou capacidade de carga, respeitando o princípio de reutilização e extensão do modelo.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Em um sistema de funcionários de uma empresa, existem diferentes tipos de colaboradores: funcionário efetivo e estagiário. Ambos possuem nome e salário, mas apenas o estagiário possui bolsa auxílio e o funcionário efetivo possui bônus. Modele essa estrutura utilizando herança e explique a escolha.
{{< solucao letra=" ">}}
{{< plantuml >}}
class Funcionario {
  -nome: String
  -salario: double
}

class FuncionarioEfetivo {
  -bonus: double
}

class Estagiario {
  -bolsaAuxilio: double
}

Funcionario <|-- FuncionarioEfetivo
Funcionario <|-- Estagiario
{{< /plantuml >}}

A herança foi escolhida porque existe uma entidade genérica (Funcionario) que representa características comuns a todos os tipos de colaboradores. As subclasses especializam esse comportamento adicionando atributos específicos. Isso garante uma hierarquia clara, facilita a evolução do sistema e evita repetição de atributos comuns como nome e salário.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Um sistema de pagamentos precisa lidar com diferentes formas de pagamento, como cartão de crédito, boleto e PIX. Todas as formas possuem um processo de pagamento, mas cada uma implementa esse processo de maneira diferente. Modele esse cenário usando herança e explique a decisão arquitetural.
{{< solucao letra=" ">}}
{{< plantuml >}}
class Pagamento {
  +processar(): void
}

class CartaoCredito {
  -numero: String
}

class Boleto {
  -codigoBarras: String
}

class Pix {
  -chave: String
}

Pagamento <|-- CartaoCredito
Pagamento <|-- Boleto
Pagamento <|-- Pix
{{< /plantuml >}}

A herança foi aplicada porque existe um comportamento comum (processar pagamento) que deve ser garantido para todas as formas de pagamento, mas com implementações diferentes. A classe base Pagamento define a abstração do comportamento, enquanto as subclasses implementam variações específicas. Isso favorece polimorfismo e reduz acoplamento no sistema.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Em um sistema de gestão universitária, existem diferentes tipos de pessoas: Professor e Aluno, ambos com nome e CPF. A universidade também possui Departamentos, e cada departamento agrupa professores, mas esses professores podem existir independentemente da existência do departamento. Modele esse cenário utilizando herança e agregação, e justifique sua modelagem.
{{< solucao letra=" ">}}
{{< plantuml >}}
class Pessoa {
  -nome: String
  -cpf: String
}

class Professor {
  -titulacao: String
}

class Aluno {
  -matricula: String
}

class Departamento {
  -nome: String
}

Pessoa <|-- Professor
Pessoa <|-- Aluno

Departamento "1" o-- "0..*" Professor
{{< /plantuml >}}

A herança é utilizada porque Professor e Aluno são especializações de Pessoa, compartilhando atributos comuns como nome e CPF. A agregação entre Departamento e Professor foi escolhida porque o professor não depende do departamento para existir; ele pode ser realocado ou existir independentemente da estrutura organizacional. Isso caracteriza uma relação fraca de pertencimento, onde o ciclo de vida do professor não é controlado pelo departamento.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Em um sistema de pedidos online, existem diferentes tipos de usuários: Cliente e Administrador, ambos com dados básicos de usuário. Um Cliente pode registrar pedidos no sistema. Cada Pedido é composto por Itens de Pedido, e cada item é parte indivisível do pedido, não existindo sem ele.

Modele esse cenário e justifique sua decisão de modelagem.
{{< solucao letra=" ">}}
{{< plantuml >}}
class Usuario {
  -id: int
  -nome: String
}

class Cliente {
  -endereco: String
}

class Administrador {
  -nivelAcesso: int
}

class Pedido {
  -numero: int
  -data: Date
}

class ItemPedido {
  -produto: String
  -quantidade: int
}

Usuario <|-- Cliente
Usuario <|-- Administrador

Cliente "1" --> "0..*" Pedido : registra
Pedido *-- "1..*" ItemPedido
{{< /plantuml >}}

A herança é utilizada porque Cliente e Administrador são especializações de Usuario, compartilhando atributos e comportamentos comuns. A associação entre Cliente e Pedido representa o fato de que o cliente registra pedidos, mas ambos possuem ciclos de vida independentes. Já a composição entre Pedido e ItemPedido é adequada porque os itens não existem sem o pedido; eles fazem parte estrutural dele e são destruídos junto com ele, caracterizando forte dependência de ciclo de vida.
{{< /solucao >}}
{{< /questao >}}

{{< questao >}}
Em um sistema de transporte público, existem diferentes tipos de veículos: Ônibus e Trem, ambos derivados de Veículo. Cada veículo pode estar associado a um Motorista responsável, porém o motorista não pertence exclusivamente a um veículo e pode dirigir diferentes veículos ao longo do tempo. Modele esse cenário utilizando herança e associação direta e justifique sua decisão.
{{< solucao letra=" ">}}
{{< plantuml >}}
class Veiculo {
  -placa: String
}

class Onibus {
  -linha: String
}

class Trem {
  -numeroVagoes: int
}

class Motorista {
  -nome: String
  -cnh: String
}

Veiculo <|-- Onibus
Veiculo <|-- Trem

Veiculo --> Motorista
{{< /plantuml >}}

A herança é usada porque Ônibus e Trem são tipos específicos de Veículo, compartilhando atributos como placa. A associação direta entre Veículo e Motorista representa uma relação flexível, onde o motorista não depende do veículo nem o veículo depende do motorista. Não há controle de ciclo de vida entre eles, apenas uma ligação funcional temporária ou operacional, o que caracteriza uma associação simples.
{{< /solucao >}}
{{< /questao >}}

{{< /lista-questoes >}}

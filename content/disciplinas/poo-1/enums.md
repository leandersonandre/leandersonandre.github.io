---
title: "Enumeradores"
slug: "enums"
description: "Tipo Enum"
tags:
- enum
---


## Definição

*Enumeradores* é um tipo especial de classe que define um conjunto de objetos imutáveis.


## Representação de enumeradores na UML

Nos diagramas de classe da UML, os enumeradores são representados pelo estereótipo `enumeration`. Os valores da enumeração devem estar em caixa alta.

{{< tabs items="Diagrama,PlantUML" >}}
{{< tab >}}
{{< plantuml >}}
enum Prioridade <<enumeration>> {
  BAIXA
  MEDIA
  ALTA
  URGENTE
}
{{< /plantuml >}}
{{< /tab >}}
{{< tab >}}
Como criar o diagrama utilizando PlantUML.
```plantuml
enum Prioridade <<enumeration>> {
  BAIXA
  MEDIA
  ALTA
  URGENTE
}
```
{{< /tab >}}

{{< /tabs >}}

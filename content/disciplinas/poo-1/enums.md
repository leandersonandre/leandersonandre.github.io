---
title: "Enumeradores"
slug: "enums"
description: "Tipo Enum"
tags:
- enum
---


## Definição

*Enumeradores* é um tipo especial de classe que define um conjunto de objetos imutáveis.


## Implementação de enumeradores no Java

```java
public enum Prioridade{
  BAIXA,
  MEDIA,
  ALTA,
  URGENTE
}
```


```java
Prioridade p = Prioridade.BAIXA;

// BAIXA
System.out.println(p);
```

```java
Prioridade p = Prioridade.ALTA;

if(p == Prioridade.ALTA){
  System.out.println("A prioridade é alta");
}
```

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

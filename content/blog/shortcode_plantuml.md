---
title: "My shortcode for PlantUML"
slug: shortcode-plantuml
description: "My shortcode for PlantUML in Hugo"
date: "2026-04-19"
tags:
- hugo
- shortcode
- plantuml
---

My shortcode to create diagrams with PlantUML.
This shortcode uses Kroki to render PlantUML diagrams.


### Example

The following example shows how to use the shortcode and its rendered output.

**Code**
```
{{</* plantuml */>}}
class Person {
  -id: long
  +getId():long
  +setId(id: long)
}
{{</* /plantuml */>}}
```

**Result**

{{< plantuml >}}
class Person {
  -id: long
  +getId():long
  +setId(id: long)
}
{{< / plantuml >}}

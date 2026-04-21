---
title: "Class Diagram with PlantUML"
slug: class-diagram-with-plantuml
description: "How to create a class diagram with PlantUML"
date: "2025-05-07"
tags:
- uml
- plantuml
---

Here's a minimalistic way to create class diagrams using PlantUML with a plain, distraction-free style.

We use the !theme plain directive and tweak the appearance with skinparam and hide commands to keep it clean and focused on the structure. This is especially useful for documentation, teaching, or quickly prototyping designs.

```plantuml
!theme plain
skinparam classAttributeIconSize 0
hide circle
class User{
  -name:String
  -username:String
  -active:boolean
  +isActive():boolean
}
```

{{< plantuml >}}
class User{
  -name:String
  -username:String
  -active:boolean
  +isActive():boolean
}
{{< /plantuml >}}
## Explanation:
**!theme plain:** Removes colors and styles to emphasize the content.

**skinparam classAttributeIconSize 0:** Hides icons next to attributes/methods.

**hide circle:** Removes small circles (like composition indicators) for a cleaner look.

This setup is great if you're aiming for simplicity in presentations or printed materials.

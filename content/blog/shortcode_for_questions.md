---
title: "My shortcode for Questions"
slug: shortcode-for-questions
description: "My shortcode for questions in Hugo"
date: "2026-04-19"
tags:
- hugo
- shortcode
- questions
---

This shortcode is useful for displaying questions with hidden solutions. Question numbers and answer option letters are automatically generated.
This shortcode supports [PlantUML](/blog/shortcode-plantuml) and [code](/blog/shortcode-code) rendering shortcodes.

### Usage

The following example shows how to use the shortcode and its rendered output.

**Code**
```text
{{</* lista-questoes */>}}

{{</* questao */>}}

The question description

{{</* alternativa */>}}
Question alternative
{{</* /alternativa */>}}

{{</* alternativa */>}}
Question alternative
{{</* /alternativa */>}}

{{</* solucao letra="B" */>}}
The question solution
{{</* /solucao */>}}

{{</* /questao */>}}

{{</* /lista-questoes */>}}
```

**Result**

{{< lista-questoes >}} 
{{< questao >}} 
The question description 
{{< alternativa >}} 
Question alternative 
{{< /alternativa >}} 
{{< alternativa >}} 
Question alternative 
{{< /alternativa >}} 
{{< solucao letra="B">}} 
The question solution 
{{< /solucao >}} 
{{< /questao >}} 
{{< /lista-questoes >}}

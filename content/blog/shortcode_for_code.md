---
title: "My shortcode for Code"
slug: shortcode-code
description: "My shortcode for code in Hugo"
date: "2026-04-19"
tags:
- hugo
- shortcode
- code
---

This shortcode is useful when you want to display raw code without syntax highlighting or automatic formatting from Hugo. It ensures the output is rendered exactly as written.


### Usage

The following example shows how to use the shortcode and its rendered output.

**Code**
```text
{{</* code */>}}
public String toString() {
    return null;
}
{{</* /code */>}}
```

**Result**

{{< code >}}
public String toString() {
    return null;
}
{{< /code >}}

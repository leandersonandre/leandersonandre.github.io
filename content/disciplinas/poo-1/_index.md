---
title: "POO I"
---

## Aulas

{{< cards >}}
{{< card link="./aula-01" title="Aula 01" >}}
{{< card link="./aula-02" title="Aula 02" >}}
{{< /cards >}}

{{< plantuml >}}
@startuml
Alice -> Bob: Hello
Bob -> Alice: Hi!
@enduml
{{< /plantuml >}}

{{< tabs >}}

{{< tab name="Python" >}}
```python
def fibonacci(n):
    if n <= 1:
        return n

    a, b = 0, 1
    for _ in range(2, n + 1):
        a, b = b, a + b

    return b


# exemplo de uso
for i in range(10):
    print(fibonacci(i))
```
{{< /tab >}}

{{< tab name="Java" >}}
```java
public class Fibonacci {

    public static int fibonacci(int n) {
        if (n <= 1) {
            return n;
        }

        int a = 0, b = 1;

        for (int i = 2; i <= n; i++) {
            int temp = a + b;
            a = b;
            b = temp;
        }

        return b;
    }

    public static void main(String[] args) {
        for (int i = 0; i < 10; i++) {
            System.out.println(fibonacci(i));
        }
    }
}
```
{{< /tab >}}

{{< /tabs >}}

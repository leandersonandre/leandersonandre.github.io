---

title: "Arranjos (Arrays)"
description: "Conceito de arranjos na linguagem Java"
tags:
- java
- arrays
- estruturas-de-dados
- memória
---

Na linguagem Java, um arranjo (array, vetor) é uma estrutura de dados utilizada para armazenar múltiplos valores do mesmo tipo em uma única variável. Ele é organizado como um bloco único e contínuo de memória, no qual os elementos são armazenados de forma sequencial.

Diferente de outras estruturas mais flexíveis, o array possui tamanho fixo. Isso significa que, no momento em que ele é criado, é necessário definir quantas posições ele terá, não sendo possível aumentar ou diminuir esse tamanho posteriormente.

## Declaração e acesso

```java
int[] numeros = new int[5];
```

Nesse exemplo, é criado um array com cinco posições. Os elementos são acessados por meio de índices, que representam suas posições dentro do arranjo. O índice sempre começa em zero, portanto o primeiro elemento está na posição 0 e o último na posição tamanho - 1.

```java
numeros[0] = 10;
numeros[1] = 20;

System.out.println(numeros[0]);
```

## Organização na memória

Como os elementos estão armazenados de forma contínua na memória, é possível acessar qualquer posição diretamente, sem necessidade de percorrer os demais elementos. Isso acontece porque o endereço de cada elemento pode ser calculado a partir de uma fórmula simples.

```text
endereço = endereço_base + (índice × tamanho_do_tipo)
```

O endereço_base representa a posição inicial do array na memória. O índice indica qual elemento se deseja acessar. O tamanho_do_tipo corresponde à quantidade de bytes ocupada pelo tipo de dado armazenado, como por exemplo 4 bytes para um inteiro.

Considerando um exemplo em que o endereço base seja 1000 e o tipo seja inteiro (4 bytes), o endereço do elemento na posição 2 seria calculado da seguinte forma:

```text
endereço = 1000 + (2 × 4)
endereço = 1008
```

Essa organização em memória permite acesso rápido e eficiente aos elementos do array.

## Inicialização

A inicialização pode ser feita diretamente no momento da declaração:

```java
int[] valores = {10, 20, 30, 40};
```

Ou preenchendo os valores posteriormente:

```java
int[] valores = new int[3];

valores[0] = 5;
valores[1] = 10;
valores[2] = 15;
```

## Valores padrão

Quando um array é criado em Java, suas posições são automaticamente inicializadas com valores padrão, mesmo que nenhum valor seja atribuído explicitamente.

```java
int[] numeros = new int[3];
System.out.println(numeros[0]); // 0
```

Tipos inteiros como int, short, byte e long recebem 0. Tipos de ponto flutuante como float e double recebem 0.0. O tipo boolean recebe false. Tipos por referência, como String e objetos, recebem null.

Esse comportamento garante que o array sempre esteja inicializado, evitando acesso a valores indefinidos.

## Tamanho do arranjo

O tamanho de um array em Java é definido no momento da sua criação e não pode ser alterado posteriormente.

```java
int[] valores = new int[5];
System.out.println(valores.length); // 5
```

O .length não é um método, mas sim um atributo do array. Esse valor é frequentemente utilizado em estruturas de repetição para percorrer todos os elementos do arranjo de forma segura.

## Percorrendo um array

Para percorrer um array, é comum utilizar a estrutura de repetição for:

```java
int[] valores = {10, 20, 30};

for (int i = 0; i < valores.length; i++) {
    System.out.println(valores[i]);
}
```

Dessa forma, evita-se acessar posições inválidas, o que causaria erro em tempo de execução.

## Percorrendo com foreach

Em Java, também é possível percorrer um array utilizando a estrutura foreach. Nesse tipo de repetição, não é necessário utilizar índices, pois o laço percorre automaticamente todos os elementos do arranjo.

```java id="w7k3mz"
int[] valores = {10, 20, 30};

for (int valor : valores) {
    System.out.println(valor);
}
```



Nesse caso, a variável `valor` recebe diretamente cada elemento do array a cada iteração, simplificando o código e reduzindo a chance de erros relacionados a índices.

## Imprimir um array

Para imprimir todos os elementos de um array em Java, pode-se utilizar a estrutura foreach, que percorre automaticamente cada valor do arranjo.

```java id="c9v2hz"
int[] valores = {10, 20, 30, 40};

for (int valor : valores) {
    System.out.print(valor + " ");
}
```

Nesse exemplo, todos os elementos do array são exibidos em sequência na mesma linha.

## Impressão com Arrays.toString

Em Java, ao tentar imprimir um array diretamente, o resultado não mostra seus elementos, mas sim uma representação interna do objeto em hexadecimal.

```java id="x2v8qp"
int[] valores = {10, 20, 30};

System.out.println(valores);
```

Saída esperada (exemplo):

```text id="p4zn8a"
[I@15db9742
```

Esse valor representa o tipo do array e seu endereço na memória, não os dados armazenados.

Para imprimir corretamente os elementos do array, utiliza-se o método `Arrays.toString`, da classe `Arrays`.

```java id="n8y3rd"
import java.util.Arrays;

int[] valores = {10, 20, 30};

System.out.println(Arrays.toString(valores));
```

Saída:

```text id="6j2qwf"
[10, 20, 30]
```

Dessa forma, os elementos do array são exibidos de maneira legível.



## Conclusão

Arrays são estruturas simples e eficientes, caracterizadas por armazenamento contínuo em memória, acesso por índice e tamanho fixo definido na criação.

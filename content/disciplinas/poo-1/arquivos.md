---
title: "Manipulação de Arquivos"
slug: "arquivos"
description: "arquivos"
tags:
- arquivos
- json
- serializacao
---


## Definição


Um **arquivo** é uma unidade de armazenamento de dados utilizada para guardar informações de forma permanente em um dispositivo, como um disco rígido, SSD, pendrive ou armazenamento em nuvem. Um arquivo pode conter diferentes tipos de conteúdo, como textos, imagens, vídeos, áudios ou dados utilizados por programas.

Cada arquivo normalmente possui um **nome**, uma **extensão** (que indica seu tipo, como `.txt`, `.pdf` ou `.jpg`) e está localizado em um diretório ou pasta dentro do sistema de arquivos.


## Leitura de arquivos


A plataforma Java oferece diferentes maneiras de realizar a leitura de arquivos. O framework Java NIO oferece uma das formas mais simples de ler um arquivo de texto.

```java
Path path = Paths.get("meu_arquivo.txt");

var linhas = Files.readAllLines(path);
```

O método `Paths.get` cria um objeto do tipo `Path`, que representa o caminho para o arquivo no sistema de arquivos. Esse objeto não realiza a leitura nem a abertura efetiva do arquivo; ele apenas encapsula o caminho informado.

Em seguida, o método `Files.readAllLines` lê todo o conteúdo do arquivo e retorna uma lista de linhas (`List<String>`), onde cada elemento corresponde a uma linha do arquivo.

Por exemplo:

```java
for (String linha : linhas) {
    System.out.println(linha);
}
```

Esse código percorre todas as linhas lidas do arquivo e as exibe no console.

**Atenção:** o método `readAllLines` carrega todo o conteúdo do arquivo na memória. Para arquivos muito grandes, pode ser mais adequado utilizar abordagens baseadas em streams, como `Files.lines`.

### Leitura com `Files.lines`

Para arquivos maiores, uma alternativa mais eficiente é utilizar o método `Files.lines`, que retorna um `Stream<String>`. Dessa forma, as linhas são processadas sob demanda, sem a necessidade de carregar todo o arquivo na memória de uma só vez.

```java
Path path = Paths.get("meu_arquivo.txt");

try (Stream<String> linhas = Files.lines(path)) {
    linhas.forEach(System.out::println);
}
```

Nesse exemplo, cada linha do arquivo é lida e exibida no console.

O bloco `try-with-resources` garante que o arquivo seja fechado automaticamente após o término da leitura.

Também é possível utilizar as operações da API de Streams para filtrar e transformar os dados:

```java
Path path = Paths.get("meu_arquivo.txt");

try (Stream<String> linhas = Files.lines(path)) {
    linhas
        .filter(linha -> !linha.isBlank())
        .map(String::toUpperCase)
        .forEach(System.out::println);
}
```

Nesse caso, apenas as linhas não vazias são processadas e convertidas para letras maiúsculas antes de serem exibidas.

## Escrita de arquivos

O framework Java NIO também fornece métodos simples para escrever arquivos. A maneira mais direta é utilizar o método `Files.write`, que grava uma coleção de linhas em um arquivo.

```java
Path path = Paths.get("meu_arquivo.txt");

List<String> linhas = List.of(
    "Primeira linha",
    "Segunda linha",
    "Terceira linha"
);

Files.write(path, linhas);
```

Se o arquivo não existir, ele será criado automaticamente. Caso já exista, seu conteúdo será substituído pelo novo conteúdo.

### Acrescentando conteúdo ao arquivo

Para adicionar conteúdo ao final de um arquivo existente, utilize a opção `StandardOpenOption.APPEND`.

```java
Path path = Paths.get("meu_arquivo.txt");

Files.write(
    path,
    List.of("Nova linha"),
    StandardOpenOption.APPEND
);
```

### Escrevendo uma única String

Também é possível gravar diretamente uma `String` utilizando o método `Files.writeString`.

```java
Path path = Paths.get("meu_arquivo.txt");

Files.writeString(
    path,
    "Olá, mundo!"
);
```

Para adicionar texto ao final do arquivo:

```java
Path path = Paths.get("meu_arquivo.txt");

Files.writeString(
    path,
    "\nNova linha",
    StandardOpenOption.APPEND
);
```

Assim como na leitura, os métodos da classe `Files` são adequados para operações simples. Para arquivos muito grandes ou quando é necessário escrever dados continuamente, pode ser mais apropriado utilizar classes como `BufferedWriter`.

### Criando ou adicionando conteúdo

Uma combinação bastante comum é utilizar as opções `CREATE` e `APPEND`. Nesse caso, o arquivo será criado caso não exista. Se já existir, o conteúdo será adicionado ao final do arquivo.

```java
Path path = Paths.get("log.txt");

Files.writeString(
    path,
    "Nova mensagem\n",
    StandardOpenOption.CREATE,
    StandardOpenOption.APPEND
);
```

## Manipulação de arquivos no modo binário

Arquivos binários armazenam dados na forma de bytes, sem uma representação textual legível para humanos. Esse formato é frequentemente utilizado para imagens, vídeos, arquivos compactados e também para o armazenamento eficiente de estruturas de dados.

Em Java, podemos utilizar as classes `DataOutputStream` e `DataInputStream` para escrever e ler dados binários.

### Gravando records em um arquivo binário

Considere o seguinte record:

```java
public record Person(
    String name,
    String surname
) {}
```

Suponha uma lista de pessoas:

```java
List<Person> people = List.of(
    new Person("João", "Silva"),
    new Person("Maria", "Souza"),
    new Person("Pedro", "Santos")
);
```

Podemos armazenar essa lista em um arquivo binário utilizando um `DataOutputStream`:

```java
Path path = Paths.get("people.dat");

try (
    var out = new DataOutputStream(
        Files.newOutputStream(path)
    )
) {
    out.writeInt(people.size());

    for (Person person : people) {
        out.writeUTF(person.name());
        out.writeUTF(person.surname());
    }
}
```

Nesse exemplo:

- O número de registros é gravado primeiro utilizando `writeInt`.
- Para cada pessoa, o nome e o sobrenome são gravados utilizando `writeUTF`.

### Lendo records de um arquivo binário

Para recuperar os dados do arquivo, utilizamos um `DataInputStream`:

```java
Path path = Paths.get("people.dat");

List<Person> people = new ArrayList<>();

try (
    var in = new DataInputStream(
        Files.newInputStream(path)
    )
) {
    int size = in.readInt();

    for (int i = 0; i < size; i++) {
        String name = in.readUTF();
        String surname = in.readUTF();

        people.add(
            new Person(name, surname)
        );
    }
}
```

O código realiza a leitura na mesma ordem em que os dados foram gravados:

1. Lê a quantidade de registros.
2. Lê o nome.
3. Lê o sobrenome.
4. Reconstrói o objeto `Person`.

### Importância da ordem dos dados

Ao trabalhar com arquivos binários, a ordem de leitura deve ser exatamente a mesma utilizada durante a gravação. Caso contrário, os dados serão interpretados incorretamente.

Por exemplo, se o arquivo foi gravado utilizando:

```java
out.writeUTF(person.name());
out.writeUTF(person.surname());
```

A leitura deve seguir a mesma sequência:

```java
String name = in.readUTF();
String surname = in.readUTF();
```

Caso a ordem seja alterada, os valores recuperados não corresponderão aos dados originais.

### Vantagens dos arquivos binários

- Menor espaço de armazenamento quando comparado a formatos textuais.
- Leitura e escrita geralmente mais rápidas.
- Permitem armazenar tipos de dados primitivos diretamente (`int`, `long`, `double`, etc.).
- São adequados para persistir estruturas de dados quando não há necessidade de edição manual do arquivo.

A principal desvantagem é que o conteúdo não pode ser facilmente inspecionado ou editado por um ser humano, exigindo que a aplicação conheça o formato utilizado para interpretar os dados corretamente.

## Serialização de objetos

A serialização é o processo de converter um objeto em uma sequência de bytes para que ele possa ser armazenado em um arquivo, transmitido pela rede ou persistido em outro meio de armazenamento.

Posteriormente, essa sequência de bytes pode ser utilizada para reconstruir o objeto original por meio do processo de desserialização.

### Tornando um objeto serializável

Para que um objeto possa ser serializado utilizando a API padrão do Java, sua classe deve implementar a interface `Serializable`.

```java
import java.io.Serializable;

public record Person(
    String name,
    String surname
) implements Serializable {}
```

A interface `Serializable` não possui métodos. Ela funciona apenas como uma marcação indicando que objetos daquela classe podem ser serializados.

### Gravando objetos em um arquivo

O Java fornece a classe `ObjectOutputStream` para serializar objetos.

```java
List<Person> people = List.of(
    new Person("João", "Silva"),
    new Person("Maria", "Souza")
);

Path path = Paths.get("people.ser");

try (
    var out = new ObjectOutputStream(
        Files.newOutputStream(path)
    )
) {
    out.writeObject(people);
}
```

Nesse exemplo, toda a lista de pessoas é serializada e gravada em um único arquivo.

### Lendo objetos de um arquivo

Para reconstruir os objetos serializados, utiliza-se a classe `ObjectInputStream`.

```java
Path path = Paths.get("people.ser");

try (
    var in = new ObjectInputStream(
        Files.newInputStream(path)
    )
) {
    @SuppressWarnings("unchecked")
    List<Person> people =
        (List<Person>) in.readObject();

    System.out.println(people);
}
```

O método `readObject` retorna um `Object`, sendo necessário realizar o cast para o tipo esperado.

### Funcionamento da serialização

Durante a serialização, o Java percorre o objeto e seus atributos, convertendo-os para uma representação binária.

O arquivo gerado não possui uma estrutura textual legível e deve ser interpretado utilizando a própria API de serialização do Java.

```text
people.ser
└── Dados binários do objeto
```

### Considerações sobre serialização

A serialização nativa do Java é simples de utilizar e pode ser útil para armazenamento temporário de objetos ou comunicação entre aplicações Java.

Entretanto, em aplicações modernas é comum utilizar formatos como JSON ou XML para persistência e troca de dados, pois eles são independentes da linguagem de programação e podem ser facilmente inspecionados e processados por diferentes sistemas.

Por esse motivo, a serialização nativa costuma ser reservada para cenários específicos em que aplicações Java precisam compartilhar objetos diretamente.

## Leitura e escrita de arquivos no formato JSON

JSON (*JavaScript Object Notation*) é um formato textual amplamente utilizado para armazenamento e troca de dados. Sua principal vantagem é ser legível por humanos e suportado por diversas linguagens de programação.

Em aplicações Java, uma das bibliotecas mais populares para trabalhar com JSON é a Jackson.

### Dependência

Para utilizar a Jackson em projetos Maven, adicione a seguinte dependência:

```xml
<!-- Consulte a versão mais recente da documentação -->
<dependency>
    <groupId>com.fasterxml.jackson.core</groupId>
    <artifactId>jackson-databind</artifactId>
    <version>{versao}</version>
</dependency>
```

### Escrevendo objetos em JSON

Considere o seguinte record:

```java
public record Person(
    String name,
    String surname
) {}
```

E uma lista de pessoas:

```java
List<Person> people = List.of(
    new Person("João", "Silva"),
    new Person("Maria", "Souza"),
    new Person("Pedro", "Santos")
);
```

Podemos converter essa lista para JSON e gravá-la em um arquivo utilizando a classe `ObjectMapper`.

```java
ObjectMapper mapper = new ObjectMapper();

mapper.writeValue(
    Paths.get("people.json").toFile(),
    people
);
```

O arquivo gerado terá um conteúdo semelhante ao seguinte:

```json
[
  {
    "name": "João",
    "surname": "Silva"
  },
  {
    "name": "Maria",
    "surname": "Souza"
  },
  {
    "name": "Pedro",
    "surname": "Santos"
  }
]
```

### Formatando o JSON

Por padrão, o JSON é gravado em uma única linha. Para gerar um arquivo formatado, utilize o método `writerWithDefaultPrettyPrinter`.

```java
ObjectMapper mapper = new ObjectMapper();

mapper.writerWithDefaultPrettyPrinter()
    .writeValue(
        Paths.get("people.json").toFile(),
        people
    );
```

### Lendo objetos de um arquivo JSON

Para reconstruir os objetos a partir do arquivo:

```java
ObjectMapper mapper = new ObjectMapper();

List<Person> people = mapper.readValue(
    Paths.get("people.json").toFile(),
    new TypeReference<List<Person>>() {}
);
```

Após a leitura, a variável `people` conterá os mesmos objetos que foram originalmente gravados.

### Utilizando a API Files

Também é possível combinar a Jackson com a API NIO.

Gravando:

```java
ObjectMapper mapper = new ObjectMapper();

byte[] json = mapper.writeValueAsBytes(people);

Files.write(
    Paths.get("people.json"),
    json
);
```

Lendo:

```java
ObjectMapper mapper = new ObjectMapper();

byte[] json = Files.readAllBytes(
    Paths.get("people.json")
);

List<Person> people = mapper.readValue(
    json,
    new TypeReference<List<Person>>() {}
);
```

### Vantagens do JSON

- Formato legível por humanos.
- Independente de linguagem de programação.
- Amplamente utilizado em APIs REST.
- Fácil integração com bancos de dados e serviços externos.
- Suporte nativo em diversas bibliotecas e frameworks.

Por esses motivos, JSON é frequentemente utilizado como alternativa à serialização nativa do Java para armazenamento e transferência de dados.

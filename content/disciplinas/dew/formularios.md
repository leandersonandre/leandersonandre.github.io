---
title: "Formulários"
slug: "formularios"
description: "Formularios em HTML"
tags:
- html
- formularios
- inputs
---

Um formulário é utilizado para coletar dados do usuário. Geralmente os dados são enviados para um servidor para ser processado.

```html
<form>

</form>
```

### Elemento input

O elemento input é um dos campos mais utilizados para coletar os dados do usuário. O elemento input permite informar uma gama diferente de informações. O atributo ```type``` define o tipo de campo e layout.


| Tipo                            | Explicação                                                                    | Exemplo de uso                      |
| ------------------------------- | ----------------------------------------------------------------------------- | ----------------------------------- |
| `<input type="button">`         | Cria um botão clicável sem ação automática. Normalmente usado com JavaScript. | Abrir modal, executar função        |
| `<input type="checkbox">`       | Caixa de seleção que permite marcar múltiplas opções.                         | Aceitar termos, escolher hobbies    |
| `<input type="color">`          | Permite selecionar uma cor em um seletor visual.                              | Escolher tema/cor de perfil         |
| `<input type="date">`           | Campo para selecionar uma data.                                               | Data de nascimento                  |
| `<input type="datetime-local">` | Permite escolher data e hora local.                                           | Agendamento de reunião              |
| `<input type="email">`          | Campo específico para e-mail com validação automática.                        | Cadastro de usuário                 |
| `<input type="file">`           | Permite enviar arquivos do computador.                                        | Upload de imagem ou PDF             |
| `<input type="hidden">`         | Campo oculto que não aparece para o usuário.                                  | Enviar ID interno no formulário     |
| `<input type="image">`          | Usa uma imagem como botão de envio do formulário.                             | Botão personalizado                 |
| `<input type="month">`          | Permite selecionar mês e ano.                                                 | Validade de cartão                  |
| `<input type="number">`         | Campo para números, podendo limitar mínimo e máximo.                          | Quantidade de produtos              |
| `<input type="password">`       | Campo de senha com caracteres ocultos.                                        | Login                               |
| `<input type="radio">`          | Permite selecionar apenas uma opção entre várias.                             | Escolher gênero, forma de pagamento |
| `<input type="range">`          | Controle deslizante para escolher valores em intervalo.                       | Controle de volume                  |
| `<input type="reset">`          | Botão que limpa os dados do formulário.                                       | Resetar formulário                  |
| `<input type="search">`         | Campo otimizado para buscas.                                                  | Barra de pesquisa                   |
| `<input type="submit">`         | Botão que envia o formulário.                                                 | Enviar cadastro                     |
| `<input type="tel">`            | Campo para números de telefone.                                               | Cadastro de contato                 |
| `<input type="text">`           | Campo de texto simples.                                                       | Nome do usuário                     |
| `<input type="time">`           | Permite selecionar horário.                                                   | Escolher hora de consulta           |
| `<input type="url">`            | Campo específico para URLs com validação.                                     | Site pessoal                        |
| `<input type="week">`           | Permite selecionar semana e ano.                                              | Planejamento semanal                |


O layout e tipo de informação do campo depende do navegador utilizado. Caso o navegador não suportar, o campo input assume o tipo ```text```.


### Atributos do input

O elemento input possui os atributos ```id```, ```name```, ```value``` e ```placeholder```.

```html
<input
    type="text"
    id="nome"
    name="nome"
    value="João"
    placeholder="Digite seu nome">
```
| Atributo      | Descrição                                                                                                  |
| ------------- | ---------------------------------------------------------------------------------------------------------- |
| `id`          | Identifica unicamente o elemento na página. É muito usado para CSS, JavaScript e associação com `<label>`. |
| `name`        | Define o nome do campo enviado ao servidor quando o formulário é submetido.                                |
| `value`       | Define o valor inicial do campo ou o valor associado ao input.                                             |
| `placeholder` | Exibe um texto de exemplo ou dica dentro do campo enquanto ele estiver vazio.                              |


## Labels

O elemento `label` define um texto para explicar qual conteúdo deve ser informado em um campo de formulário (`input`).

O `label` é associado a um `input` por meio do atributo `for`, cujo valor deve ser igual ao atributo `id` do `input` correspondente.

```html
<label for="nome">Nome:</label>
<input type="text" id="nome" name="nome" placeholder="Digite seu nome">
```

## Exemplo de Formulário

{{< tabs items="Formulário,Código HTML" >}}
{{< tab >}}

 <form>
    <table>
        <tr>
            <td><label for="nome">Nome:</label></td>
            <td><input type="text" id="nome" name="nome" placeholder="Digite seu nome"></td>
        </tr>
        <tr>
            <td><label for="email">Email:</label></td>
            <td><input type="email" id="email" name="email" placeholder="Digite seu email"></td>
        </tr>
        <tr>
            <td><label for="password">Senha:</label></td>
            <td><input type="password" id="password" name="password" placeholder="Digite seu password"></td>
        </tr>
        <tr>
            <td><input type="reset" value="Limpar"></td>
        </tr>
    </table>
</form>

{{< /tab >}}
{{< tab >}}
```html
 <form>
    <table>
        <tr>
            <td><label for="nome">Nome:</label></td>
            <td><input type="text" id="nome" name="nome" placeholder="Digite seu nome"></td>
        </tr>
        <tr>
            <td><label for="email">Email:</label></td>
            <td><input type="email" id="email" name="email" placeholder="Digite seu email"></td>
        </tr>
        <tr>
            <td><label for="password">Senha:</label></td>
            <td><input type="password" id="password" name="password" placeholder="Digite seu password"></td>
        </tr>
        <tr>
            <td><input type="reset" value="Limpar"></td>
        </tr>
    </table>
</form>
```
{{< /tab >}}
{{< /tabs >}}

Exemplo de uso de `checkbox` e `radio button`.
{{< tabs items="Formulário,Código HTML" >}}
{{< tab >}}


<form>
        <table>
            <tr>
                <td><label for="nome">Sabores da pizza:</label></td>
                <td><input type="checkbox" id="cb_4_queijos" name="cb_4_queijos">4 Queijos</td>
            </tr>
            <tr>
                <td></td>
                <td><input type="checkbox" id="cb_calabreza" name="cb_calabreza">Calabreza</td>
            </tr>
            <tr>
                <td></td>
                <td><input type="checkbox" id="cb_portuguesa" name="cb_portuguesa">Portuguesa</td>
            </tr>
            <tr>
                <td></td>
                <td><input type="checkbox" id="cb_frango_catupiry" name="cb_frango_catupiry">Frango com Catupiry</td>
            </tr>
        </table>
        <table>
            <tr>
                <td><label for="nome">Refrigerante:</label></td>
                <td><input type="radio" id="radio_cocacola" name="refrigerante">Coca-Cola</td>
            </tr>
            <tr>
                <td></td>
                <td><input type="radio" id="radio_cocacola_zero" name="refrigerante">Coca-Cola Zero</td>
            </tr>
            <tr>
                <td></td>
                <td><input type="radio" id="radio_sprite" name="refrigerante">Sprite</td>
            </tr>
            <tr>
                <td></td>
                <td><input type="radio" id="radio_fanta" name="refrigerante">Fanta Laranja</td>
            </tr>
        </table>
    </form>
{{< /tab >}}
{{< tab >}}
```html
<form>
        <table>
            <tr>
                <td><label for="nome">Sabores da pizza:</label></td>
                <td><input type="checkbox" id="cb_4_queijos" name="cb_4_queijos">4 Queijos</td>
            </tr>
            <tr>
                <td></td>
                <td><input type="checkbox" id="cb_calabreza" name="cb_calabreza">Calabreza</td>
            </tr>
            <tr>
                <td></td>
                <td><input type="checkbox" id="cb_portuguesa" name="cb_portuguesa">Portuguesa</td>
            </tr>
            <tr>
                <td></td>
                <td><input type="checkbox" id="cb_frango_catupiry" name="cb_frango_catupiry">Frango com Catupiry</td>
            </tr>
        </table>
        <table>
            <tr>
                <td><label for="nome">Refrigerante:</label></td>
                <td><input type="radio" id="radio_cocacola" name="refrigerante">Coca-Cola</td>
            </tr>
            <tr>
                <td></td>
                <td><input type="radio" id="radio_cocacola_zero" name="refrigerante">Coca-Cola Zero</td>
            </tr>
            <tr>
                <td></td>
                <td><input type="radio" id="radio_sprite" name="refrigerante">Sprite</td>
            </tr>
            <tr>
                <td></td>
                <td><input type="radio" id="radio_fanta" name="refrigerante">Fanta Laranja</td>
            </tr>
        </table>
    </form>
```
{{< /tab >}}
{{< /tabs >}}


Exemplo de uso de `range`, `data` e `color`.
{{< tabs items="Formulário,Código HTML" >}}
{{< tab >}}
<form>
        <table>
            <tr>
                <td><label for="volume">Volume:</label></td>
                <td><input type="range" id="volume" name="volume"></td>
            </tr>
            <tr>
                <td><label for="data">Data:</label></td>
                <td><input type="date" id="data" name="data"></td>
            </tr>
            <tr>
                <td><label for="cor">Cor:</label></td>
                <td><input type="color" id="cor" name="cor"></td>
            </tr>
        </table>
    </form>
{{< /tab >}}
{{< tab >}}
```html
<form>
        <table>
            <tr>
                <td><label for="volume">Volume:</label></td>
                <td><input type="range" id="volume" name="volume"></td>
            </tr>
            <tr>
                <td><label for="data">Data:</label></td>
                <td><input type="date" id="data" name="data"></td>
            </tr>
            <tr>
                <td><label for="cor">Cor:</label></td>
                <td><input type="color" id="cor" name="cor"></td>
            </tr>
        </table>
    </form>
```
{{< /tab >}}
{{< /tabs >}}


# Variavéis no JavaScript

**Var**: 
- Antigo método de declaração de variáveis, não é limitado a blocos de código e pode ser redeclarado.


```javascript
var x = 10;
console.log(x); Output: 10
```

**Let**: 
- Introduzido no ECMAScript 6 (ES6), permite a declaração de variáveis limitadas ao escopo de bloco em que são definidas, evitando redeclarações.

```javascript
let y = 20;
console.log(y); Output: 20
```

**Const**: 
- Também introduzido no ES6, declara constantes que não podem ser reatribuídas após a inicialização e também têm escopo de bloco.

```javascript
const z = 30;
console.log(z); Output: 30
```
ㅤ
# Escopo
O escopo em JavaScript refere-se à acessibilidade e visibilidade de variáveis e funções dentro de um código.
ㅤ

**Escopo Global:** 
- Variáveis declaradas fora de qualquer função ou bloco de código têm escopo global.
- Elas podem ser acessadas de qualquer lugar no código, incluindo dentro de funções ou blocos de código.
- Variáveis globais são declaradas sem a palavra-chave var, let ou const.
  
```javascript
var globalVar = "global";

function minhaFuncao() {
    console.log(globalVar); // Acessa a variável globalVar
}
minhaFuncao(); // Output: Variável global
```

ㅤ

**Escopo de Função:** 
- Variáveis declaradas dentro de uma função têm escopo local àquela função.
- Elas só podem ser acessadas dentro da função onde foram declaradas.
- Variáveis locais têm prioridade sobre variáveis globais com o mesmo nome.
```javascript
function minhaFuncao() {
    var localVar = "local";
    console.log(localVar); // Acessa a variável localVar dentro da função
}

minhaFuncao(); // Output: Variável local
console.log(localVar); // Erro: localVar não está definida
```
ㅤ

**Escopo de Bloco:**
- Introduzido no ECMAScript 6 (ES6) com as palavras-chave let e const.
- Variáveis declaradas com let e const têm escopo de bloco.
- O escopo de bloco se refere ao escopo limitado ao bloco de código em que as variáveis foram declaradas.
- Variáveis de bloco só são acessíveis dentro do bloco onde são definidas.
  
```javascript
function minhaFuncao() {
    if (true) {
        let blockVar = "bloco";
        console.log(blockVar); // Acessa a variável blockVar dentro do bloco
    }
    console.log(blockVar); // Erro: blockVar não está definida fora do bloco
}

minhaFuncao();
```
ㅤ

# Tipos de dados
  _O JavaScript suporta diversos tipos de dados, incluindo:_

1. **Number**: Representa números inteiros ou de ponto flutuante. Por exemplo: `10`, `3.14`.

2. **String**: Sequência de caracteres delimitada por aspas simples (`''`) ou aspas duplas (`""`). Por exemplo: `'Olá, mundo!'`, `"JavaScript"`.

3. **Boolean**: Representa um valor lógico verdadeiro (`true`) ou falso (`false`).

4. **Null**: Representa a ausência de valor intencional. Quando uma variável é definida como `null`, isso significa que ela não possui nenhum valor.

5. **Undefined**: Representa uma variável que foi declarada, mas ainda não foi atribuída a nenhum valor. Se uma variável é declarada sem atribuir um valor a ela, seu valor é `undefined`.

6. **Object**: Uma coleção de pares de chave-valor, onde as chaves são strings (ou símbolos) e os valores podem ser de qualquer tipo de dados, incluindo outros objetos. Por exemplo: `{ nome: 'João', idade: 30 }`.

7. **Array**: Uma coleção ordenada de valores, onde cada valor é identificado por um índice numérico. Por exemplo: `[1, 2, 3, 4, 5]`.

8. **Function**: Um objeto que contém um bloco de código que pode ser executado quando chamado. Funções em JavaScript são de primeira classe, o que significa que podem ser passadas como argumentos para outras funções, retornadas de outras funções e atribuídas a variáveis.

9.  **Symbol**: Um tipo de dado cujas instâncias são únicas e imutáveis. Símbolos são frequentemente usados como chaves de propriedade de objetos quando o objetivo é que a chave seja exclusiva.

ㅤ
# Objeto

No JavaScript, um objeto é uma estrutura de dados que permite armazenar e organizar dados de maneira mais complexa do que os tipos de dados simples, como números e strings. Um objeto é uma coleção de pares de chave-valor, onde cada chave (também conhecida como propriedade) está associada a um valor. Aqui está um exemplo básico de um objeto em JavaScript:

```javascript
var pessoa = {
    nome: "João",
    idade: 30,
    cidade: "São Paulo"
};
```

Neste exemplo, `pessoa` é um objeto com três propriedades: `nome`, `idade` e `cidade`, cada uma com seu próprio valor.

Para acessar as propriedades de um objeto, você pode usar a notação de ponto (`objeto.propriedade`) ou a notação de colchetes (`objeto['propriedade']`):

```javascript
console.log(pessoa.nome); // Output: João
console.log(pessoa['idade']); // Output: 30
```

Você também pode adicionar novas propriedades a um objeto ou modificar propriedades existentes:

```javascript
pessoa.profissao = "Engenheiro";
pessoa['idade'] = 31;

console.log(pessoa.profissao); // Output: Engenheiro
console.log(pessoa.idade); // Output: 31
```

Além disso, as propriedades de um objeto podem conter valores de qualquer tipo de dados, incluindo outros objetos, funções e até mesmo arrays:

```javascript
var carro = {
    marca: "Toyota",
    modelo: "Corolla",
    ano: 2020,
    proprietario: {
        nome: "Maria",
        idade: 25
    },
    verificarAno: function() {
        return new Date().getFullYear() - this.ano;
    }
};

console.log(carro.proprietario.nome); // Output: Maria
console.log(carro.verificarAno()); // Output: 4 (supondo que o ano atual seja 2024)
```

Os objetos são uma parte fundamental da linguagem JavaScript e são amplamente utilizados para representar dados complexos e estruturas de programação. Eles oferecem uma maneira flexível e poderosa de organizar e manipular dados em JavaScript.


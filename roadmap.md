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
# Tipos primitivos

Também conhecidos como tipos de dados primitivos, em programação são os tipos de dados básicos e fundamentais que são suportados diretamente pela linguagem de programação. Esses tipos de dados primitivos são valores simples, que não têm métodos ou propriedades próprios.

1. **Booleano**: O tipo booleano representa um valor lógico verdadeiro ou falso. Em JavaScript, os valores booleanos são `true` ou `false`. Eles são comumente usados em expressões condicionais e operações lógicas.

   
   ```javascript
   var estaChovendo = true;
   var solBrilhando = false;
   ```

2. **Número**: O tipo número representa valores numéricos, seja inteiros ou de ponto flutuante. Em JavaScript, números podem ser representados diretamente ou usando notação científica. 

   
   ```javascript
   var idade = 25;
   var altura = 1.75;
   ```

3. **String (Corda)**: O tipo string representa uma sequência de caracteres, geralmente delimitada por aspas simples (`''`) ou aspas duplas (`""`). Strings são usadas para representar texto em JavaScript.

   
   ```javascript
   var nome = 'Maria';
   var mensagem = "Olá, mundo!";
   ```

4. **Indefinido (Undefined)**: O valor `undefined` é atribuído automaticamente a variáveis que foram declaradas mas não inicializadas. Também é o valor retornado por funções que não retornam explicitamente um valor.

   
   ```javascript
   var x;
   console.log(x); // Output: undefined
   ```

5. **Nulo (Null)**: O valor `null` é usado para representar a ausência intencional de qualquer valor ou objeto. É diferente de `undefined`, que geralmente indica uma variável não inicializada.

   
   ```javascript
   var y = null;
   ```

# Exercícios


**1. Variáveis:**


Declare uma variável chamada `idade` e atribua a ela o valor correspondente à sua idade.

**Resposta:**
```javascript
var idade = 25;
```

**2. Tipos de Dados:**


Identifique o tipo de dado das seguintes variáveis:

a) `var nome = "Ana";`

b) `var numero = 10;`

c) `var estaChovendo = true;`

**Resposta:**
a) `String`
b) `Number`
c) `Boolean`

**3. Declaração de Variáveis:**


Declare e inicialize uma variável para armazenar o seu país de origem.

**Resposta:**
```javascript
var paisOrigem = "Brasil";
```

**4. Escopo (Global, Bloco, Função):**


Determine se as seguintes variáveis têm escopo global, de bloco ou de função:

a) `var nome = "João";`

b) `let idade = 30;`

c) 
```javascript
function minhaFuncao() {
    var cidade = "São Paulo";
}
```

**Resposta:**
a) Escopo Global
b) Escopo de Bloco
c) Escopo de Função

**5. Tipos Primitivos:**


Identifique os tipos primitivos das seguintes variáveis:

a) `var salario = 2500;`

b) `var endereco = null;`

c) `var temperatura;`

**Resposta:**
a) `Number`
b) `Null`
c) `Undefined`




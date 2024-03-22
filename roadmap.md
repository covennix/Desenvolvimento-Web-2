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


# Objeto

Em JavaScript, um objeto é uma estrutura de dados que permite armazenar e organizar dados de maneira mais complexa do que os tipos de dados simples, como números e strings. Um objeto é uma coleção de pares de chave-valor, onde cada chave (também conhecida como propriedade) está associada a um valor.

```javascript
var pessoa = {
    nome: "João",
    idade: 30,
    cidade: "São Paulo"
};
```

Neste exemplo, `pessoa` é um objeto com três propriedades: `nome`, `idade` e `cidade`, cada uma com seu próprio valor.

Para acessar as propriedades de um objeto, podemos usar a notação de ponto (`objeto.propriedade`) ou a notação de colchetes (`objeto['propriedade']`):

```javascript
console.log(pessoa.nome); // Output: João
console.log(pessoa['idade']); // Output: 30
```

Também podemos adicionar novas propriedades a um objeto ou modificar propriedades existentes:

```javascript
pessoa.profissao = "Engenheiro";
pessoa['idade'] = 31;

console.log(pessoa.profissao); // Output: Engenheiro
console.log(pessoa.idade); // Output: 31
```

As propriedades de um objeto podem conter valores de qualquer tipo de dados, incluindo outros objetos, funções e até mesmo arrays:

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

# Array

Um array é uma estrutura de dados que permite armazenar múltiplos valores em uma única variável. Os valores em um array podem ser de qualquer tipo de dados, incluindo números, strings, objetos, outros arrays e até mesmo funções. Um array é uma coleção ordenada de elementos, onde cada elemento é identificado por um índice numérico.

### Criando Arrays:
Existem várias maneiras de criar um array em JavaScript:

1. **Notação Literal de Array**: Utilizando colchetes `[]` e inserindo os elementos separados por vírgulas.

   ```javascript
   var numeros = [1, 2, 3, 4, 5];
   var nomes = ["Ana", "João", "Maria"];
   ```

2. **Constructor Array**: Utilizando o construtor `Array()` e passando os elementos como argumentos.

   ```javascript
   var frutas = new Array("Maçã", "Banana", "Laranja");
   ```

### Acessando Elementos:
Os elementos de um array são acessados utilizando seus índices, que começam em 0 e vão até o comprimento do array menos 1.

```javascript
var frutas = ["Maçã", "Banana", "Laranja"];
console.log(frutas[0]); // Output: Maçã
console.log(frutas[1]); // Output: Banana
console.log(frutas[2]); // Output: Laranja
```

### Propriedades e Métodos de Array:
JavaScript fornece várias propriedades e métodos embutidos para manipular arrays:

- `length`: Propriedade que retorna o número de elementos em um array.

  ```javascript
  var numeros = [1, 2, 3, 4, 5];
  console.log(numeros.length); // Output: 5
  ```

- `push()`: Método que adiciona um ou mais elementos ao final de um array e retorna o novo comprimento do array.

  ```javascript
  var frutas = ["Maçã", "Banana"];
  frutas.push("Laranja");
  console.log(frutas); // Output: ["Maçã", "Banana", "Laranja"]
  ```

- `pop()`: Método que remove o último elemento de um array e retorna esse elemento.

  ```javascript
  var frutas = ["Maçã", "Banana", "Laranja"];
  var ultimaFruta = frutas.pop();
  console.log(ultimaFruta); // Output: Laranja
  console.log(frutas); // Output: ["Maçã", "Banana"]
  ```

- `forEach()`: Método que executa uma função para cada elemento do array.

  ```javascript
  var numeros = [1, 2, 3, 4, 5];
  numeros.forEach(function(numero) {
      console.log(numero);
  });
  // Output:
  // 1
  // 2
  // 3
  // 4
  // 5
  ```

# Operadores básicos

### 1. Operadores Aritméticos:
Operadores aritméticos são utilizados para realizar operações matemáticas básicas. Os principais operadores aritméticos em JavaScript são:

- `+`: Adição
- `-`: Subtração
- `*`: Multiplicação
- `/`: Divisão
- `%`: Resto da divisão (módulo)
- `++`: Incremento
- `--`: Decremento


```javascript
var a = 10;
var b = 5;
console.log(a + b); // Output: 15
console.log(a - b); // Output: 5
console.log(a * b); // Output: 50
console.log(a / b); // Output: 2
console.log(a % b); // Output: 0
console.log(++a);   // Output: 11
console.log(--b);   // Output: 4
```

### 2. Operadores de Comparação:
Operadores de comparação são utilizados para comparar valores e retornar um resultado booleano. Os principais operadores de comparação em JavaScript são:

- `==`: Igual a
- `!=`: Diferente de
- `===`: Estritamente igual a (valor e tipo)
- `!==`: Estritamente diferente de (valor e tipo)
- `>`: Maior que
- `<`: Menor que
- `>=`: Maior ou igual a
- `<=`: Menor ou igual a


```javascript
var x = 10;
var y = 5;
console.log(x == y);  // Output: false
console.log(x != y);  // Output: true
console.log(x === "10");  // Output: false
console.log(x !== "10");  // Output: true
console.log(x > y);   // Output: true
console.log(x <= y);  // Output: false
```

### 3. Operadores Lógicos:
Operadores lógicos são utilizados para realizar operações lógicas em valores booleanos. Os principais operadores lógicos em JavaScript são:

- `&&`: E lógico (AND)
- `||`: Ou lógico (OR)
- `!`: Negação lógica (NOT)


```javascript
var a = true;
var b = false;
console.log(a && b);  // Output: false
console.log(a || b);  // Output: true
console.log(!a);      // Output: false
```

### 4. Operador typeof:
O operador `typeof` é utilizado para retornar o tipo de dado de uma expressão ou variável. Os tipos de dados possíveis retornados pelo operador `typeof` são:

- `"number"`: Número
- `"string"`: String
- `"boolean"`: Booleano
- `"object"`: Objeto (exceto null)
- `"function"`: Função
- `"undefined"`: Indefinido


```javascript
var num = 10;
var texto = "Olá";
var condicao = true;
var objeto = {};
var funcao = function() {};
var indefinido;
console.log(typeof num);       // Output: number
console.log(typeof texto);     // Output: string
console.log(typeof condicao);  // Output: boolean
console.log(typeof objeto);    // Output: object
console.log(typeof funcao);    // Output: function
console.log(typeof indefinido);// Output: undefined
```

# Exercícios

- Crie um objeto chamado 'pessoa' com as propriedades 'nome', 'idade' e 'cidade'.
Em seguida, imprima o nome e a idade da pessoa.

```javascript
var pessoa = {
    nome: "Maria",
    idade: 30,
    cidade: "São Paulo"
};

console.log("Nome:", pessoa.nome);
console.log("Idade:", pessoa.idade);
```


- Crie um array chamado 'cores' com as cores "vermelho", "azul" e "verde".
Em seguida, imprima a segunda cor do array.
```javascript
var cores = ["vermelho", "azul", "verde"];

console.log("Segunda cor:", cores[1]);
```

- Adicione a cor "amarelo" ao final do array 'cores' criado anteriormente.
Em seguida, remova a primeira cor do array.

```javascript
cores.push("amarelo");
cores.shift();

console.log(cores);
```

### Exercícios sobre Operadores Básicos:

**1. Aritméticos:**

Declare duas variáveis 'a' e 'b' com os valores 10 e 5, respectivamente.
Em seguida, imprima o resultado das operações de adição, subtração, multiplicação, divisão e módulo.

```javascript
var a = 10;
var b = 5;

console.log("Adição:", a + b);
console.log("Subtração:", a - b);
console.log("Multiplicação:", a * b);
console.log("Divisão:", a / b);
console.log("Módulo:", a % b);
```

**2. Comparação:**

Declare duas variáveis 'x' e 'y' com os valores 10 e 5, respectivamente.
Em seguida, imprima o resultado das operações de igualdade, diferença, maior que, menor que, maior ou igual a e menor ou igual.
```javascript
var x = 10;
var y = 5;

console.log("Igualdade:", x == y);
console.log("Diferença:", x != y);
console.log("Maior que:", x > y);
console.log("Menor que:", x < y);
console.log("Maior ou igual a:", x >= y);
console.log("Menor ou igual a:", x <= y);
```

**3. Lógicos:**

Declare duas variáveis booleanas 'p' e 'q' com os valores true e false, respectivamente.
Em seguida, imprima o resultado das operações lógicas AND, OR e NOT.

```javascript
var p = true;
var q = false;

console.log("AND:", p && q);
console.log("OR:", p || q);
console.log("NOT:", !p);
```

**4. typeof:**

Declare variáveis com diferentes tipos de dados (number, string, boolean, object, undefined) e imprima o tipo de cada uma.
```javascript
var num = 10;
var texto = "Olá";
var condicao = true;
var objeto = {};
var indefinido;

console.log("Tipo de num:", typeof num);
console.log("Tipo de texto:", typeof texto);
console.log("Tipo de condicao:", typeof condicao);
console.log("Tipo de objeto:", typeof objeto);
console.log("Tipo de indefinido:", typeof indefinido);
```




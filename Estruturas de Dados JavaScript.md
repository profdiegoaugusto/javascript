# Estruturas de Dados JavaScript

Criado em: May 1, 2024 8:01 AM
Tags: estruturas de dados, javascript

# Introdução

Estruturas de dados são maneiras organizadas de armazenar e gerenciar dados em um computador de forma eficiente. Elas fornecem métodos para organizar, acessar e manipular os dados de maneira que facilite a realização de operações específicas, como inserção, exclusão, busca e ordenação.

O JavaScript oferece várias estruturas de dados nativas que podem ser usadas para armazenar e manipular dados de forma eficiente. Algumas das estruturas de dados nativas do JavaScript incluem:

1. **Arranjos (Arrays):** Arrays em JavaScript são objetos que armazenam uma coleção ordenada de elementos, os quais podem ser de qualquer tipo de dado. Eles são acessados por meio de índices numéricos e têm métodos embutidos para adicionar, remover e manipular elementos.
2. **Objetos (Object):** Os objetos em JavaScript são coleções de pares chave-valor, onde cada chave é única e mapeada para um valor. Eles são muito flexíveis e podem ser usados para representar uma variedade de estruturas de dados, incluindo arrays associativos, dicionários e conjuntos.
3. **Mapas (Map):** Os mapas são coleções de pares chave-valor semelhantes a objetos, mas com algumas diferenças importantes. Em um mapa, as chaves podem ser de qualquer tipo de dado, não apenas strings ou símbolos como em objetos. Além disso, a ordem das chaves em um mapa é garantida, o que não é o caso dos objetos.
4. **Conjuntos (Set):** Conjuntos são coleções de valores únicos, o que significa que cada valor em um conjunto só pode ocorrer uma vez. Eles são úteis para verificar a existência de um elemento em uma coleção sem precisar se preocupar com duplicatas.

Essas estruturas de dados nativas do JavaScript são poderosas e versáteis, e são amplamente utilizadas no desenvolvimento de aplicativos da web e outras aplicações JavaScript. Dependendo das necessidades específicas do seu código, você pode escolher a estrutura de dados mais apropriada para manipular seus dados de maneira eficiente e eficaz.

# 1. Arranjos (Arrays)

Arrays em JavaScript são objetos especiais usados para armazenar múltiplos valores em uma única variável. Eles são uma coleção ordenada de elementos, onde cada elemento pode ser acessado por um índice. Os arrays em JavaScript podem conter valores de diferentes tipos de dados, como números, strings, objetos, funções e até mesmo outros arrays.

## 1.1. Criação de Arrays

Instanciando objetos do tipo lista usando a palavra-chave  `new`

```jsx
let listaVazia = new Array();           // Array vazio
let numeros = new Array(1, 2, 3, 4, 5); // Array com elementos
```

Criando listas de maneira implícita usando colchetes

```jsx
let listaVazia = [];                          // Array vazio
let numeros = [1, 2, 3, 4, 5];                // Array com elementos
let frutas = ["maçã", "banana", "laranja"];   // Array de strings

// Criando um array misto
let misto = [1, "Hello", true, { idade: 5 }];
```

## 1.2 Obter Tamanho da Lista

Para obter o número de elementos (tamanho, comprimento ou matematicamente o valor de n) em um array, você pode usar a propriedade **`length`**. Por exemplo:

```jsx
let numeros = [1, 2, 3, 4, 5];
console.log(numeros.length); // Saída: 5
```

## 1.3 Inserir Elementos na Lista

```jsx
let numeros = [1, 2, 3];
numeros[3] = 5;           // Adiciona 5 ao índice 3 do array

numeros.unshift(0);       // Adiciona 0 ao início do array
numeros.push(4);          // Adiciona 4 ao final do array

console.log(numeros);     // Saída: [0, 1, 2, 3, 5, 4]
```

## 1.4 Acessar Elementos da Lista

```jsx
let letras = ["a", "b", "c"];
console.log(letras[1]);           // Saída: "b"
console.log(letras.indexOf("b")); // Saída:  1
console.log(letras.indexOf("x")); // Saída:  -1, indicando elemento ausente
```

## 1.5 Iterar nos Elementos da Lista

```jsx
let numeros = [1, 2, 3, 4, 5];

// Usando um loop for para percorrer o array
for (let i = 0; i < numeros.length; i++) {
  console.log(numeros[i]);
}

// Usando o método foreach para percorrer o array
numeros.forEach((d, i) => {		
  console.log(i + " = " + d); // d é o elemento e i o índice
});
```

## 1.6 Atualizar Elementos da Lista

```jsx
let numeros = [1, 2, 3]; 
numeros[1] = 4;           // Atualiza o segundo elemento para 4
console.log(numeros);     // Saída: [1, 4, 3]
```

## 1.7 Excluir Elementos da Lista

```jsx
let numeros = [1, 2, 3, 4, 5];
numeros.pop();         // Remove o último elemento (5)
numeros.shift();       // Remove o primeiro elemento (1)
numeros.splice(1, 1);  // Remove um elemento no índice 1
console.log(numeros);  // Saída: [2, 3, 4]
```

## 1.8 Pesquisar Elementos da Lista

```jsx
let numeros = [1, 2, 3, 4, 5];

// Encontrar o primeiro número maior que 3
let resultado = numeros.find((d) => {
  return d > 3;
});

console.log(resultado); // Saída: 4
```

## 1.9 Filtrar Elementos da Lista

```jsx
let numeros = [1, 2, 3, 4, 5];

// Encontrar o primeiro número maior que 3
let resultado = numeros.filter((d) => {
  return d > 3;
});

console.log(resultado); // Saída: 4
```

## 1.10 Ordenar Elementos da Lista

```jsx
// Ordenação Crescente de Números
let numerosCrescente = [4, 2, 5, 1, 3];
numerosCrescente.sort((a, b) => a - b); // Função de comparação para ordem crescente
console.log("Números em Ordem Crescente:", numerosCrescente); // Saída: [1, 2, 3, 4, 5]

// Ordenação Decrescente de Números
let numerosDecrescente = [4, 2, 5, 1, 3];
numerosDecrescente.sort((a, b) => b - a); // Função de comparação para ordem decrescente
console.log("Números em Ordem Decrescente:", numerosDecrescente); // Saída: [5, 4, 3, 2, 1]

// Ordenação Crescente de Vogais
let vogaisCrescente = ['u', 'a', 'o', 'e', 'i'];
vogaisCrescente.sort(); // Ordenação de strings por padrão (ordem crescente)
console.log("Vogais em Ordem Crescente:", vogaisCrescente); // Saída: ['a', 'e', 'i', 'o', 'u']

// Ordenação Decrescente de Vogais
let vogaisDecrescente = ['u', 'a', 'o', 'e', 'i'];
vogaisDecrescente.sort().reverse(); // Ordenação de strings por padrão e depois inversão (ordem decrescente)
console.log("Vogais em Ordem Decrescente:", vogaisDecrescente); // Saída: ['u', 'o', 'i', 'e', 'a']
```

A expressão **`b - a`** é uma função de comparação usada como argumento para o método **`sort()`** em JavaScript. Quando usada dessa forma, essa função indica ao **`sort()`** como os elementos devem ser ordenados. Aqui está o que essa função de comparação faz:

- Se **`a`** é menor que **`b`**, a função retorna um número negativo. Isso indica que **`a`** deve ser classificado antes de **`b`**.
- Se **`a`** é maior que **`b`**, a função retorna um número positivo. Isso indica que **`b`** deve ser classificado antes de **`a`**.
- Se **`a`** é igual a **`b`**, a função retorna **`0`**. Nesse caso, não há necessidade de troca de posição.

Quando usamos **`b - a`**, estamos ordenando de forma decrescente. Isso porque, se **`b`** é maior que **`a`**, **`b - a`** será positivo, indicando que **`b`** deve ser classificado antes de **`a`**, o que resulta em uma ordenação decrescente.

Se quisermos uma ordenação crescente, usaríamos **`a - b`**, pois, nesse caso, se **`a`** é menor que **`b`**, **`a - b`** será negativo, indicando que **`a`** deve ser classificado antes de **`b`**, resultando em uma ordenação crescente.

## 1.11 Mapear Elementos da Lista

```jsx
let numeros = [1, 2, 3, 4, 5];

let numerosDobrados = numeros.map(function(numero) {
  return numero * 2;
});

console.log(numerosDobrados); // Saída: [2, 4, 6, 8, 10]
```

# 2. Objetos (Objects)

Em JavaScript, os objetos são estruturas de dados que permitem armazenar coleções de pares chave-valor. Cada chave (também chamada de propriedade) em um objeto é única e está associada a um valor. Os valores podem ser de qualquer tipo de dado, incluindo números, strings, booleanos, arrays, funções e até mesmo outros objetos.

## 2.1 Criação de Objetos

Instanciando objetos usando a palavra-chave  `new`

```jsx
let pessoa = new Object();

pessoa.nome = "João";
pessoa.idade = 30;
pessoa.cidade = "São Paulo";
```

Usando a notação de Objeto Literal

```jsx
let pessoa = {
  nome: "Ana",
  idade: 25,
  cidade: "São Paulo",
  casado: false,
  dataNascimento: new Date(1999, 5, 15), // Representa 15 de junho de 1999
  altura: 1.65,
  interesses: ["viajar", "ler", "cozinhar"]
};

console.log(pessoa);
```

## 2.2 Acessar Chaves e Valores

O método **`Object.keys()`** retorna um array contendo os nomes das propriedades enumeráveis de um objeto.

```jsx
let pessoa = {
  nome: "João",
  idade: 30,
  cidade: "São Paulo"
};

let propriedades = Object.keys(pessoa);
console.log(propriedades); // Saída: ["nome", "idade", "cidade"]

for (let propriedade in pessoa) {
  console.log(propriedade); // Saída: "nome", "idade", "cidade"
}
```

Para obter os valores das propriedades de um objeto em JavaScript, você pode usar o método **`Object.values()`**

```jsx
let pessoa = {
  nome: "João",
  idade: 30,
  cidade: "São Paulo"
};

let valores = Object.values(pessoa);
console.log(valores); // Saída: ["João", 30, "São Paulo"]
```

## 2.3 Obter Valores dos Objetos

```jsx
console.log(pessoa.nome) ;     // Saída: "João"
console.log(pessoa["idade"]);  // Saída: 30
```

## 2.4 Atualizar Valores dos Objetos

```jsx
pessoa.idade = 31;
pessoa["idade"] = 31
```

## 2.5 Excluir Propriedade de um Objeto

```jsx
delete pessoa.cidade;
```

## 2.6 Iterar pelas Propriedades dos Objetos

O loop **`for...in`** itera sobre todas as propriedades enumeráveis de um objeto, permitindo acessar os nomes das propriedades.

```jsx
let pessoa = {
  nome: "João",
  idade: 30,
  cidade: "São Paulo"
};

for (let propriedade in pessoa) {
  console.log(propriedade); // Saída: "nome", "idade", "cidade"
}

for (let propriedade in pessoa) {
  let valor = pessoa[propriedade];
  console.log(valor); // Saída: "João", 30, "São Paulo"
}
```

## 2.7 Listas de Objetos

```jsx
let produtos = [
  { nome: 'Camiseta', preco: 20, emEstoque: true },
  { nome: 'Calça', preco: 30, emEstoque: false },
  { nome: 'Sapato', preco: 50, emEstoque: true },
  { nome: 'Boné', preco: 10, emEstoque: false },
  { nome: 'Óculos', preco: 25, emEstoque: true }
];

let produtosEmEstoque = produtos.filter((produto) => {
  return produto.emEstoque == true;
});

console.log(produtosEmEstoque);
```

# 3. Mapas (Maps)

Mapas (Map) em JavaScript são uma estrutura de dados que permite armazenar pares chave-valor, onde cada chave pode ser de qualquer tipo de dado, e cada valor associado pode ser de qualquer tipo de dado também. Ao contrário dos objetos, as chaves de um Map podem ser objetos e não apenas strings ou símbolos. 

Mapas são úteis em situações onde você precisa associar valores a chaves únicas e acessar esses valores posteriormente de forma eficiente. Aqui estão algumas situações comuns em que você pode usar Mapas:

1. **Associação de dados complexos**: Quando você precisa associar dados mais complexos, como objetos ou funções, a chaves específicas.
2. **Preservação da ordem de inserção**: Os Mapas preservam a ordem de inserção dos elementos, o que pode ser útil em situações onde a ordem é importante.
3. **Chaves de qualquer tipo**: Ao contrário dos objetos em JavaScript, as chaves de um Map podem ser de qualquer tipo de dado, incluindo objetos, funções e valores primitivos.
4. **Evitar sobrescrita de propriedades do protótipo**: Como os Mapas são objetos independentes, você pode usá-los para armazenar dados sem o risco de sobrescrever propriedades do protótipo.

## 3.1 Criação de Maps

```jsx
let mapa = new Map();
```

## 3.2 Obter Quantidade de Elementos

```jsx
console.log(mapa.size); // Saída: 0 (o mapa está vazio)
```

## 3.3 Inserir Elementos

```jsx
mapa.set("chave", "valor");
```

## 3.4 Obter Elementos

```jsx
console.log(mapa.get("chave")); // Saída: "valor"
```

## 3.5 Atualizar Elementos

```jsx
mapa.set("chave", "novo valor");
```

## 3.6 Excluir Elementos

```jsx
mapa.delete("chave");
```

## 3.7 Iterar pelos Elementos do Map

Iterando nos Elementos de um Map usando forEach()

```jsx
let mapa = new Map();
mapa.set("a", 1);
mapa.set("b", 2);
mapa.set("c", 3);

mapa.forEach(function(valor, chave) {
  console.log("Chave:", chave, "Valor:", valor);
});
```

Usando for ….of

```jsx
let mapa = new Map();
mapa.set("a", 1);
mapa.set("b", 2);
mapa.set("c", 3);

for (let [chave, valor] of mapa) {
  console.log("Chave:", chave, "Valor:", valor);
}
```

Neste exemplo, usamos a estrutura **`for...of`** para iterar sobre os elementos do Map. Usamos a sintaxe **`[chave, valor]`** para desestruturar cada par chave-valor à medida que iteramos. Dentro do loop, imprimimos a chave e o valor de cada elemento.

## 3.8 Exemplos

```jsx
let mapa = new Map();

mapa.set("nome", "Ana");
mapa.set("idade", 30);
mapa.set("cidade", "São Paulo");

console.log(mapa.get("nome")); // Saída: "Ana"
console.log(mapa.size); // Saída: 3 (três pares chave-valor no mapa)

mapa.delete("idade"); // Removendo a chave "idade"

console.log(mapa.has("idade")); // Saída: false (a chave "idade" foi removida)
```

```jsx
// Criando objetos aluno com informações adicionais
let aluno1 = { id: 1, nome: "Ana", sobrenome: "Silva", curso: "Engenharia de Software" };
let aluno2 = { id: 2, nome: "João", sobrenome: "Santos", curso: "Engenharia de Software" };
let aluno3 = { id: 3, nome: "Maria", sobrenome: "Souza", curso: "Engenharia de Software" };

let notas = new Map();

// Associando cada aluno com sua nota no Map
notas.set(aluno1, 8.5);
notas.set(aluno2, 7.0);
notas.set(aluno3, 9.2);

// Obtendo e imprimindo as notas de cada aluno
console.log("Nota de " + aluno1.nome + " " + aluno1.sobrenome + ": " + notas.get(aluno1));
console.log("Nota de " + aluno2.nome + " " + aluno2.sobrenome + ": " + notas.get(aluno2));
console.log("Nota de " + aluno3.nome + " " + aluno3.sobrenome + ": " + notas.get(aluno3));
```

# 4. Conjuntos (Sets)

Sets são coleções de valores únicos em JavaScript, o que significa que cada valor pode ocorrer apenas uma vez em um conjunto. Sets são úteis quando você precisa armazenar uma lista de valores únicos e não precisa se preocupar com a ordem dos elementos.

Sets em JavaScript são úteis em situações onde você precisa armazenar uma coleção de valores únicos, sem repetições. Aqui estão algumas situações comuns em que você pode usar Sets:

1. **Remoção de duplicatas**: Se você tem uma lista de valores e precisa garantir que cada valor apareça apenas uma vez, um Set é uma escolha ideal.
2. **Verificação de existência de valores**: Você pode usar um Set para verificar rapidamente se um determinado valor está presente na coleção ou não.
3. **Operações de conjunto**: Sets são úteis para realizar operações de conjunto, como união, interseção e diferença entre conjuntos.

## 4.1 Criação e Sets

```jsx
let conjuntoVazio = new Set();
let conjunto = new Set([1, 2, 3, 4, 5]);
```

## 4.2 Obter Quantidade de Elementos

```jsx
console.log(conjuntoNumerico.size); // Saída: 5 (quantidade de elementos no conjunto)
```

## 4.3 Adicionar Elementos

```jsx
conjunto.add(6);
```

## 4.4 Obter Elementos

Os Sets não têm métodos específicos para ler elementos individuais, mas você pode verificar se um elemento está presente usando o método **`has()`**.

```jsx
console.log(conjunto.has(6)); // Saída: true (o elemento 6 está presente no conjunto)
```

## 4.5 Atualizar Elementos

Os Sets **não permitem atualizar elementos individualmente**, mas você pode adicionar novamente o novo valor usando o método **`add()`**, que substituirá o valor anterior se já estiver presente.

```jsx
conjunto.add(6); // Substitui o valor existente por 6
```

## 4.6 Excluir Elementos

```jsx
conjunto.delete(6);
```

## 4.7 Iterar nos Elementos

```jsx
let conjuntoNumerico = new Set([1, 2, 3, 4, 5]);

conjuntoNumerico.forEach((valor) => {
  console.log(valor);
});
```

```jsx
let conjunto = new Set();

// Adicionando pares de chave e valor ao conjunto
conjunto.add({ chave: "a", valor: 1 });
conjunto.add({ chave: "b", valor: 2 });
conjunto.add({ chave: "c", valor: 3 });

// Percorrendo Chaves
for (let elemento of conjunto) {
  console.log(elemento);
}

// Percorrendo Chaves
for (let chave of conjunto.keys()) {
  console.log(chave);
}

// Percorrendo Valores
for (let valor of conjunto.values()) {
  console.log(valor);
}

// Utilizando o Método entries() 
for (let [valor, chave] of conjunto.entries()) {
  console.log("Valor:", valor, "Chave:", chave);
}
```

### 4.7.1 **Convertendo um Set em um Array e Iterando sobre ele**

Você também pode converter um Set em um array usando o operador spread (**`...`**) ou o construtor **`Array.from()`**, e depois iterar sobre os elementos do array usando métodos de iteração de arrays como **`forEach()`** ou **`map()`**. Exemplo com spread operator:

```jsx
let conjunto = new Set([1, 2, 3, 4, 5]);
let array = [...conjunto];

array.forEach(function(valor) {
  console.log(valor);
});
```

Exemplo com Array.from():

```jsx

let conjunto = new Set([1, 2, 3, 4, 5]);
let array = Array.from(conjunto);

array.forEach(function(valor) {
  console.log(valor);
});
```

## 4.8 Operações de Conjuntos

```jsx
// Função para calcular a união entre dois conjuntos
function calcularUniao(conjuntoA, conjuntoB) {
    let uniao = new Set(conjuntoA);
    for (let elemento of conjuntoB) {
        uniao.add(elemento);
    }
    return uniao;
}

// Função para calcular a interseção entre dois conjuntos
function calcularIntersecao(conjuntoA, conjuntoB) {
    let intersecao = new Set();
    for (let elemento of conjuntoA) {
        if (conjuntoB.has(elemento)) {
            intersecao.add(elemento);
        }
    }
    return intersecao;
}

// Função para calcular a diferença entre dois conjuntos (A - B)
function calcularDiferenca(conjuntoA, conjuntoB) {
    let diferenca = new Set();
    for (let elemento of conjuntoA) {
        if (!conjuntoB.has(elemento)) {
            diferenca.add(elemento);
        }
    }
    return diferenca;
}

// Função para calcular a diferença simétrica entre dois conjuntos
function calcularDiferencaSimetrica(conjuntoA, conjuntoB) {
    let diferencaSimetrica = new Set();
    for (let elemento of conjuntoA) {
        if (!conjuntoB.has(elemento)) {
            diferencaSimetrica.add(elemento);
        }
    }
    for (let elemento of conjuntoB) {
        if (!conjuntoA.has(elemento)) {
            diferencaSimetrica.add(elemento);
        }
    }
    return diferencaSimetrica;
}

// Criando os conjuntos
let conjuntoA = new Set([1, 2, 3, 4, 5]);
let conjuntoB = new Set([4, 5, 6, 7, 8]);

// Calculando e exibindo os resultados
console.log("Conjunto A:", conjuntoA);
console.log("Conjunto B:", conjuntoB);
console.log("União:", calcularUniao(conjuntoA, conjuntoB));
console.log("Interseção:", calcularIntersecao(conjuntoA, conjuntoB));
console.log("Diferença (A - B):", calcularDiferenca(conjuntoA, conjuntoB));
console.log("Diferença Simétrica:", calcularDiferencaSimetrica(conjuntoA, conjuntoB));
```
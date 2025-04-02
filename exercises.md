# Exercícios de Revisão - M1

**1) Considere o seguinte código. Qual é o valor armazenado na variável numeros?**

```js
const array = [1, 2, 3, 4, 5, 6];
const numeros = array.filter(num => num % 2 === 0);
```

a) [1, 3, 5]

b) [1, 2, 3]

c) [2, 3, 4]

d) [2, 4, 6]

<br>

**2) Qual será a saída do código?**

```js
let dia = 3;
switch dia) {
  case 1:
    console.log("Domingo");
    break;
  case 2:
    console.log("Segunda-feira");
    break;
  default:
    console.log("Outro dia");
}
```

a) "Domingo"

b) "Segunda-feira"

c) "Outro dia"

d) Erro, pois não há case para o valor 3.

<br>

**3) Considerando as comparações `a == b` e `a === b`, qual das alternativas descreve corretamente o resultado de cada comparação?**

```js
let a = 10;
let b = "10";
```

a) a == b retorna false e a === b retorna false.

b) a == b retorna true e a === b retorna true.

c) a == b retorna true e a === b retorna false.

d) a == b retorna false e a === b retorna true.

<br>

**4) Você está desenvolvendo um recurso para um aplicativo de gerenciamento de listas de convidados para eventos. O aplicativo deve permitir que o organizador do evento identifique rapidamente se existe um convidado que atenda a critérios específicos dentro de uma lista de convidados. Cada convidado é representado por um objeto com as propriedades nome, idade e confirmado (um booleano que indica se o convidado confirmou sua assistência ao evento). O objetivo é encontrar o primeiro convidado que:**

- **Confirmou sua participação ao evento.**

- **Tem 30 anos ou mais.**

**Você decide criar uma função encontrarConvidado Especial que recebe a lista de convidados como argumento e retorna o nome do convidado que satisfaz as condições acima, ou null se nenhum convidado satisfizer esses critérios.**

**Considere o array de convidados da imagem abaixo como exemplo.**

**Qual das seguintes implementações da função encontrarConvidadoEspecial está correta e efetivamente retorna o nome do convidado que satisfaz as condições especificadas?**

**Observe as alternativas na imagem abaixo e assinale a alternativa correta.**

```javascript
let convidadas = [
    { nome: "Maria", idade: 15, confirmado: true },
    { nome: "Joana", idade: 25, confirmado: false },
    { nome: "Fabiola", idade: 12, confirmado: true },
    { nome: "Luiza", idade: 18, confirmado: true }
];
```

a) 
```js
function encontrarConvidadaEspecial (convidados){
    convidados.forEach(convidado => {
        if convidado.confirmado && convidado.idade >= 30 {
            return convidado.nome;
        };
    });
    return null;
}
```

b) 
```js
function encontrarConvidadaEspecial (convidados){
    return convidados
        .filter(convidado => convidado.confirmado && convidado.idade >= 18)
        .map(convidado => convidado.nome)[0] || null;
}
```

c) 
```js
function encontrarConvidadaEspecial (convidados){
    for (let i = 0; i < convidados.length; i++) {
        if (convidados[i].confirmado && convidados[i].idade >= 30) {
            return convidados[i].nome;
        };
    };
    return null
}
```

d) 
```js
function encontrarConvidadaEspecial (convidados){
    convidados.forEach(convidado => {
        if (convidado.confirmado && convidado.idade >=30) {
            return convidado.nome;
        };
    });
    return null
}
```

<br>

**5) Qual é o valor armazenado em x e por que ele ocorre dessa forma?**

```js
let x = "10" + 5;
```

a) 15, pois os valores são somados numericamente.

b) "105", pois o número é convertido em string e ocorre cocatenação.

c) 105, por conta da multiplicação implícita.

d) "15", pois o JavaScript soma os valores como strings.

<br>

**6) Por que a tentativa de alterar o valor de PI gera um erro?**

```js
const PI = 3.14;
PI = 3.1415; 
```

a) Porque PI foi declarado com const e seu valor é imutável.

b) Porque PI é uma variável global.

c) Porque o valor 3.14 não pode ser alterado em JavaScript.

d) Porque constantes só aceitam valores inteiros.

<br>

**7) Considere o código abaixo. Qual será o valor impresso no console?**

```js
const numeros = [1, 2, 3, 4, 5];
let soma = 0;
for (let i = 0; i < numeros.length; i++) {
  soma += numeros[i];
}
console.log(soma);
```

a) 10

b) 15

c) 12

d) 20

<br>

**8) Você está criando uma função que analisa a temperatura para indicar o estado da água. A função deve retornar:**

- **`"sólido"` se a temperatura for menor que 0,**
- **`"líquido"` se a temperatura estiver entre 0 (inclusive) e 100 (exclusive),**
- **`"gasoso"` se a temperatura for igual ou maior que 100.**

**Assinale a alternativa que representa corretamente essa função:**

a)

```js
function estadoDaAgua(temperatura) {
  if (temperatura < 0) return "sólido";
  if (temperatura >= 0 && temperatura < 100) return "líquido";
  return "gasoso";
}
```

b)

```js
function estadoDaAgua(temperatura) {
  if (temperatura > 100) return "gasoso";
  else if (temperatura > 0) return "líquido";
  else return "sólido";
}
```

c)

```js
function estadoDaAgua(temperatura) {
  switch(temperatura) {
    case temperatura < 0: return "sólido";
    case temperatura < 100: return "líquido";
    default: return "gasoso";
  }
}
```

d)

```js
function estadoDaAgua(temperatura) {
  if (temperatura == 0) return "sólido";
  if (temperatura == 100) return "gasoso";
  return "líquido";
}
```

<br>

**9) Qual será a saída do código abaixo?**

```javascript
const conta = (x) => x * 2;
console.logconta(5));
```  

a) `5`  

b) `10` 

c) `x * 2`  

d) `Erro`  

<br>

**10) Analise o código a seguir. Qual será a saída impressa no console?**

```js
const letras = ['a', 'b', 'c', 'd'];
let resultado = '';
for (let i = 0; i < letras.length; i++) {
  if (letras[i] === 'c') {
    break;
  }
  resultado += letras[i];
}
console.log(resultado);
```

a) "abcd"

b) "abc"

c) "a"

d) "ab"

<br>

**11) Qual será a saída do código abaixo?**

```js
function expoa, b) {
  let expo = a ** b
}

console.log(expo(2, 3))
```

a) Retorna `undefined`

b) Retorna `4`  

c) Retorna `8`  

d) Causa um erro  

<br>

**12) Analise o seguinte código. Qual é o valor armazenado na variável maximo após a execução do laço?**

```js
const valores = [3, 7, 2, 9, 5];
let maximo = valores[0];
for (let i = 1; i < valores.length; i++) {
  if (valores[i] > maximo) {
    maximo = valores[i];
  }
}
console.log(maximo);
```

a) 7

b) 5

c) 3

d) 9 

<br>

**13) Qual é o valor padrão de uma variável que foi declarada, mas não inicializada?**

```js
let x;
console.log(x);
```

a) null

b) undefined.

c) 0

d) ""

<br>

**14) Em um jogo desenvolvido com Phaser, você precisa mover um sprite de um ponto inicial para um ponto final. Para isso, você precisa calcular a trajetória do sprite. A trajetória do sprite pode ser representada por uma linha reta. A posição inicial do sprite é representada pelo vetor "origem" e a posição final do sprite é representada pelo vetor "destino".**

**Considerando o código JavaScript abaixo, qual alternativa implementa corretamente a função "calcular Trajetoria", que calcula a trajetória do sprite?**

```js
function calcularTrajetoria(origem, destino) {
  // aqui você deve implementar a função escolhendo uma das alternativas
}

const origem = new Phaser.Math.Vector2(100, 100);
const destino = new Phaser.Math.Vector2(200, 200);
const trajetoria = calcularTrajetoria(origem, destino);
```

**Observe as alternativas na imagem abaixo e assinale a alternativa correta.**

a)
```js
function calcularTrajetoria(origem, destino) {
  const trajetoria = destino.subtract(origem);
  return trajetoria
}
```

b)
```js
function calcularTrajetoria(origem, destino) {
  const trajetoria = destino.clone();
  return trajetoria
}
```

c) 
```js
function calcularTrajetoria(origem, destino) {
  const trajetoria = origem.add(destino);
  return trajetoria
}
```

d) 
```js
function calcularTrajetoria(origem, destino) {
  const trajetoria = origem.multiply(destino);
  return trajetoria
}
```

<br>

**15) O paradigma de programação orientada a objetos envolve a identificação e abstração de entidades, de acordo com o escopo de um sistema. Essas entidades formam o vocabulário do sistema. Por exemplo, se estamos desenvolvendo um sistema para um consultório médico, entidades como prontuário, paciente, médico, etc., fazem parte do vocabulário e serão implementadas pelas classes.**

**Considerando os conceitos e funcionalidades da programação orientada a objetos (POO) em JavaScript, analise as afirmativas a seguir:**

**I. O constructor é um método especial de uma dasse em JavaScript, utilizado para criar e inicializar um objeto criado a partir da classe.**

**II. A palavra-chave extends é utilizada para criar uma classe mãe, que herda todas as propriedades e métodos da classe filha, induindo métodos estáticos, facilitando a reutilização de código.**

**III. Ao utilizar this dentro de um método de uma classe, ele se refere ao objeto que invocou o método, permitindo acessar propriedades e métodos do objeto em questão.**

**IV. Uma instância de uma classe pode ser criada sem a necessidade de invocar o constructor explicitamente, utilizando a palavra-chave new seguida pelo nome da classe.**

**É correto APENAS o que se afirma em:**

a) I e III são verdadeiras.

b) I, II e III são verdadeiras.

c) II, III e IV são verdadeiras.

d) I, III e IV são verdadeiras.

<br>

**16) A linguagem JavaScript oferece diversas formas de iterar sobre arrays e realizar operações com seus elementos, incluindo o uso de laços e condicionais. Estas estruturas de controle permitem não apenas percorrer cada elemento da lista, mas também tomar decisões baseadas em cada um desses elementos, tornando a manipulação de dados flexivel e poderosa.**

**Qual será a saída do console após a execução deste trecho de código?**

```js
let numeros = [2, 3, 5, 7, 11, 13, 17, 19, 23, 29];
let selecioandos = [];

for (let i = 0; i < numeros.length; i++) {
  if (numeros[i] % 3 === 0 || numeros[i] % 5 === 0) {
    selecionados.push(numeros[i]);
  }
}
```

a) [3, 5, 15, 30]

b) [3, 5]

c) [3, 5, 15, 25]

d) [3, 5, 15]

<br>

**17) Você está desenvolvendo um sistema de gestão de conteúdo digital utilizando JavaScript. Neste sistema, há uma classe ConteudoDigital que serve como base, contendo atributos como titulo e criador. Além disso, existe uma classe derivada Video que estende ConteudoDigital adicionando um novo atributo chamado duracao, Ambas as classes possuem um método info() que retorna uma string com informações sobre o conteúdo.**

**Observe o código abaixo.**

**Considerando a estrutura das classes ConteudoDigital e Video no sistema de gestão de conteúdo digital, qual dos seguintes códigos cria corretamente uma instância de `Video` e chama o método `info()` para exibir suas informações?**

**Observe as alternativas na imagem abaixo e assinale a correta.**

```js
class ConteudoDigital {
  constructor(titulo, criador) {
    this.titulo = titulo;
    this.criador = criador;
  }

  info() {
    return `Título: ${this.titulo}, Criado por: ${this.criador}`;
  }
}

class Video extends ConteudoDigital {
  constructor(titulo, criador, duracao) {
    super(titulo, criador);
    this.duracao = duracao;
  }

  info() {
    return `${super.info()}, Duração: ${this.duracao} minutos.`
  }
}
```

a)
```js
let meuVideo = new Video("JS1", "Inteli", 30);
console.log(meuVideo.info())
```

b) 
```js
let meuVideo = new ConteudoDigital("JS1", "Inteli", 30);
console.log(meuVideo.info())
```

c) 
```js
let meuVideo = new Video("JS1", 30);
console.log(meuVideo.info())
```

d) 
```js
let meuVideo = new Video();
console.log(meuVideo.info())
```
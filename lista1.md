# Instruções
- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 8 questões objetivas assinalando a alternativa correta e **justificando sua resposta.**
- Resolva as 2 questões dissertativas escrevendo no próprio arquivo .md
- Lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com o uso de ChatGPT (e similares), pois entregar algo só para ganhar nota não fará você aprender. Não seja dependente da máquina!
- Ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas
**1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.**
```javascript
console.log(x);
var x = 5;
console.log(y);
let y = 10;
```
a) A saída será undefined seguido de erro 

b) A saída será 5 seguido de 10

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log

alternativa correta (A)

explicacao 
- A variável x existe porque foi declarada com var mas ainda não tem um valor na hora que voce tenta imprimir e á y foi declarada com let e esse tipo de variável não pode ser acessado antes da sua definicao

**2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.**

```javascript
function soma(a, b) {
    if (a || b === 0) {
        return "Erro: número inválido";
    }
    return a + b;
}
console.log(soma(2, 0));
```

a) Substituir if (a || b === 0) por if (a === 0 || b === 0)

b) Substituir if (a || b === 0) por if (a === 0 && b === 0)

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0)

alternativa (A)

explicacao
- A expressão original não verifica corretamente se a ou b são 0

______
**3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
function calcularPreco(tipo) {
    let preco;

    switch(tipo) {
        case "eletrônico":
            preco = 1000;
        case "vestuário":
            preco = 200;
            break;
        case "alimento":
            preco = 50;
            break;
        default:
            preco = 0;
    }

    return preco;
}

console.log(calcularPreco("eletrônico"));
```

a) O código imprime 1000.

b) O código imprime 200.

c) O código imprime 50.

d) O código gera um erro.

alternativa (B)

explicacao
- O switch não tem break após o primeiro caso, então continua executando o próximo sobrescrevendo o valor para 200

______
**4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
let numeros = [1, 2, 3, 4, 5];

let resultado = numeros.map(x => x * 2).filter(x => x > 5).reduce((a, b) => a + b, 0);

console.log(resultado);
```
a) 0

b) 6

c) 18

d) 24

alternativa (d)

Multiplica os números por 2- 2,4,6,8,10

Filtra os números maiores que 5-  6,8,10

Soma tudo: 6 + 8 + 10 = 24
______
**5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.**

```javascript
let lista = ["banana", "maçã", "uva", "laranja"];
lista.splice(1, 2, "abacaxi", "manga");
console.log(lista);
```

a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

c) ["banana", "abacaxi", "manga", "laranja"]

d) ["banana", "maçã", "uva", "abacaxi", "manga"]

alternativa (c)

explicacao
O splice remove dois elementos e insere dois novos no lugar mudando a lista.
______
**6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta**

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.  
II. Em JavaScript, a herança é implementada através da palavra-chave `extends`.


a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.

b) As duas afirmações são verdadeiras, mas a segunda não justifica a primeira.

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.

alternativa (a)

Herança é usada para compartilhar código entre classes e o extends permite que isso aconteça em JavaScript.
______
**7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.**

```javascript
class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

class Funcionario extends Pessoa {
  constructor(nome, idade, salario) {
    super(nome, idade);
    this.salario = salario;
  }

  apresentar() {
    super.apresentar();
    console.log(`Meu salário é R$ ${this.salario}.`);
  }
}
```


I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.  
II) O método `apresentar()` da classe Funcionario sobrepõe o método `apresentar()` da classe Pessoa, mas chama o método da classe pai usando `super`.  
III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

a) I e II são verdadeiras.

b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.

alternativa (a)

A classe Funcionario herda da classe Pessoa e sobrescreve o método apresentar() usando super para chamar o método da classe pai

______

**8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.**

**Asserção:** O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.  
**Razão:** Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

b) A asserção é verdadeira e a razão é falsa.

c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção.

alternativa (b)

Polimorfismo é um conceito correto mas a razão que fala sobre sobrecarga de métodos não se aplica em JavaScript que não suporta sobrecarga da mesma maneira.
______

# Questões dissertativas
9) O seguinte código deve retornar a soma do dobro dos números de um array, mas contém erros. Identifique os problema e corrija o código para que funcione corretamente. Adicione comentários ao código explicado sua solução para cada problema.

```javascript
function somaArray(numeros) {

    for (i = 0; i < numeros.size; i++) {
        soma = 2*numeros[i];
    }
    return soma;
}
console.log(somaArray([1, 2, 3, 4]));
```
**resposta**
```javascript
function somaArray(numeros) {

    // Faltou a variável ser criada
    var soma = 0; 

    // .size não existe, o certo é .length
    for (i = 0; i < numeros.length; i++) {
        soma += 2*numeros[i]; // faltou acumular a soma
    }
    return soma;
}
console.log(somaArray([1, 2, 3, 4]));
```

______
10) Crie um exemplo prático no qual você tenha duas classes:

- Uma classe `Produto` com atributos `nome` e `preco`, e um método `calcularDesconto()` que aplica um desconto fixo de 10% no preço do produto.
- Uma classe `Livro` que herda de `Produto` e modifica o método `calcularDesconto()`, aplicando um desconto de 20% no preço dos livros.

Explique como funciona a herança nesse contexto e como você implementaria a modificação do método na classe `Livro`.

**Resposta**

```javascript
// Classe Produto
class Produto {
    constructor(nome, preco) {
      this.nome = nome;
      this.preco = preco;
    }
  
    // Método que calcula o desconto de 10%
    calcularDesconto() {
      const desconto = 0.10;  // 10% de desconto
      this.preco -= this.preco * desconto;
    }
  }
  
  // Classe Livro que herda de Produto
  class Livro extends Produto {
    constructor(nome, preco, autor) {
      // Chama o construtor da classe pai
      super(nome, preco);
      this.autor = autor;
    }
  
    // Sobrescreve o método calcularDesconto para aplicar 20% de desconto
    calcularDesconto() {
      const desconto = 0.20;  // 20% de desconto para livros
      this.preco -= this.preco * desconto;
    }
  }
  
  // Exemplo de uso
  
  const produto = new Produto("Camiseta", 100);
  console.log(`Preço original do produto: R$ ${produto.preco}`);
  produto.calcularDesconto();
  console.log(`Preço após desconto de 10%: R$ ${produto.preco}`);
  
  const livro = new Livro("Shakespeare", 150, "John Doe");
  console.log(`Preço original do livro: R$ ${livro.preco}`);
  livro.calcularDesconto();
  console.log(`Preço após desconto de 20%: R$ ${livro.preco}`);
```

**Explicação**
-  A herança em meu código funciona desse jeito pois uma classe pode herdar as propriedades e métodos de outra atraves do extends. No exemplo, a classe Livro herda de Produto puxando os atributos nome e preco e o método calcularDesconto() da classe Produto. Porém, a classe Livro pode modificar esse método para que ele tenha um comportamento diferente, igual eu fiz com o calculardesconto como foi solicitado. Isso é feito sobrescrevendo o método calcularDesconto() na classe Livro, o que seria um ajuste da lógica conforme foi pedido.

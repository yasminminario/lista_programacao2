# Questões objetivas

**1)** Considere o seguinte código JavaScript:

```javascript
//EX01
let x = 17
let y = 5
let z = 8

resultadoBooleano =  (x < y) && (z > x) || (x - y > z)
console.log(resultadoBooleano)

const listaDeNumeros = [1, 2, 3, 4, 5];
let soma = 0;

for (let i = 0; i < listaDeNumeros.length; i++) {
  soma += listaDeNumeros[i];
}

console.log("A soma dos números é:", soma);

```
Qual das seguintes alternativas melhor descreve o que o código faz?

A) O código avalia a expressão booleana, imprime o resultado `false`, calcula a soma dos números de 1 a 5 e imprime o resultado no console.

**B) O código avalia a expressão booleana, imprime o resultado `true`, calcula a soma dos números de 1 a 5 e imprime o resultado no console.** (resposta certa)

C) O código avalia a expressão booleana, imprime o resultado `true` e verifica se o número 5 está presente na lista de números.

D) O código avalia a expressão booleana, imprime o resultado `false` e ordena a lista de números em ordem crescente.


______

**2)** Analise as funções calcularOrcamento() e calcularOrcamento2(). Num cenário em que a lista gastos fosse incializada como var gastos = [3600, 950, 620, 38] em ambas funções.

```javascript
//Versão 1 da função que calcula orçamento
function calculaOrcamento(){

    var gastos = [1800, 950, 620, 38];
    var totalGastos = gastos[0];
    var salario = 3500;
    var saldo = 0; 
    var statusSaldo =  'positivo';
    var i = 1;

    do{
        totalGastos += gastos[i];
        i++;
    } while(salario >= totalGastos && i<gastos.length)
    
    saldo = salario - totalGastos;

    if (saldo < 0 ){
        statusSaldo = 'negativo';
    } 
    console.log (`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
```

```javascript
//Versão 2 da função que calcula orçamento
function calculaOrcamento2(){

    var gastos = [1800, 950, 620, 38];
    var totalGastos = gastos[0];
    var salario = 3500;
    var statusSaldo =  'positivo';
    var saldo = 0;
    var i = 1;

    while(salario >= totalGastos && i<gastos.length){
        totalGastos += gastos[i];
        i++;
    }

    saldo = salario - totalGastos;
    if (saldo < 0 ){
        statusSaldo = 'negativo';
    } 
    console.log (`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
```

Escolha a opção que responde corretamente qual seria a saída após a execução de cada função:

A) As funções calcularOrcamento() e calcularOrcamento2() teriam a mesma saída: 'Seu saldo é negativo de -1050.'

**B) A saída de calcularOrcamento() seria: 'Seu saldo é negativo de -1050.' e a de calcularOrcamento2() seria: 'Seu saldo é negativo de -100.'** (resposta certa)

C) A saída de calcularOrcamento() seria: 'Seu saldo é negativo de -100.' e a de calcularOrcamento2() seria: 'Seu saldo é negativo de -1050.'

D) As funções calcularOrcamento() e calcularOrcamento2() teriam a mesma saída: 'Seu saldo é negativo de -100.'

______

**3)** Considere o seguinte trecho de código em JavaScript:
```javascript
//EX03
const numero = 10;

if (numero % 2 === 0) {
  console.log("O número é par!");
} else if (numero % 3 === 0) {
  console.log("O número é divisível por 3!");
} else {
  console.log("O número é ímpar e não é divisível por 3!");
}
```

 Qual das seguintes alternativas é a descrição mais precisa do que o código faz?


A) O código verifica se o número é divisível por 3 e, se for, exibe a mensagem "O número é divisível por 3!".

B) O código verifica se o número é par ou ímpar. Se for par, exibe a mensagem "O número é par!". Se for ímpar, exibe a mensagem "O número é ímpar!".

C) O código verifica se o número é par, ímpar ou divisível por 3. Se for par, exibe a mensagem "O número é par!". Se for divisível por 3, exibe a mensagem "O número é divisível por 3!". Se for ímpar, exibe a mensagem "O número é ímpar e não é divisível por 3!".

**D) O código verifica se o número é par, se é divisível por 3 ou se é ímpar. Se for par, exibe a mensagem "O número é par!". Se for divisível por 3 (e não for par), exibe a mensagem "O número é divisível por 3!". Se for ímpar (e não for divisível por 3), exibe a mensagem "O número é ímpar e não é divisível por 3!".** (resposta certa)


______

**4)** Qual será o resultado impresso no console após a execução desse código?
```javascript
//EX04
var saldo = 1000;
var limiteCredito = 500;
var valorCompras = [200, 800, 300, 400, 600];

for (var i = 0; i < valorCompras.length; i++) {
    var valorCompra = valorCompras[i];

    if (valorCompra <= saldo) {
        console.log("Compra " + (i+1) + " aprovada. Saldo restante: " + (saldo - valorCompra));
        saldo -= valorCompra;
    } else if (valorCompra <= saldo + limiteCredito) {
        console.log("Compra " + (i+1) + " aprovada com limite de crédito. Saldo restante: " + ((saldo + limiteCredito) - valorCompra));
        saldo = 0;
        limiteCredito -= (valorCompra - saldo);
    } else {
        console.log("Compra " + (i+1) + " negada. Saldo insuficiente e limite de crédito excedido.");
    }
}
```

Escolha a opção que responde corretamente:

A)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 400

Compra 4 aprovada com limite de crédito. Saldo restante: 0

Compra 5 aprovada. Saldo restante: -200


B)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 200

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.

Compra 5 negada. Saldo insuficiente e limite de crédito excedido.


C)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 400

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.


**D)**

**Compra 1 aprovada. Saldo restante: 800**

**Compra 2 aprovada. Saldo restante: 0**

**Compra 3 aprovada com limite de crédito. Saldo restante: 200**

**Compra 4 negada. Saldo insuficiente e limite de crédito excedido.**

**Compra 5 negada. Saldo insuficiente e limite de crédito excedido.** (resposta certa)

______

**5)** Qual é o principal ciclo de vida de um jogo em Phaser.js?

Escolha a opção que responde corretamente:

A) Setup -> Update -> Draw

**B) Preload -> Create -> Update**

C) Load -> Initialize -> Render

D) Begin -> Play -> End
______

**6)** Qual é o objetivo principal do módulo Arcade Physics em Phaser.js?

Escolha a opção que responde corretamente:

A) Renderizar gráficos 3D para jogos em HTML5.

**B) Simular interações físicas realistas, como colisões e movimentos, em jogos 2D.**

C) Criar efeitos de áudio para melhorar a experiência do usuário em jogos.

D) Gerenciar a lógica do jogo e a sincronização de eventos em jogos multiplayer.

______

# Questões dissertativas

**7)** 
```
var idade;

console.log ("insira sua idade");
idade = 28;

if (idade < 16) {
    console.log("você não pode votar");
} else if (idade >= 16 && idade < 18) {
    console.log ("o voto é facultativo");
} else {
    console.log ("o voto é obrigatório");
}
```
______

**8)** 
```
Classe FormaGeometrica:
    Atributos:
        - cor
Método Construtor(cor):
        Definir o valor do atributo cor com o valor passado como parâmetro.

Classe Retangulo herda de FormaGeometrica:
    Atributos:
        - cor
        - comprimento
        - largura

    Método Construtor(cor, comprimento, largura):
        Chamar o construtor da classe pai, passando cor como parâmetro
        Definir o valor dos atributos comprimento e largura com os valores passados como parâmetro.

    Método CalcularArea():
        Retornar comprimento * largura

Classe Circulo herda de FormaGeometrica:
    Atributos:
        - cor
        - raio

    Método Construtor(cor, raio):
        Chamar o construtor da classe pai, passando cor como parâmetro
        Definir o valor do atributo raio com o valor passado como parâmetro.

    Método CalcularArea():
        Retornar π * raio^2

```

______

**9)** 
```
Função corrida(distancia, velocidadeInicial, aceleracao, velocidadeMaxima, tempoMaximo):
    tempo = 0
    velocidade = velocidadeInicial

    Enquanto (distancia > 0) E (tempo <= tempoMaximo):
        velocidade = velocidadeInicial + aceleracao * tempo

        Se velocidade > velocidadeMaxima:
            velocidade = velocidadeMaxima

        distanciaPercorrida = velocidade * intervaloDeTempo

        Se distancia < distanciaPercorrida:
            distanciaPercorrida = distancia
            distancia = 0
        Senão:
            distancia -= distanciaPercorrida

        tempo += intervaloDeTempo

    Se distancia == 0:
        Retornar tempo
    Senão:
        Retornar "Tempo máximo excedido"

tempoTotal = corrida(distanciaDesejada, velocidadeInicialDesejada, aceleracaoDesejada, velocidadeMaximaPermitida, tempoMaximoPermitido)

Se tipo(tempoTotal) == número:
    Exibir "O carro completou a corrida em ", tempoTotal, " minutos."
Senão:
    Exibir "O carro não conseguiu completar a corrida dentro do tempo máximo."

```

______

**10)** 
```
Função MultiplicacaoDeMatrizes(matrizA, matrizB):
    Se tamanho(matrizA[0]) ≠ tamanho(matrizB) então:
        Retornar "As matrizes não podem ser multiplicadas. O número de colunas de A não é igual ao número de linhas de B."
    Senão:
        linhasMatrizA <- tamanho(matrizA)
        colunasMatrizA <- tamanho(matrizA[0]) # Número de colunas de matrizA
        colunasMatrizB <- tamanho(matrizB[0]) # Número de colunas de matrizB
        matrizResultado <- novaMatriz(linhasMatrizA, colunasMatrizB)

        Para i de 0 até linhasMatrizA-1 faça:
            Para j de 0 até colunasMatrizB-1 faça:
                produto <- 0
                Para k de 0 até tamanho(matrizB)-1 faça:
                    produto <- produto + matrizA[i][k] * matrizB[k][j]
                matrizResultado[i][j] <- produto

        Retornar matrizResultado

# Exemplo de uso da função
matrizA <- [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
matrizB <- [[9, 8, 7], [6, 5, 4], [3, 2, 1]]

matrizMultiplicacao <- MultiplicacaoDeMatrizes(matrizA, matrizB)
Escrever("Multiplicação das matrizes:")
ImprimirMatriz(matrizMultiplicacao)


```

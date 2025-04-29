1. Métodos de String em JavaScript
Manipulação de conteúdo:

charAt(index): Retorna o caractere localizado no índice indicado.

charCodeAt(index): Retorna o código Unicode do caractere no índice indicado.

concat(str1, str2, ...): Junta duas ou mais strings e retorna uma nova.

includes(substring): Verifica se a string contém a substring, retornando true ou false.

indexOf(substring, start): Retorna o índice da primeira ocorrência da substring. Retorna -1 se não encontrar.

lastIndexOf(substring, start): Retorna o índice da última ocorrência da substring.

slice(start, end): Extrai uma parte da string e retorna a nova substring.

substring(start, end): Semelhante ao slice, mas não aceita índices negativos.

substr(start, length): Extrai parte da string começando em um índice e por uma quantidade de caracteres (não é recomendado em código moderno).

Transformação de conteúdo:

toUpperCase(): Converte todos os caracteres para maiúsculas.

toLowerCase(): Converte todos os caracteres para minúsculas.

trim(): Remove espaços em branco no início e no fim da string.

replace(search, replacement): Substitui uma substring por outra.

Divisão e junção:

split(separator, limit): Divide a string em um array de substrings, usando o separador indicado.

join(separator) (do Array): Junta os elementos de um array em uma string, separando com o separador indicado.

2. Métodos de Arrays em JavaScript
Busca e Verificação:

indexOf(elemento, start): Retorna o primeiro índice em que o elemento é encontrado no array, ou -1 se não encontrar.

lastIndexOf(elemento, start): Retorna o último índice onde o elemento aparece.

includes(elemento, start): Verifica se o array contém o elemento, retornando true ou false.

find(callback): Retorna o primeiro elemento que satisfaz a função de teste fornecida.

findIndex(callback): Retorna o índice do primeiro elemento que satisfaz a função de teste.

Transformação e Iteração:

forEach(callback): Executa uma função para cada elemento do array. Não retorna novo array.

map(callback): Cria um novo array com o resultado da função aplicada a cada elemento do array original.

filter(callback): Cria um novo array com os elementos que passam no teste implementado pela função.

reduce(callback, initialValue): Executa uma função "redutora" em cada elemento do array, resultando em um único valor.

Ordenação:

sort(callback): Ordena os elementos do array no lugar. Se não passar uma função de comparação, os elementos são convertidos para string e ordenados lexicograficamente.

reverse(): Inverte a ordem dos elementos no array original.

3. Matrizes (Arrays de Arrays) de Forma Entendível
Pense em uma matriz como uma tabela com linhas e colunas. Em JavaScript, é representada como um array em que cada elemento é outro array.

Exemplo:

let matriz = [ [1, 2], [3, 4], [5, 6] ];

Para acessar elementos, usamos dois índices: primeiro a linha, depois a coluna.

Exemplo:

matriz[0][0] retorna 1 (primeiro elemento da primeira linha).
matriz[1][1] retorna 4 (segundo elemento da segunda linha).

Iteração em Matrizes (modo padrão):

for (let i = 0; i < matriz.length; i++) { console.log(Linha ${i}:); for (let j = 0; j < matriz[i].length; j++) { console.log( Coluna ${j}: ${matriz[i][j]}); } }

Explicações importantes:

matriz.length: número de linhas.

matriz[i].length: número de colunas na linha i.

Por que não usar matriz[0].length para tudo?
Porque se a matriz for irregular (com linhas de tamanhos diferentes), você pode tentar acessar índices que não existem ou ignorar elementos.

Forma segura para matrizes irregulares:

let matrizIrregular = [ [1, 2], [3], [4, 5, 6] ];

for (let i = 0; i < matrizIrregular.length; i++) { let linha = ""; for (let j = 0; j < matrizIrregular[i].length; j++) { linha += matrizIrregular[i][j] + " | "; } console.log(Linha ${i}: ${linha}); }

Assim você garante que percorre todos os elementos corretamente.

4. Node.js, NPM, Express.js e Caminhos
1. Inicialização do Projeto (NPM):

Abra o terminal na pasta do projeto.
Execute: npm init -y
Isso cria o arquivo package.json com as informações básicas do projeto.

2. Instalação do Express.js (NPM):

Execute: npm install express
Isso instala o Express.js e adiciona a dependência no package.json.

3. Arquivo Principal (Exemplo server.js):

const express = require('express');
const app = express();
const PORT = 3000;

Definindo rotas:

app.get('/', (req, res) => {
res.send('Olá, mundo com Express!');
});

app.get('/users/:id', (req, res) => {
const userId = req.params.id;
res.send(Detalhes do usuário com ID: ${userId});
});

Exemplo de Middleware:

const loggerMiddleware = (req, res, next) => {
console.log([${new Date().toISOString()}] ${req.method} ${req.url});
next();
};

app.use(loggerMiddleware);

Iniciando o servidor:

app.listen(PORT, () => {
console.log(Servidor rodando em http://localhost:${PORT});
});

Resumo dos conceitos:

npm init -y: Gera o package.json rapidamente.

npm install express: Instala o Express.js.

require('express'): Importa o módulo do Express.

app.get(): Cria uma rota que responde a requisições GET.

req.params: Acessa parâmetros de rota.

Middleware: Função que intercepta requisições.

app.use(): Aplica middleware para todas as rotas.

app.listen(): Inicia o servidor.

Sintaxe Básica do JavaScript
Declaração de variáveis:

let nome = "Maria";
const idade = 30;
var sobrenome = "Silva"; // (não é recomendado usar var)

Tipos básicos:

String: "texto"

Number: 10, 3.14

Boolean: true, false

Array: [1, 2, 3]

Object: { chave: "valor" }

2. Condicionais em JavaScript
if, else if, else:

if (idade >= 18) {
console.log("Maior de idade");
} else {
console.log("Menor de idade");
}

Operador ternário:

let status = (idade >= 18) ? "Adulto" : "Menor";

switch:

let dia = 3;

switch (dia) {
case 1:
console.log("Domingo");
break;
case 2:
console.log("Segunda");
break;
default:
console.log("Outro dia");
break;
}

3. Laços de Repetição em JavaScript
for tradicional:

for (let i = 0; i < 5; i++) {
console.log(i);
}

for...of (para Arrays):

let frutas = ["maçã", "banana", "uva"];

for (let fruta of frutas) {
console.log(fruta);
}

for...in (para objetos):

let pessoa = { nome: "João", idade: 25 };

for (let chave in pessoa) {
console.log(chave + ": " + pessoa[chave]);
}

while:

let contador = 0;

while (contador < 3) {
console.log(contador);
contador++;
}

do...while:

let numero = 0;

do {
console.log(numero);
numero++;
} while (numero < 3);

4. Formatação de Strings em JavaScript
Concatenação tradicional (+):

let saudacao = "Olá " + nome + "!";

Template literals (crase `):

let mensagem = Olá ${nome}, você tem ${idade} anos.;

Métodos úteis para strings:

"texto".toUpperCase() → transforma para MAIÚSCULAS

"TEXTO".toLowerCase() → transforma para minúsculas

" texto ".trim() → remove espaços nas pontas

"abc".includes("a") → retorna true se contém "a"

"abc".replace("a", "z") → troca "a" por "z"

5. Operadores Úteis em JavaScript
Aritméticos:

(soma)

(subtração)

(multiplicação)

/ (divisão)

% (módulo, resto da divisão)

Comparação:

== (igualdade de valor)

=== (igualdade de valor e tipo)

!= (diferente)

!== (diferente valor ou tipo)

(maior)

< (menor)

= (maior ou igual)

<= (menor ou igual)

Lógicos:

&& (E)

|| (OU)

! (NÃO)

6. Funções Básicas em JavaScript
Função tradicional:

function saudacao(nome) {
return "Olá, " + nome + "!";
}

Arrow function (forma moderna):

const saudacao = (nome) => {
return Olá, ${nome}!;
}

Se for uma linha só, pode simplificar:

const saudacao = nome => Olá, ${nome}!;

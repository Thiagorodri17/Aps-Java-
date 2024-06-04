# Aps-Java-
Trabalho de Java 
Disciplina: JavaScript
Código Da Turma: 963R
Nome: Thiago Rodrigues Santos
Matrícula: 2024101222
Link do GitHub: 
Função isPrime(num)
Essa função verifica se um número é primo ou não. Um número é primo se
For maior que 1 e não for divisível por nenhum número além de 1 e ele
Mesmo.
Function isPrime(num) {
 If (num <= 1) return false; // Números menores ou iguais a 1 não são
Primos
 If (num === 2) return true; // 2 é primo
 If (num % 2 === 0) return false; // Números pares maiores que 2 não são
Primos
 For (let i = 3; i <= Math.sqrt(num); i += 2) {
 If (num % i === 0) return false; // Se for divisível por qualquer
Número, não é primo
 }
 Return true; // Se não for divisível por nenhum, é primo
}
2. Função findLargestPrimes()
Essa função solicita um número ao usuário e encontra os 10 maiores
Números primos a partir desse número.
Function findLargestPrimes() {
 Let startNum = parseInt(prompt(“Digite um número:”));
 Let primes = [];

 // Inicializa a busca de números primos começando pelo startNum
 Let num = startNum;

 While (primes.length < 10) {
 If (isPrime(num)) {
 Primes.push(num);
 }
 Num++; // Incrementa para verificar o próximo número
 }

 // Exibe os 10 maiores números primos encontrados
 Console.log(“Os 10 maiores números primos a partir de “ + startNum + “
São:”);
 Console.log(primes);
}
Lógica Completa com o Loop
A função findLargestPrimes() usa um loop para iterar através dos números
Começando pelo número fornecido pelo usuário e verifica se cada número é
Primo usando a função isPrime(). Mantemos uma contagem dos números
Primos encontrados e exibimos os 10 maiores números primos quando a
Contagem atingir 10.
Código Completo
Aqui está o código completo combinando as duas funções:
Function isPrime(num) {
 If (num <= 1) return false;
 If (num === 2) return true;
 If (num % 2 === 0) return false;
 For (let i = 3; i <= Math.sqrt(num); i += 2) {
 If (num % i === 0) return false;
 }
 Return true;
}
Function findLargestPrimes() {
 Let startNum = parseInt(prompt(“Digite um número:”));
 Let primes = [];

 Let num = startNum;

 While (primes.length < 10) {
 If (isPrime(num)) {
 Primes.push(num);
 }
 Num++;
 }

 Console.log(“Os 10 maiores números primos a partir de “ + startNum +
“ são:”);
 Console.log(primes);
}
// Chama a função para iniciar a busca
findLargestPrimes();
1. Função isPrime(num): Verifica se um número é primo.
2. Função findLargestPrimes(): Solicita um número ao usuário, começa a
Verificar a partir desse número, e continua até encontrar 10 números
Primos.
3. Loop: Dentro da findLargestPrimes(), utilizamos um loop while que
Continua a incrementar o número e verificar se é primo até que 10 números
Primos sejam encontrados.
4. Exibição: Ao final, os 10 números primos encontrados são exibidos no
Console

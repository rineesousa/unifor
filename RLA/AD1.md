
<img src="https://drive.google.com/uc?id=1SOzRTjUt7cuBJpSqoK90fcAiKBrnpUJo" width="400">

**Curso:** ciencia da computação <br>
**Disciplina:** Raciocínio lógico algorítmico <br>
**Código/Turma:** T160-39 <br>
**Professor:** Ricardo Carubbi <br>
**Data:** 20/03/2024 <br>
**Aluno(a):** Rinee Alves Matos De Sousa <br>
**Matrícula:** 2417146 <br>

**1a chamada (Sim/Não):** sim <br>
**2a chamada (Sim/Não):** nao

### Exercicio 1
```
1  ALGORITMO troca_valores
2  DECLARE a, b, aux: INTEIRO
3  INICIO
4    ESCREVA "Digite o valor da a: "
5    LEIA a
6    ESCREVA "Digite o valor da b: "
7    LEIA b
8    aux = a
9    a = b
10   b = aux
11   ESCREVA "a =", a
12   ESCREVA "b =", b
13 FIM
```
### COMENTARIO 
Este pseudocódigo descreve um algoritmo simples para trocar os valores de duas variáveis, 'a' e 'b', utilizando uma variável auxiliar 'aux'. Inicialmente, o usuário é solicitado a fornecer os valores de 'a' e 'b'. Em seguida, os valores são trocados utilizando a variável auxiliar para armazenar temporariamente um dos valores. Por fim, os novos valores de 'a' e 'b' são exibidos. Este é um método eficaz e comum para realizar a troca de valores entre duas variáveis em muitas linguagens de programação.

### Exercicio 2
```
1  ALGORITMO contagem_aprovados
2  DECLARE n, cont, i, nota: INTEIRO
3  INICIO
4    ESCREVA "Digite o número de alunos: "
5    LEIA n
6    cont = 0
7    i = 1
8    ENQUANTO i <= n FAÇA
9      ESCREVA "Digite a nota do aluno ", i, ": "
10     LEIA nota
11     SE nota >= 50 E nota <= 100 ENTAO
12       cont = cont + 1
13     FIM_SE
14     i = i + 1
15   FIM_ENQUANTO
16   ESCREVA "Número de alunos aprovados: ", cont
17 FIM

```
### COMENTARIO 
Esse pseudocódigo descreve um algoritmo para contar o número de alunos aprovados, considerando um intervalo de notas entre 50 e 100. Inicialmente, solicita-se ao usuário que insira o número total de alunos ('n'). Em seguida, o algoritmo inicia um loop enquanto 'i' for menor ou igual a 'n'. Dentro desse loop, o algoritmo solicita a nota do aluno 'i' e verifica se está dentro do intervalo de aprovação (50 a 100). Se a nota estiver dentro desse intervalo, o contador 'cont' é incrementado em 1. Após percorrer todas as notas dos alunos, o algoritmo exibe o número total de alunos aprovados. Este é um algoritmo simples e eficaz para calcular a contagem de alunos aprovados em um conjunto de notas.

### Exercicio 3
```
1  ALGORITMO soma_numeros
2  DECLARE n, soma, i, num: INTEIRO
3  INICIO
4    ESCREVA "Digite a quantidade de números (n >= 0): "
5    LEIA n
6    SE n < 0 ENTAO
7      ESCREVA "O valor deve ser maior ou igual a zero!"
8      RETORNE
9    FIM_SE
10   soma = 0
11   i = 1
12   ENQUANTO i <= n FAÇA
13     ESCREVA "Digite um número: "
14     LEIA num
15     soma = soma + num
16     i = i + 1
17   FIM_ENQUANTO
18   ESCREVA "A soma dos números é ", soma
19 FIM

```
### COMENTARIOS 
Este pseudocódigo descreve um algoritmo para calcular a soma de uma quantidade 'n' de números fornecidos pelo usuário. Primeiro, solicita-se ao usuário que insira a quantidade de números ('n'), garantindo que 'n' seja maior ou igual a zero. Se 'n' for menor que zero, o algoritmo exibirá uma mensagem de erro e retornará, encerrando a execução. Caso contrário, a variável 'soma' é inicializada como zero e um loop é iniciado para solicitar 'n' números do usuário. A cada iteração do loop, o algoritmo adiciona o número fornecido à variável 'soma'. Após a obtenção de todos os números, a soma total é exibida. Este é um algoritmo simples e útil para calcular a soma de uma série de números fornecidos pelo usuário, com uma validação básica para garantir que a quantidade de números seja válida.

### Exercicio 4
```
1  ALGORITMO serie_S
2  DECLARE n, i, numerador, denominador: INTEIRO
3  DECLARE termo, S: REAL
4  INICIO
5    ESCREVA "Digite o número de termos da série S: "
6    LEIA n
7    S = 0
8    PARA i DE 0 ATÉ n PASSO 1 FAÇA
9      numerador = 2 * i + 1
10     denominador = 2 * i + 2
11     termo = numerador / denominador
12     S += termo
13   FIM_PARA
14   ESCREVA "Soma da série S é ", S
15 FIM

```
### COMENTARIOS 
Este é um algoritmo eficiente para calcular a soma de uma série matemática específica até um número de termos determinado pelo usuário. É útil para fins de análise numérica e pode ser adaptado para diferentes séries matemáticas.

### Exercicio 5
```
1  ALGORITMO calcular_fatorial
2  DECLARE n, i, fator: INTEIRO
3  INICIO
4    ESCREVA "Digite um número inteiro não-negativo: "
5    LEIA n
6    SE n < 0 ENTAO
7      ESCREVA "O valor deve ser maior ou igual a zero!"
8      RETORNE
9    FIM_SE
10   fator = 1
11   PARA i DE 1 ATÉ n PASSO 1 FAÇA
12     fator = fator * i
13   FIM_PARA
14   ESCREVA "O fatorial de ", n, " é: ", fator
15 FIM

```
### COMENTARIO
Este pseudocódigo descreve um algoritmo para calcular o fatorial de um número inteiro não negativo fornecido pelo usuário. Inicialmente, o usuário é solicitado a inserir um número inteiro não negativo ('n'). O algoritmo verifica se o número fornecido é válido, ou seja, se é maior ou igual a zero. Se o número não for válido, o algoritmo exibirá uma mensagem de erro e encerrará a execução. Caso contrário, o algoritmo calcula o fatorial do número utilizando um loop 'PARA', multiplicando progressivamente o valor de 'fator' pelo valor atual do índice do loop até atingir 'n'. Após o término do loop, o resultado do fatorial é exibido na tela. Este é um algoritmo eficiente e comum para calcular o fatorial de um número inteiro, útil em diversas aplicações matemáticas e de programação.

### Exercicio 6
```
1  ALGORITMO serie_fibonacci
2  DECLARE n, a, b, termo_atual, i: INTEIRO
3  INICIO
4    ESCREVA "Número de termos da série Fibonacci: "
5    LEIA n
6    a = 0
7    b = 1
8    PARA i DE 1 ATÉ n PASSO 1 FAÇA
9      ESCREVA a
10     termo_atual = a + b
11     a = b
12     b = termo_atual
13   FIM_PARA
14 FIM

```
### COMENTARIO 
Este pseudocódigo descreve um algoritmo para gerar os primeiros 'n' termos da sequência de Fibonacci. A sequência de Fibonacci é uma série de números em que cada número é a soma dos dois anteriores.

No início do algoritmo, o usuário é solicitado a fornecer o número de termos da sequência desejada ('n'). As variáveis 'a' e 'b' são inicializadas como 0 e 1, respectivamente, pois estes são os dois primeiros números da sequência.

Em seguida, um loop 'PARA' é utilizado para iterar de 1 até 'n', onde cada iteração exibe o valor atual de 'a' (que é o primeiro número da sequência de Fibonacci para a iteração atual), calcula o próximo termo da sequência de Fibonacci somando 'a' e 'b' e atualiza as variáveis 'a' e 'b' para os próximos números na sequência.

Ao final do loop, os 'n' primeiros termos da sequência de Fibonacci são exibidos. Este é um algoritmo simples e eficaz para gerar a sequência de Fibonacci até um número específico de termos, sendo útil em várias aplicações matemáticas e de programação.

### Exercicio 7
```
1  ALGORITMO inverte_numero
2  DECLARE num, num_inv, digito: INTEIRO
3  INICIO
4    ESCREVA "Digite um número inteiro: "
5    LEIA num
6    SE num >= 0 ENTAO
7      num_inv = 0
8      SE num > 0 ENTAO
9        REPITA
10         digito = num % 10
11         num_inv = num_inv * 10 + digito
12         num = num // 10
13        ATÉ num > 0
14     ESCREVA "Número invertido:", num_inv
15   SENAO
16     ESCREVA "O número deve ser positivo!"
17   FIM_SE
18 FIM

```
### COMENTARIO 
Este pseudocódigo descreve um algoritmo para inverter um número inteiro positivo fornecido pelo usuário.

Inicialmente, o usuário é solicitado a inserir um número inteiro ('num'). O algoritmo verifica se o número fornecido é maior ou igual a zero. Se for, o algoritmo inicia o processo de inversão.

O algoritmo utiliza uma variável 'num_inv' para armazenar o número invertido e um loop 'REPITA' para iterar enquanto o número fornecido for maior que zero. Dentro do loop, o algoritmo calcula o último dígito do número original ('num') usando o operador de módulo (%), e adiciona esse dígito à variável 'num_inv' após deslocar os dígitos já invertidos uma posição para a esquerda e somar o último dígito. O número original é então atualizado, dividindo-o por 10 para remover o último dígito.

Após inverter todos os dígitos do número, o algoritmo exibe o número invertido ('num_inv'). Se o número fornecido não for positivo, o algoritmo exibirá uma mensagem de erro.

Este é um algoritmo eficiente e útil para inverter números inteiros positivos, e pode ser utilizado em diversas aplicações, como processamento de dados e criptografia.

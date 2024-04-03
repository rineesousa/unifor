# UNIFOR
**nome**: rinee alves 
**disciplina**:Raciocínio logico algorítmico 

## Lista 3

### Exercicio 1
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite um número inteiro positivo}}
B --> C[\numero\]
C --> D{Verificar se número é negativo}
D -- SIM --> E{{Exibir mensagem de erro e solicitar novo número}}
E --> F[ESCREVA Número inválido. Por favor, digite um número inteiro positivo.]
F --> B
D -- NÃO --> G{{Verificar se número é par ou ímpar}}
G --> H{numero MOD 2 = 0}
H -- SIM --> I{{Exibir Número é par}}
I --> J[ESCREVA numero, é um número par.]
J --> K([FIM])
H -- NÃO --> L{{Exibir Número é ímpar}}
L --> M[ESCREVA numero,  é um número ímpar.]
M --> K

```
### Pseudocodigo
```
1  ALGORITMO verificar_par_ou_impar
2  DECLARE numero: INTEIRO
3  INICIO
4    REPITA
5        ESCREVA "Digite um número inteiro positivo: "
6        LEIA numero
7        
8        SE numero < 0 ENTÃO
9            ESCREVA "Número inválido. Por favor, digite um número inteiro positivo."
10       FIM_SE
11   ATÉ que numero >= 0
12   
13   SE numero MOD 2 = 0 ENTÃO
14       ESCREVA numero, " é um número par."
15   SENÃO
16       ESCREVA numero, " é um número ímpar."
17   FIM_SE
18   
19   FIM
```
### Teste de mesa
Vamos criar uma tabela semelhante usando o pseudocódigo fornecido:

| número | número >= 0 | resto | resto == 0 | Saída |
| ------ | ----------- | ----- | ---------- | ------|
| -1     | F           |       |            | "Número inválido. Por favor, digite um número inteiro positivo." |
| 0      | V           | 0     | V          | "0 é um número par." |
| 13     | V           | 1     | F          | "13 é um número ímpar." |
| 30     | V           | 0     | V          | "30 é um número par." |

### COMENTARIO 
Este pseudocódigo descreve um algoritmo para verificar se um número inteiro positivo fornecido pelo usuário é par ou ímpar.

Inicialmente, o algoritmo entra em um loop 'REPITA', que continuará solicitando ao usuário para digitar um número inteiro positivo até que o número fornecido seja de fato positivo. Durante cada iteração do loop, o usuário é solicitado a inserir um número, que é armazenado na variável 'numero'. 

Se o número fornecido pelo usuário for negativo, o algoritmo exibirá uma mensagem de erro e solicitará que o usuário insira um número positivo. O loop continuará executando até que um número válido seja inserido.

Após obter um número inteiro positivo, o algoritmo verifica se o número é par ou ímpar usando o operador MOD. Se o resultado da operação MOD 2 for igual a zero, o número é considerado par e uma mensagem indicando isso é exibida. Caso contrário, o número é considerado ímpar e uma mensagem indicando isso é exibida.

Este é um algoritmo simples e eficaz para verificar se um número inteiro é par ou ímpar, com uma validação básica para garantir que apenas números positivos sejam aceitos. Ele pode ser útil em várias situações onde a classificação de números por paridade é necessária.

### Exercicio 2

### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Inicializar contador}}
B --> C[\contador = 0\]
C --> D{Verificar se contador é menor ou igual a 30}
D -- SIM --> E{{Exibir contador}}
E --> F[ESCREVA contador]
F --> G{{Incrementar contador}}
G --> H[contador = contador + 3]
H --> D
D -- NÃO --> I([FIM])

```
### Pseudocodigo
```
1  ALGORITMO exibir_multiplos_de_3
2  DECLARE contador: INTEIRO
3  INICIO
4    PARA contador DE 0 ATÉ 30 PASSO 3 FAÇA
5        ESCREVA contador
6    FIM_PARA
7   
8    FIM

```
### Teste de mesa

| contador | contador é múltiplo de 3 | Saída |
| -------- | ------------------------ | ------|
| 0        | V                        | 0     |
| 3        | V                        | 3     |
| 6        | V                        | 6     |
| 9        | V                        | 9     |
| 12       | V                        | 12    |
| 15       | V                        | 15    |
| 18       | V                        | 18    |
| 21       | V                        | 21    |
| 24       | V                        | 24    |
| 27       | V                        | 27    |
| 30       | V                        | 30    |

### COMENTARIO 
Este pseudocódigo descreve um algoritmo simples para exibir os múltiplos de 3 no intervalo de 0 a 30.

O algoritmo utiliza um loop 'PARA' que começa em 0 e vai até 30, com incrementos de 3 em 3. Dentro do loop, cada número do contador é verificado e, se for um múltiplo de 3, é exibido na tela.

Esse é um método direto e eficiente para encontrar e exibir os múltiplos de 3 dentro de um intervalo específico. É útil em situações em que apenas os múltiplos de um determinado número precisam ser identificados e exibidos.

### Exercicio 3

### Fluxograma
```mermaid
flowchart 
A([Início]) --> B[Inicializar soma como 0]
    B --> C[Inicializar sequência de números]
    C --> D{Há mais números na sequência?}
    D -->|Sim| E[Adicionar próximo número à soma]
    E --> F{Há mais números na sequência?}
    F -->|Sim| D
    F -->|Não| G[Imprimir soma]
    G --> H([Fim])
```
### Pseudocodigos
```
1  ALGORITMO calcular_soma_sequencia
2  DECLARE sequencia: VETOR DE INTEIRO
3  DECLARE tamanho, soma, i: INTEIRO
4  INICIO
5    tamanho <- tamanho do vetor sequencia
6    soma <- 0
7    
8    // Preencher o vetor sequencia
9    PARA i DE 0 ATÉ tamanho - 1 FAÇA
10       ESCREVA "Digite o elemento ", i + 1, " da sequência: "
11       LEIA sequencia[i]
12   FIM_PARA
13   
14   // Calcular a soma da sequência
15   PARA i DE 0 ATÉ tamanho - 1 FAÇA
16       soma <- soma + sequencia[i]
17   FIM_PARA
18   
19   ESCREVA "A soma da sequência é: ", soma
20   
21   FIM

```
### Teste de mesa

| Sequência | Tamanho | Soma | Saída |
| --------- | ------- | ---- | ----- |
| {2, 5, 8} | 3       | 15   | "A soma da sequência é: 15" |
### COMENTARIO 
Este pseudocódigo descreve um algoritmo para calcular a soma dos elementos de uma sequência de números fornecidos pelo usuário.

Inicialmente, o algoritmo declara um vetor de inteiros chamado 'sequencia' e variáveis para armazenar o tamanho da sequência, a soma dos elementos e um índice de iteração.

O algoritmo então solicita ao usuário que insira cada elemento da sequência, preenchendo o vetor 'sequencia' com os valores fornecidos.

Após preencher o vetor, o algoritmo utiliza um loop 'PARA' para percorrer todos os elementos do vetor e calcular a soma dos seus valores, armazenando o resultado na variável 'soma'.

Por fim, o algoritmo exibe a soma dos elementos da sequência.

Este é um algoritmo eficaz para calcular a soma dos elementos de uma sequência de números. É útil em diversas situações, como em problemas matemáticos ou análise de dados. Além disso, o uso de vetores permite que o algoritmo seja aplicado a sequências de qualquer tamanho.

### Exercicio 4

### Fluxograma 
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Inicializar soma e contador}}
B --> C[soma = 0]
C --> D[contador = 0]
D --> E{{Repetir até que seja digitada uma nota negativa}}
E --> F{Digite a nota do aluno ou uma nota negativa para encerrar}
F --> G[\nota\]
G --> H{Verificar se nota é maior ou igual a zero}
H -- SIM --> I{{Atualizar soma e contador}}
I --> J[soma = soma + nota]
J --> K[contador = contador + 1]
H -- NÃO --> L{{Verificar se contador é maior que zero}}
L --> M{Definir quantidade_notas}
M --> N[quantidade_notas = contador]
N --> O{Calcular média}
O --> P[media = soma / contador]
P --> Q{{Exibir quantidade de notas e média}}
Q --> R[ESCREVA Foram lidas , quantidade_notas,  notas.]
R --> S[ESCREVA A média aritmética é , media, !]
L -- NÃO --> T{{Exibir mensagem de nenhuma nota inserida}}
T --> U[ESCREVA Nenhuma nota foi inserida!]
U --> V([FIM])
E -- NÃO --> V
```
### Pseudocodigo
```
1  ALGORITMO calcular_media_alunos
2  DECLARE nota, soma, contador: REAL
3  DECLARE quantidade_notas: INTEIRO
4  INICIO
5    soma <- 0
6    contador <- 0
7    
8    REPITA
9        ESCREVA "Digite a nota do aluno (ou uma nota negativa para encerrar): "
10       LEIA nota
11       
12       SE nota >= 0 ENTÃO
13           soma <- soma + nota
14           contador <- contador + 1
15       FIM_SE
16   ATÉ que nota < 0
17   
18   SE contador > 0 ENTÃO
19       quantidade_notas <- contador
20       media <- soma / contador
21       ESCREVA "Foram lidas ", quantidade_notas, " notas."
22       ESCREVA "A média aritmética é ", media, "!"
23   SENÃO
24       ESCREVA "Nenhuma nota foi inserida!"
25   FIM_SE
26   
27   FIM
```
### Teste de mesa
| Nota | Nota >= 0 | Soma | Contador | Saída |
| ---- | --------- | ---- | -------- | ------|
| 5.0  | V         | 5.0  | 1        | |
| 7.5  | V         | 12.5 | 2        | |
| -1   | F         |      |          | "Foram lidas 2 notas. A média aritmética é 6.25!" |

### COMENTARIO
Este pseudocódigo descreve um algoritmo para calcular a média aritmética das notas dos alunos. O algoritmo solicita ao usuário que insira as notas dos alunos, permitindo que eles insiram quantas notas desejarem. O usuário pode encerrar a entrada de notas inserindo um valor negativo.

O algoritmo utiliza variáveis para armazenar a soma das notas ('soma'), o número de notas inseridas ('contador') e a quantidade total de notas ('quantidade_notas'). Além disso, é declarada uma variável para armazenar a média das notas ('media').

Durante o processo de entrada das notas, o algoritmo verifica se a nota inserida pelo usuário é válida (ou seja, se é não negativa). Se for, a nota é somada à soma total das notas e o contador é incrementado. O loop continua até que o usuário insira uma nota negativa, indicando o fim da entrada.

Após encerrar a entrada de notas, o algoritmo verifica se pelo menos uma nota foi inserida (verificando se o contador é maior que zero). Se sim, calcula a média aritmética das notas e exibe a quantidade total de notas lidas e a média aritmética. Se nenhum nota foi inserida, o algoritmo exibe uma mensagem informando isso.

Este é um algoritmo eficaz para calcular a média das notas dos alunos, permitindo uma entrada flexível de dados e fornecendo feedback adequado ao usuário. É útil em situações onde é necessário calcular a média de um conjunto variável de valores, como em sistemas de gestão educacional.

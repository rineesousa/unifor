# UNIFOR
**nome**: rinee alves 
**disciplina**:Raciocínio logico algorítmico 
## Lista 2 

### Exercicio 1
### Fluxograma
```mermaid
flowchart TD
A([INICIO]) --> B{{Digite o primeiro número}}
B --> C[\num1\]
C --> D{{Digite o segundo número}}
D --> E[\num2\]
E --> F{{Digite o terceiro número}}
F --> G[\num3\]
G --> H{{Digite o quarto número}}
H --> I[\num4\]
I --> J[soma = num1 + num2 + num3 + num4]
J --> K[media = soma / 4]
K --> L{{'A média é: ', media}}
L --> M([FIM])
```
### Pseudocodigo
```
1  ALGORITMO calcular_media
2  DECLARE num1, num2, num3, num4, soma, media: REAL
3  INICIO
4    ESCREVA "Digite o primeiro número: "
5    LEIA num1
6    ESCREVA "Digite o segundo número: "
7    LEIA num2
8    ESCREVA "Digite o terceiro número: "
9    LEIA num3
10   ESCREVA "Digite o quarto número: "
11   LEIA num4
12   soma = num1 + num2 + num3 + num4
13   media = soma / 4
14   ESCREVA "A média é: ", media
15 FIM

```
### Teste de mesa


| Teste | num1 | num2 | num3 | num4 | soma (cálculo esperado) | média (cálculo esperado) | Saída esperada |
| ----- | ---- | ---- | ---- | ---- | ----------------------- | ------------------------ | --------------- |
| 1     | 2    | 4    | 6    | 8    | 20 (2 + 4 + 6 + 8)      | 5                        | "A média é: 5"  |

### COMENTARIO 
Este pseudocódigo descreve um algoritmo simples para calcular a média de quatro números fornecidos pelo usuário.

Inicialmente, o usuário é solicitado a inserir quatro números. Cada número é armazenado em uma variável diferente: 'num1', 'num2', 'num3' e 'num4'. 

Em seguida, o algoritmo calcula a soma desses quatro números e armazena o resultado na variável 'soma'. Depois, a média é calculada dividindo a soma pelo número de elementos, que neste caso é 4. O resultado é armazenado na variável 'media'.

Por fim, o algoritmo exibe a média calculada na tela.

Este é um algoritmo simples e eficaz para calcular a média de um conjunto de números. Ele pode ser útil em diversas situações, como em aplicações de processamento de dados ou em sistemas de notas escolares.


### Exercicio 2

### Fluxograma
```mermaid
flowchart TD
A([INICIO]) --> B{{Digite a temperatura em Celsius C}}
B --> C[\temp_C\]
C --> D[Converter para Fahrenheit]
D --> E[temp_F = 9/5 * temp_C + 32]
E --> F{{A temperatura em Fahrenheit é: , temp_F}}
F --> G([FIM])
```
### Pseucodigo
```
1  ALGORITMO converter_temperatura
2  DECLARE temp_C, temp_F: REAL
3  INICIO
4    ESCREVA "Digite a temperatura em Celsius (C): "
5    LEIA temp_C
6    temp_F = (9/5) * temp_C + 32
7    ESCREVA "A temperatura em Fahrenheit é: ", temp_F
8  FIM

```
### Teste de mesa
| Teste | temp_C | temp_F (cálculo esperado) | Saída esperada |
| ----- | ------ | -------------------------- | --------------- |
| 1     | 0      | 32                         | "A temperatura em Fahrenheit é: 32" |

 ### COMENTARIO 
 Este pseudocódigo descreve um algoritmo simples para converter uma temperatura de Celsius para Fahrenheit. 

Inicialmente, o usuário é solicitado a inserir a temperatura em graus Celsius ('temp_C'). Em seguida, o algoritmo realiza o cálculo da conversão de Celsius para Fahrenheit usando a fórmula padrão de conversão, que é multiplicar a temperatura em Celsius por 9/5 e adicionar 32. O resultado da conversão é armazenado na variável 'temp_F'. 

Por fim, o algoritmo exibe a temperatura convertida em Fahrenheit na tela.

Este é um algoritmo útil e direto para realizar a conversão de temperatura entre as escalas Celsius e Fahrenheit. Pode ser empregado em muitas aplicações práticas, como em programas de previsão do tempo, sistemas de controle de temperatura ou em tarefas de engenharia e física.

### Exercicio 3

### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite o primeiro número}}
B --> C[\num1\]
C --> D{{Digite o segundo número}}
D --> E[\num2\]
E --> F{{Digite o operador +, -, *, /}}
F --> G[\operador\]
G --> H{operador é '+'}
H -- SIM --> I{Efetuar adição}
I --> J[resultado = num1 + num2]
J --> K{{'O resultado da adição é: ', resultado}}
K --> L([FIM])
H -- NÃO --> M{operador é '-'}
M -- SIM --> N{Efetuar subtração}
N --> O[resultado = num1 - num2]
O --> K
M -- NÃO --> P{operador é '*'}
P -- SIM --> Q{Efetuar multiplicação}
Q --> R[resultado = num1 * num2]
R --> K
P -- NÃO --> S{operador é '/'}
S -- SIM --> T{Verificar divisão por zero}
T -- SIM --> U[Se num2 != 0 então calcular divisão]
U --> V[resultado = num1 / num2]
V --> K
T -- NÃO --> W[Escrever Erro: Divisão por zero.]
W --> L
S -- NÃO --> X[Escrever Operador inválido.]
X --> L
```
### Pseudocodigo
```
1  ALGORITMO calculadora
2  DECLARE num1, num2, resultado: REAL
3  DECLARE operador: CARACTERE
4  INICIO
5    ESCREVA "Digite o primeiro número: "
6    LEIA num1
7    ESCREVA "Digite o segundo número: "
8    LEIA num2
9    ESCREVA "Digite o operador (+, -, *, /): "
10   LEIA operador
11   SE operador = '+' ENTAO
12     resultado = num1 + num2
13     ESCREVA "O resultado da adição é: ", resultado
14   SENAO SE operador = '-' ENTAO
15     resultado = num1 - num2
16     ESCREVA "O resultado da subtração é: ", resultado
17   SENAO SE operador = '*' ENTAO
18     resultado = num1 * num2
19     ESCREVA "O resultado da multiplicação é: ", resultado
20   SENAO SE operador = '/' ENTAO
21     SE num2 != 0 ENTAO
22       resultado = num1 / num2
23       ESCREVA "O resultado da divisão é: ", resultado
24     SENAO
25       ESCREVA "Erro: Divisão por zero."
26     FIM_SE
27   SENAO
28     ESCREVA "Operador inválido."
29   FIM_SE
30 FIM
```
### Teste de mesa
| Etapa | Descrição                              | Dados/Resultado |
|-------|----------------------------------------|------------------|
| Início|                                        |                  |
| Passo 1| Digite o primeiro número - a:         | a = 10           |
| Passo 2| Digite o operador: +, -, *, /:        | operador = "+"   |
| Passo 3| Digite o segundo número - b:          | b = 5            |
| Passo 4| Verificar operador válido:            | Sim              |
| Passo 5| Realizar operação:                    | resultado = 15   |
| Passo 6| Imprimir resultado:                   | 15               |
| Passo 7| Fim                                   |                  |

### COMENTARIO 
Este pseudocódigo descreve uma calculadora simples que permite ao usuário realizar operações básicas de adição, subtração, multiplicação e divisão entre dois números.

O usuário é solicitado a inserir dois números e o operador desejado (adição, subtração, multiplicação ou divisão). Depois de inserir os números e o operador, o algoritmo verifica qual operação deve ser realizada com base no operador fornecido.

Se o operador for '+', o algoritmo realiza a adição dos dois números e exibe o resultado. Se for '-', realiza a subtração, se for '*', realiza a multiplicação e se for '/', realiza a divisão. Além disso, o algoritmo também verifica se a divisão por zero é evitada.

Caso o operador inserido não seja válido, o algoritmo exibe uma mensagem de erro indicando que o operador é inválido.

Este é um algoritmo básico e útil para realizar operações aritméticas simples, podendo ser útil em várias situações cotidianas que envolvam cálculos simples.

### Exercicio 4

### Fluxograma
```mermaid
flowchart TD
A([INÍCIO]) --> B{{Digite a idade}}
B --> C[\idade\]
C --> D{idade >= 5}
D -- SIM --> E{idade <= 7}
E -- SIM --> F{{'Categoria: Infantil A'}}
F --> L([FIM])
E -- NÃO --> G{idade <= 10}
G -- SIM --> H{{'Categoria: Infantil B'}}
H --> L
G -- NÃO --> I{idade <= 13}
I -- SIM --> J{{'Categoria: Juvenil A'}}
J --> L
I -- NÃO --> K{idade <= 17}
K -- SIM --> M{{'Categoria: Juvenil B'}}
M --> L
K -- NÃO --> N{{'Categoria: Adulto'}}
N --> L
D -- NÃO --> O{{'Idade inválida'}}
O --> L

```
### Pseudocodigo
```
1  ALGORITMO categorizar_idade
2  DECLARE idade: INTEIRO
3  INICIO
4    ESCREVA "Digite a idade: "
5    LEIA idade
6    
7    SE idade >= 5 E idade <= 7 ENTÃO
8        ESCREVA "Categoria: Infantil A"
9    
10   SENÃO SE idade <= 10 ENTÃO
11       ESCREVA "Categoria: Infantil B"
12   
13   SENÃO SE idade <= 13 ENTÃO
14       ESCREVA "Categoria: Juvenil A"
15   
16   SENÃO SE idade <= 17 ENTÃO
17       ESCREVA "Categoria: Juvenil B"
18   
19   SENÃO
20       ESCREVA "Categoria: Adulto"
21   
22   FIM_SE
23   
24   FIM
```
### Teste de mesa
| Etapa | Descrição                                        | Dados/Resultado |
|-------|--------------------------------------------------|------------------|
| Início|                                                |                  |
| Passo 1| Digite a idade:                                 | idade =          |
| Passo 2| Verificar idade >= 5 E idade <= 7              |                  |
|        |   - Verdadeiro:                                |                  |
|        |     - Categoria: Infantil A                    |                  |
| Passo 3| Verificar idade <= 10                          |                  |
|        |   - Verdadeiro:                                |                  |
|        |     - Categoria: Infantil B                    |                  |
| Passo 4| Verificar idade <= 13                          |                  |
|        |   - Falso:                                     |                  |
| Passo 5| Verificar idade <= 17                          |                  |
|        |   - Falso:                                     |                  |
| Passo 6| Categoria: Adulto                               |                  |
| Passo 7| Fim                                            |                  |
```
### COMENTARIO
Este pseudocódigo descreve um algoritmo simples para categorizar a idade de uma pessoa em diferentes faixas etárias, de acordo com critérios estabelecidos para cada categoria.

O usuário é solicitado a inserir a idade, que é armazenada na variável 'idade'. Em seguida, o algoritmo verifica a idade inserida e, com base nessa idade, determina em qual categoria a pessoa se enquadra.

Se a idade estiver entre 5 e 7 anos (inclusive), o algoritmo exibe a mensagem "Categoria: Infantil A". Se estiver entre 8 e 10 anos (inclusive), exibe "Categoria: Infantil B". Se estiver entre 11 e 13 anos (inclusive), exibe "Categoria: Juvenil A". Se estiver entre 14 e 17 anos (inclusive), exibe "Categoria: Juvenil B". Se a idade for maior que 17 anos, exibe "Categoria: Adulto".

Este é um algoritmo eficiente e claro para classificar a idade em diferentes categorias, sendo útil em diversas situações, como em sistemas de inscrição esportiva, atividades recreativas ou eventos culturais que exigem categorização por faixa etária.

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


# UNIFOR
**nome**: rinee alves 
**disciplina**:Raciocínio logico algorítmico 
## Lista 1, Exercício 1
### fluxograma 
```mermaid 
flowchart TD
a([inicio])--> B{{digite um numero}}
B --> C[\numero\]
C --> D{nmero> 0}
D --nao--> F[o numero nao e positivo!]
D --sim--> E[resto= numero % 2]
F --> Z([FIM]) 
E --> G{resto == 0}
G --nao--> H{{ o numero e impar!}}
G --sim--> I{{ o numero e apar!}} 
H --> Z
I --> Z
```
###Pseudocódigo
```  
1  ALGORITIMO verifica_par_impar
2  DECLARE numero, resto NUMERICO
3  ESCREVA "digite um numero"
4 LEIA numero 
5 SE numero > 0 ENTAO 
6 		resto = numero % 2
7		se resto for == 0 ENTAO
8			ESCREVA "o numero é par!"
9		SENAO
10			ESCREVA "o numero e impar!"
11	SENAO
12		ESCREVA "o numero nao e positivo!"
13FIM_ALGORITIMO
```  
#### Teste de mesa (0,25 ponto)
| numero | numero >= 0 | resto | resto == 0 | Saída |
| -- | -- | -- | -- | -- | 
| -1 | F |   |   | "O número deve ser postivo!" |
| 0  | V | 0 | V | "O número é par!" |
| 13 | V | 1 | F | "O número é impar!" |
| 30 | V | 0 | V | "O número é par!" |

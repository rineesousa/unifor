
# UNIFOR
**nome**: rinee alves 
**disciplina**:Raciocínio logico algorítmico 
## Exercício 3
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

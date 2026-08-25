# Rules de math

retorna sempre um número

## Operations:

 - math:
    - '+': soma
    - '-': subtração
    - '*': multiplicação
    - '/': divisão
    - '%': resto de divisão
    - '**': potência

 - round ["round-up", "round-down", "cut-up", "cut-down"]
    - 'round-up': 
        - 0.4 > 0 | 0.5 > 1 | 0.6 > 1
    - 'round-down': 
        - 0.4 > 0 | 0.5 > 0 | 0.6 > 1
    - 'cut-up': 
        - 0.1 > 1 | 0.9 > 1
    - 'cut-down': 
        - 0.1 > 0 | 0.9 > 0

## Exemplos:

### Operação simples de soma e multiplicação
    // Equivale a algo como: 1 + (2 * 3) = 7

    {
        "mimic-version": '1.0.0',
        "rule-type": 'math',
        "root": {
            "operation-type": 'math',
            "operation": '+',
            "arguments": [
                1,

                {
                    "operation-type": 'math',
                    "operation": '*',
                    "arguments": [
                        2, 3
                    ]
                }
            ]
        }
    } > 7

### Rounds
    // round-up(1/2) + 1/2 = 1,5
    {
        "mimic-version": '1.0.0',
        "rule-type": 'math',
        "root": {

            "operation-type": 'math',
            "operation": '+',
            "arguments": [

                {
                    "operation-type": 'round',
                    "operation": 'round-up',
                    "arguments": [
                        {
                            "operation-type": 'math',
                            "operation": '/',
                            arguments: [
                                1, 2
                            ]
                        }
                    ]
                },
                
                {
                    "operation-type": 'math',
                    "operation": '/',
                    "arguments": [
                        1, 2
                    ]
                }

            ],
        }
    } > 1,5
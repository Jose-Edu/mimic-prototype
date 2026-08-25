# Rule validation
Sempre retorna um boolean

## Operations:

 - validation:
    - '=': igual
    - '!=': diferente
    - 'and': AND
    - 'or': OR
    - 'xor': XOR
    - 'not': NOT
    - '>': Maior
    - '<': Menor
    - '>=': Maior ou igual
    - '<=': Menor ou igual

## Exemplo:

{
    "mimic-version": '1.0.0',
    "rule-type": 'valitation',
    "root": {
        "operation-type": 'validation',
        "operation": 'and',
        "arguments": [

            {
                "operation-type": 'validation',
                "operation": '>',
                "arguments": [5, 1]
            },

            {
                "operation-type": 'validation',
                "operation": 'not',
                "arguments": [
                    {                
                    "operation-type": 'validation',
                    "operation": '<',
                    "arguments": [5, 1]
                    }
                ]
            }
        ]
    }
} > True
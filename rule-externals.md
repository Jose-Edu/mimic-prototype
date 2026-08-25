# Rules externals

Resolvem dados externos à rule

## Operations:
 - get_related: retorna um valor/entity a partir de uma entity base. Recebe uma lista de níveis nescessários para resolver a dependência: ["internal_name", "tabela de relação", "nome para consulta"]
 - get: retorna o valor direto de uma dependência "internal_name"
 - get_by_id: retorna um valor externo por id, sem preenchimento externo: "tabela", "id"


## Exemplos:

considerando campo atk = 1

{
    "mimic_version": '1.0.0',
    "rule_type": '',
    "root": {
        "operation_type": 'math',
        "operation": '+',
        "arguments": [
        {
            "operation_type": "external",
            "operation": "get_related",
            "arguments": [
                ["sheet1", "entity_attribute", "atk"]
            ],
        },

        1

        ]
    }
} > 2

// considerando o ext como um int 1
{
    "mimic_version": '1.0.0',
    "rule_type": '',
    "root": {
        "operation_type": 'math',
        "operation": '+',
        "arguments": [
        {
            "operation_type": "external",
            "operation": "get",
            "arguments": [
                "ext"
            ],
        },

        1

        ]
    }
} > 2

{
    "mimic_version": '1.0.0',
    "rule_type": '',
    "root": {
        "operation_type": 'math',
        "operation": '+',
        "arguments": [
        {
            "operation_type": "external",
            "operation": "get",
            "arguments": [
                "global"
            ],
        },

        1

        ]
    }
} > 2

considere rule de id 1 como uma regra que dobra um valor
{
    "mimic_version": '1.0.0',
    "rule_type": '',
    "root": {
        "operation_type": 'math',
        "operation": '+',
        "arguments": [
        {
            "operation_type": "rule",
            "operation": "invoke"
            "arguments": [
                {
                    "operation_type": "external",
                    "operation": "get_by_id",
                    "arguments": [
                        "rules", "1"
                    ]
                },
                [5]
            ]
        },

        1

        ]
    }
} > 11


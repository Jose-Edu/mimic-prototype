# Rules de relationship
Não tem retorno, define valores de atributos da entidade

## Exemplos:

{
    "mimic-version": '1.0.0',
    "rule-type": 'relationship',
    "external": [
        {
            "resolve_method": "manual",
            "entity": "int",
            "internal_name": "XP"
        }
    ],
    "root": {
                "operation-type": 'relationship',
                "operation": 'set',
                "arguments": [
                    "attributes", // entity
                    [ // lista de campos definidos
                        [
                            "entity_attribute_entry", // tabela de entrada do valor

                            { // valor, no caso, define nível = xp/10
                                "operation-type": 'round',
                                "operation": 'round_down',
                                "arguments": [

                                    {
                                        "operation-type": 'math',
                                        "operation": '/',
                                        "arguments": [
                                            {
                                                "operation-type": 'external',
                                                "operation": 'get',
                                                "arguments": ["XP"]
                                            },
                                            10
                                        ]
                                    }

                                ]
                            }
                        ]
                    ]
                ]
    }
}
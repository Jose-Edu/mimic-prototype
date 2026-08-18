# Rules de action
Regra de ação, não tem retorno, tem efeito colateral

## Exemplos:
{
    "mimic-version": '1.0.0',
    "rule-type": 'action',
    "external": [
        {
            "entity": "sheets",
            "type_id": "1",
            "internal_name": "sheet1"
        },
        {
            "entity": "int",
            "internal_name": "atk"
        },
    ],
    "root": {
        "operation-type": 'action',
        "operation": '',
        "arguments": [

            {
                "operation-type": 'action',
                "operation": 'set',
                "arguments": [
                    
                ]
            }

        ]
    }
}
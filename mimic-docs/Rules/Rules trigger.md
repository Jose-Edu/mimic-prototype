

Regras de trigger para outras rules, executam o trigger quando a lógica retorna true.
Rules desse tipo sempre iniciam com um método trigger de um evento mimic em uma entity.
Esses métodos recebem uma entity e um boolean de validação

- on_use
- on_update
- on_create
- on_delete
- on_any

{
    "mimic-version": '1.0.0',
    "rule-type": 'trigger',
    "root": {
        "operation-type": 'trigger',
        "operation": 'on_any',
        "arguments": [
            {
                "operation_type": "external",
                "operation": "get",
                "arguments": [
                    "minhaEntidade"
                ]
            },
            true
        ]
    }
} executa o trigger em qualquer evento na entidade

{
    "mimic-version": '1.0.0',
    "rule-type": 'trigger',
    "root": {
        "operation-type": 'trigger',
        "operation": 'on_any',
        "arguments": [
            {
                "operation_type": "external",
                "operation": "get",
                "arguments": [
                    "minhaEntidade"
                ]
            },
            false
        ]
    }
} nunca executa o trigger

{
    "mimic-version": '1.0.0',
    "rule-type": 'trigger',
    "root": {
        "operation-type": 'trigger',
        "operation": 'on_any',
        "arguments": [
            {
                "operation_type": "external",
                "operation": "get",
                "arguments": [
                    "minhaEntidade"
                ]
            },

            {
                "operation-type": 'validation',
                "operation": '>',
                "arguments": [
                {
                    "operation_type": "external",
                    "operation": "get",
                    "arguments": [
                        "meuNum"
                    ]
                }, 
                5]
            }
        ]
    }
} executa o trigger em qualquer evento da entidade se o meuNum for maior que 5

[[Rules de validation]]
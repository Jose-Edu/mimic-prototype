# Rules entity use


## Rule:
- invoke: chama uma rule recebida [rule_id, rule_type, [args]]

### invoke:
considere id 1 como uma rule math que dobra um valor
{
    "mimic_version": '1.0.0',
    "rule_type": '',
    "external": []
    "root": {
        "operation_type": 'math',
        "operation": '+',
        "arguments": [
        {
            "operation_type": "rule",
            "operation": "invoke"
            "arguments": [
                1,
                "math",
                [5]
            ]
        },

        1

        ]
    }
} > 11
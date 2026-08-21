# Rules entity use


## Rule:

### invoke:
considere rule de id 1 como uma regra que dobra um valor
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
                {
                    "operation_type": "external",
                    "operation": "get_by_id",
                    "arguments": [
                        ["rules", "1"]
                    ]
                },
                [5]
            ]
        },

        1

        ]
    }
} > 11
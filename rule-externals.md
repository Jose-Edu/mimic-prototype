# Rules externals

considerando campo atk = 1

{
    "mimic-version": '1.0.0',
    "rule-type": '',
    "external": [
        {
            "entity": "sheets",
            "type-id": "1",
            "internal-name": "sheet1"
        }
    ]
    "root": {
        "operation-type": 'math',
        "operation": '+',
        "arguments": [
        {
            "operation-type": "external",
            "operation": "get-related",
            "arguments": [
                ["sheet1", "entity_attribute", "atk"]
            ],
            "external": "sheet1",
            "in": "attributes"
        },

        1

        ]
    }
} > 2

{
    "mimic-version": '1.0.0',
    "rule-type": '',
    "external": [
        {
            "entity": "globals",
            "internal-name": "global"
        }
    ]
    "root": {
        "operation-type": 'math',
        "operation": '+',
        "arguments": [
        {
            "operation-type": "external",
            "operation": "get",
            "arguments": [
                "global"
            ],
            "external": "sheet1",
            "in": "attributes"
        },

        1

        ]
    }
} > 2

considere rule de id 1 como uma regra que dobra um valor
{
    "mimic-version": '1.0.0',
    "rule-type": '',
    "external": []
    "root": {
        "operation-type": 'math',
        "operation": '+',
        "arguments": [
        {
            "operation-type": "external",
            "operation": "get-by-id",
            "arguments": [
                ["rules", "1"],
                [5]
            ],
            "external": "sheet1",
            "in": "attributes"
        },

        1

        ]
    }
} > 11


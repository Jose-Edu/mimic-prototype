# Rules externals

considerando campo atk = 1

{
    "mimic-version": '1.0.0',
    "rule-type": '',
    "external": [
        {
            "entity": "sheet",
            "type-id": "1"
            "internal-name": "sheet1"

        }
    ]
    "root": {
        "operation-type": 'math',
        "operation": '+',
        "arguments": [{
            "operation-type": "external",
            "operation": "get-external",
            "external": "sheet1",
            "in": "attributes"
        }]
    }
} > 2


A tabela `sheet_type_sheet_type` define a [[Rules/Rules|regra de relacionamento]] de sheet_type. Serve para aplicar regra que será usada em [[sheet_sheet]].

## Estrutura

| Nome da Coluna         | Tipo | Constraints               | Descrição                                      |
| ---------------------- | ---- | ------------------------- | ---------------------------------------------- |
| id_sheet_type_main     | uuid | PK, FK -> [[sheet_types]] | Tipo de ficha dona da rule.                    |
| id_sheet_type_children | uuid | PK, FK -> [[sheet_types]] | Ficha usada como parâmetro de entrada na rule. |
| id_relationship_rule   | uuid | FK -> [[rules]]           | Referência à regra associada.                  |


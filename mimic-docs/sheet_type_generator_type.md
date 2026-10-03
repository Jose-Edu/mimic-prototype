

A tabela `sheet_type_generator_type` registra quais sheet_types aplicam quais generator_types.

## Estrutura

| Nome da Coluna               | Tipo    | Constraints               | Descrição                                                        |
| ---------------------------- | ------- | ------------------------- | ---------------------------------------------------------------- |
| id_sheet_type_generator_type | uuid    | PK                        | Identificador único do registro desta tabela.                    |
| id_sheet_type                | uuid    | FK -> [[sheet_types]]     | Referência ao sheet_type.                                        |
| id_generator_type            | uuid    | FK -> [[generator_types]] | Referência ao generator_type.                                    |
| order                        | integer | -                         | Valor numérico usado para ordenar itens em sequências ou listas. |


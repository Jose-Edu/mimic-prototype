

A tabela `sheet_skill_attribute_entry` registra as entradas de valores de atributos de habilidades para cada ficha.

## Estrutura

| Nome da Coluna           | Tipo    | Constraints                  | Descrição                                     |
| ------------------------ | ------- | ---------------------------- | --------------------------------------------- |
| id_sheet_skill_attribute | uuid    | PK                           | Identificador único do registro desta tabela. |
| id_sheet_skill           | uuid    | FK -> [[sheet_skill]]        | Referência à ficha e à skill.                 |
| id_attribute             | uuid    | FK -> [[attributes]]         | Referência ao atributo relacionado.           |
| order                    | integer | -                            | Ordem de entrada do valor.                    |
| attribute_number         | number  | Nullable                     | Entrada de valor para caso de number.         |
| attribute_string         | varchar | Nullable                     | Entrada de valor para caso de string.         |
| attribute_boolean        | boolean | Nullable                     | Entrada de valor para caso de boolean.        |
| attribute_entity         | uuid    | Nullable, FK -> [[entities]] | Entrada de valor para caso de entity.         |


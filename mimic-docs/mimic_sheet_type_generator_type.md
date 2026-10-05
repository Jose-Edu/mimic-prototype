

A tabela `mimic_sheet_type_generator_type` registra quais sheet_types aplicam quais generator_types.

## Estrutura

| Nome da Coluna    | Tipo    | Constraints                     | Descrição                                          |
| ----------------- | ------- | ------------------------------- | -------------------------------------------------- |
| id                | uuid    | PK                              | Identificador único do registro desta tabela.      |
| id_sheet_type     | uuid    | FK -> [[mimic_sheet_types]]           | Referência ao sheet_type.                          |
| id_generator_type | uuid    | FK -> [[mimic_generator_types]] | Referência ao generator_type.                      |
| order             | integer | -                               | Ordem de inserção a nível de [[Rules/Rules\|Rule]] |

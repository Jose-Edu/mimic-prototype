

A tabela `mimic_action_type_generator_type` registra quais tipos de actions serão aplicados em cada tipo gerador.

## Estrutura

| Nome da Coluna    | Tipo | Constraints                   | Descrição        |
| ----------------- | ---- | ----------------------------- | ---------------- |
| id_action_type     | uuid | PK, FK -> [[mimic_action_types]]     | Tipo de action.   |
| id_generator_type | uuid | PK, FK -> [[mimic_generator_types]] | Tipo de gerador. |


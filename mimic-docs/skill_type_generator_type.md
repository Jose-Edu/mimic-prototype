

A tabela `skill_type_generator_type` registra quais tipos de skills serão aplicados em cada tipo gerador.

## Estrutura

| Nome da Coluna    | Tipo | Constraints                   | Descrição        |
| ----------------- | ---- | ----------------------------- | ---------------- |
| id_skill_type     | uuid | PK, FK -> [[skill_types]]     | Tipo de skill.   |
| id_generator_type | uuid | PK, FK -> [[generator_types]] | Tipo de gerador. |


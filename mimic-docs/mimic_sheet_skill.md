

A tabela `mimic_sheet_skill` registra quais fichas possuem quais skills.

## Estrutura

| Nome da Coluna | Tipo | Constraints      | Descrição                                     |
| -------------- | ---- | ---------------- | --------------------------------------------- |
| id             | uuid | PK               | Identificador único do registro desta tabela. |
| id_sheet       | uuid | FK -> [[mimic_sheets]] | Referência à ficha associada.                 |
| id_skill       | uuid | FK -> [[mimic_skills]] | Referência à habilidade relacionada.          |


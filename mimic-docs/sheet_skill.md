

A tabela `sheet_skill` registra quais fichas possuem quais skills.

## Estrutura

| Nome da Coluna | Tipo | Constraints      | Descrição                                     |
| -------------- | ---- | ---------------- | --------------------------------------------- |
| id_sheet_skill | uuid | PK               | Identificador único do registro desta tabela. |
| id_sheet       | uuid | FK -> [[sheets]] | Referência à ficha associada.                 |
| id_skill       | uuid | FK -> [[skills]] | Referência à habilidade relacionada.          |


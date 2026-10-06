

A tabela `mimic_sheet_action` registra quais fichas possuem quais actions.

## Estrutura

| Nome da Coluna | Tipo | Constraints      | Descrição                                     |
| -------------- | ---- | ---------------- | --------------------------------------------- |
| id             | uuid | PK               | Identificador único do registro desta tabela. |
| id_sheet       | uuid | FK -> [[mimic_sheets]] | Referência à ficha associada.                 |
| id_action       | uuid | FK -> [[mimic_actions]] | Referência à habilidade relacionada.          |




A tabela `sheet_group_sheet` registra o relacionamento N:N entre sheets e sheet_groups. Representa quais fichas estão em quais grupos.

## Estrutura

| Nome da Coluna | Tipo | Constraints                | Descrição                      |
| -------------- | ---- | -------------------------- | ------------------------------ |
| id_sheet_group | uuid | PK, FK -> [[sheet_groups]] | Referencia ao grupo associado. |
| id_sheet       | uuid | PK, FK -> [[sheets]]       | Referência à ficha associada.  |


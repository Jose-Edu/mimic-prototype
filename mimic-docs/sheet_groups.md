
A tabela `sheet_groups` registra o um grupo de [[sheets]], servindo para controlar party, um conjunto de itens e etc.

## Estrutura

| Nome da Coluna | Tipo    | Constraints            | Descrição                                     |
| -------------- | ------- | ---------------------- | --------------------------------------------- |
| id_sheet_group | uuid    | PK, FK -> [[entities]] | Identificador único do registro desta tabela. |
| name           | varchar | -                      | Nome do grupo.                                |


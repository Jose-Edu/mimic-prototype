
A tabela `mimic_sheet_groups` registra o um grupo de [[mimic_sheets]], servindo para controlar party, um conjunto de itens e etc.

## Estrutura

| Nome da Coluna | Tipo    | Constraints                  | Descrição                                     |
| -------------- | ------- | ---------------------------- | --------------------------------------------- |
| id             | uuid    | PK, FK -> [[mimic_entities]] | Identificador único do registro desta tabela. |
| name           | varchar | -                            | Nome do grupo.                                |




A tabela `mimic_sheet_sheet` organiza as entradas de dependências de [[Rules/Rules|Rules]] entre fichas.

## Estrutura

| Nome da Coluna    | Tipo    | Constraints      | Descrição                                     |
| ----------------- | ------- | ---------------- | --------------------------------------------- |
| id                | uuid    | PK               | Identificador único do registro desta tabela. |
| id_sheet_main     | uuid    | FK -> [[mimic_sheets]] | Ficha dona de rule.                           |
| id_sheet_children | uuid    | FK -> [[mimic_sheets]] | Ficha de parâmetro de entrada.                |
| order             | integer | -                | Ordem de entrada da dependência.              |



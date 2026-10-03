

A tabela `sheet_sheet` organiza as entradas de dependências de [[Rules/Rules|Rules]] entre fichas.

## Estrutura

| Nome da Coluna    | Tipo    | Constraints      | Descrição                                     |
| ----------------- | ------- | ---------------- | --------------------------------------------- |
| id_sheet_sheet    | uuid    | PK               | Identificador único do registro desta tabela. |
| id_sheet_main     | uuid    | FK -> [[sheets]] | Ficha dona de rule.                           |
| id_sheet_children | uuid    | FK -> [[sheets]] | Ficha de parâmetro de entrada.                |
| order             | integer | -                | Ordem de entrada da dependência.              |



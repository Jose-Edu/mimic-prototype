

A tabela `mimic_sheet_generator` registra quais geradores estão sendo aplicados na criação de uma ficha.

## Estrutura

| Nome da Coluna | Tipo    | Constraints                | Descrição                                               |
| -------------- | ------- | -------------------------- | ------------------------------------------------------- |
| id             | uuid    | PK                         | Identificador único do registro desta tabela.           |
| id_sheet       | uuid    | FK -> [[mimic_sheets]]           | Referência à ficha associada.                           |
| id_generator   | uuid    | FK -> [[mimic_generators]] | Referência ao gerador relacionado.                      |
| order          | integer | -                          | Ordem de aplicação na [[Rules/Rules\|Rule]] de geração. |


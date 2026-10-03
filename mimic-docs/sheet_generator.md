

A tabela `sheet_generator` registra quais geradores estão sendo aplicados na criação de uma ficha.

## Estrutura

| Nome da Coluna     | Tipo    | Constraints          | Descrição                                               |
| ------------------ | ------- | -------------------- | ------------------------------------------------------- |
| id_sheet_generator | uuid    | PK                   | Identificador único do registro desta tabela.           |
| id_sheet           | uuid    | FK -> [[sheets]]     | Referência à ficha associada.                           |
| id_generator       | uuid    | FK -> [[generators]] | Referência ao gerador relacionado.                      |
| order              | integer | -                    | Ordem de aplicação na [[Rules/Rules\|Rule]] de geração. |


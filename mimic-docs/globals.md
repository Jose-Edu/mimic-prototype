

A tabela `globals` registram os atributos globais do sistema. Usado para registrar valores de controle geral que não se aplica a uma ficha em expecífico.

## Estrutura

| Nome da Coluna | Tipo    | Constraints            | Descrição                                     |
| -------------- | ------- | ---------------------- | --------------------------------------------- |
| id_global      | uuid    | PK, FK -> [[entities]] | Identificador único do registro desta tabela. |
| id_attribute   | uuid    | FK -> [[attributes]]   | Atributo da global.                           |
| name           | varchar | -                      | Nome da global.                               |



A tabela `mimic_globals` registram os atributos globais do sistema. Usado para registrar valores de controle geral que não se aplica a uma ficha em expecífico.

## Estrutura

| Nome da Coluna | Tipo    | Constraints                  | Descrição                                     |
| -------------- | ------- | ---------------------------- | --------------------------------------------- |
| id             | uuid    | PK, FK -> [[mimic_entities]] | Identificador único do registro desta tabela. |
| id_attribute   | uuid    | FK -> [[mimic_attributes]]   | Atributo da global.                           |
| name           | varchar | -                            | Nome da global.                               |

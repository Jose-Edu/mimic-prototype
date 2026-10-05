

A tabela `mimic_tags` registra as tags do sistema. Tags são marcações que servem para categorizar entidade a nível de metadados ou até como dado de controle em [[Rules/Rules|Rules]].

## Estrutura

| Nome da Coluna | Tipo    | Constraints             | Descrição                                     |
| -------------- | ------- | ----------------------- | --------------------------------------------- |
| id             | uuid    | PK                      | Identificador único do registro desta tabela. |
| id_system      | uuid    | FK -> [[mimic_systems]] | Sistema no qual a tag está.                   |
| name           | varchar | -                       | Nome da tag.                                  |

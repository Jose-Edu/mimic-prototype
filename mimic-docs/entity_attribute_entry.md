

A tabela `entity_attribute_entry` registra o valor atual de um atributo de uma entidade. Cada relacionamento pode ter mais de uma entrada, dependendo da estrutura.

## Estrutura

| Nome da Coluna            | Tipo    | Constraints                  | Descrição                                                                          |
| ------------------------- | ------- | ---------------------------- | ---------------------------------------------------------------------------------- |
| id_entity_attribute_entry | uuid    | PK                           | Identificador único do registro desta tabela.                                      |
| order                     | integer | Default 1                    | Número de prioridade para aplicar na estrutura, como explicado em [[value_types]]. |
| id_entity_attribute       | uuid    | FK -> [[entity_attribute]]   | Refêrencia ao relacionamento no qual essa entrada se aplica.                       |
| attribute_number          | number  | Nullable                     | Valor a ser aplicado em caso do tipo de valor ser number.                          |
| attribute_string          | varchar | Nullable                     | Valor a ser aplicado em caso do tipo de valor ser string.                          |
| attribute_boolean         | boolean | Nullable                     | Valor a ser aplicado em caso do tipo de valor ser boolean.                         |
| attribute_entity          | uuid    | Nullable, FK -> [[entities]] | Valor a ser aplicado em caso do tipo de valor ser entity.                          |

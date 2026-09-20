

A tabela `attribute_items` define sub atributos, usados internamente na geração de valores de [[attributes]]

## Estrutura

| Nome da Coluna          | Tipo    | Constraints            | Descrição                                                                   |
| ----------------------- | ------- | ---------------------- | --------------------------------------------------------------------------- |
| id_attribute_item       | uuid    | PK, FK -> [[entities]] | Identificador único do registro desta tabela.                               |
| id_attribute_composer   | uuid    | FK -> [[attributes]]   | Sub atributo interno.                                                       |
| id_attribute_composable | uuid    | FK -> [[attributes]]   | Atributo pai.                                                               |
| name                    | varchar | -                      | Nome descritivo do registro, usado para identificação humana e organização. |

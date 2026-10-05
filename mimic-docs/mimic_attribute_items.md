

A tabela `mimic_attribute_items` define sub atributos, usados internamente na geração de valores de [[mimic_attributes]]

## Estrutura

| Nome da Coluna          | Tipo    | Constraints            | Descrição                                                                   |
| ----------------------- | ------- | ---------------------- | --------------------------------------------------------------------------- |
| id                      | uuid    | PK, FK -> [[mimic_entities]] | Identificador único do registro desta tabela.                               |
| id_attribute_composer   | uuid    | FK -> [[mimic_attributes]]   | Sub atributo interno.                                                       |
| id_attribute_composable | uuid    | FK -> [[mimic_attributes]]   | Atributo pai.                                                               |
| name                    | varchar | -                      | Nome descritivo do registro, usado para identificação humana e organização. |

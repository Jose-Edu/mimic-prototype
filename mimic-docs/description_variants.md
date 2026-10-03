

A tabela `description_variants` define as variantes de descrições usadas no sistema, ex: "Português", "Inglês" e etc.

## Estrutura

| Nome da Coluna              | Tipo    | Constraints                         | Descrição                                                                   |
| --------------------------- | ------- | ----------------------------------- | --------------------------------------------------------------------------- |
| id_description_variant      | uuid    | PK                                  | Identificador único do registro desta tabela.                               |
| id_description_variant_type | uuid    | FK -> [[description_variant_types]] | Referência ao tipo de elemento.                                             |
| name                        | varchar | -                                   | Nome descritivo do registro, usado para identificação humana e organização. |

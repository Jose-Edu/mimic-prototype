

A tabela `description_variants` define as variantes de descrições usadas no sistema, ex: "Título", "Descrição principal" e etc.

## Estrutura

| Nome da Coluna              | Tipo    | Constraints                         | Descrição                                                                   |
| --------------------------- | ------- | ----------------------------------- | --------------------------------------------------------------------------- |
| id_description_variant      | integer | PK                                  | Identificador único do registro desta tabela.                               |
| id_description_variant_type | integer | FK -> [[description_variant_types]] | Referência ao tipo de elemento.                                             |
| name                        | varchar | -                                   | Nome descritivo do registro, usado para identificação humana e organização. |

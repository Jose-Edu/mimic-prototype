---
type: database_table
tags:
  - db
  - table
  - mimic
  - description_variants
  - descriptions
system_domain: Descrição e narrativa
---

# Tabela: description_variants

A tabela `description_variants` define as variantes de descrições usadas no sistema, ex: "Título", "Descrição principal" e etc.

## Estrutura

| Nome da Coluna              | Tipo    | Constraints                         | Descrição                                                                   |
| --------------------------- | ------- | ----------------------------------- | --------------------------------------------------------------------------- |
| id_description_variant      | integer | PK                                  | Identificador único do registro desta tabela.                               |
| id_description_variant_type | integer | FK -> [[description_variant_types]] | Referência ao tipo de elemento.                                             |
| name                        | varchar | -                                   | Nome descritivo do registro, usado para identificação humana e organização. |

## Relacionamentos

- Outward Links: [[description_variant_types]]
- Inward Links: [[descriptions]]

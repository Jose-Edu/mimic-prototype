---
type: database_table
tags:
  - db
  - table
  - mimic
  - description_variant_types
  - descriptions
system_domain: Descrição e narrativa
---

# Tabela: description_variant_types

A tabela `description_variant_types` define os tipos de descrições usadas no sistema, ex: "Versão principal", "Versão curta" e etc.
## Estrutura

| Nome da Coluna              | Tipo    | Constraints       | Descrição                                          |
| --------------------------- | ------- | ----------------- | -------------------------------------------------- |
| id_description_variant_type | integer | PK                | Identificador único do registro desta tabela.      |
| id_system                   | integer | FK -> [[systems]] | Referência ao sistema ao qual o registro pertence. |
| name                        | varchar | -                 | Nome do tipo.                                      |

## Relacionamentos

- Outward Links: [[systems]]
- Inward Links: [[description_variants]]

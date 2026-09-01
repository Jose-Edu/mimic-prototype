---
type: database_table
tags: [db, table, mimic, description_variant_types]
system_domain: "Descrição e narrativa"
---

# Tabela: description_variant_types

A tabela `description_variant_types` organiza a parte do modelo de dados responsável por o comportamento e a persistência de description variant types no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_description_variant_type | integer | PK | Referência ao tipo de elemento. |
| id_system | integer | FK -> [[systems]] | Referência ao sistema ao qual o registro pertence. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |

## Relacionamentos

- Outward Links: [[systems]]
- Inward Links: [[description_variants]]

---
type: database_table
tags: [db, table, mimic, description_variants]
system_domain: "Descrição e narrativa"
---

# Tabela: description_variants

A tabela `description_variants` organiza a parte do modelo de dados responsável por o comportamento e a persistência de description variants no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_description_variant | integer | PK | Chave estrangeira para a tabela relacionada. |
| id_description_variant_type | integer | FK -> [[description_variant_types]] | Referência ao tipo de elemento. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |

## Relacionamentos

- Outward Links: [[description_variant_types]]
- Inward Links: [[descriptions]]

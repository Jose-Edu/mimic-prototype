---
type: database_table
tags: [db, table, mimic, sheet_types]
system_domain: "Fichas e mapas"
---

# Tabela: sheet_types

A tabela `sheet_types` organiza a parte do modelo de dados responsável por o comportamento e a persistência de sheet types no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_sheet_type | integer | PK, FK -> [[entities]] | Referência ao tipo de elemento. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |
| id_validation_rule | integer | FK -> [[rules]] | Referência à regra associada. |
| id_compose_rule | integer | FK -> [[rules]] | Referência à regra associada. |
| id_base_generator | interger // (optional) | FK -> [[generators]] | Referência ao gerador relacionado. |

## Relacionamentos

- Outward Links: [[entities]], [[rules]], [[rules]], [[generators]]
- Inward Links: [[sheets]], [[sheet_type_generator_type]], [[sheet_type_sheet_type]], [[sheet_type_sheet_type]]

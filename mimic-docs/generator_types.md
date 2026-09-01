---
type: database_table
tags: [db, table, mimic, generator_types]
system_domain: "Geradores"
---

# Tabela: generator_types

A tabela `generator_types` organiza a parte do modelo de dados responsável por o comportamento e a persistência de generator types no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_generator_type | integer | PK, FK -> [[entities]] | Referência ao tipo de elemento. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |
| id_validation_rule | integer | FK -> [[rules]] | Referência à regra associada. |
| id_compose_rule | integer | FK -> [[rules]] | Referência à regra associada. |

## Relacionamentos

- Outward Links: [[entities]], [[rules]], [[rules]]
- Inward Links: [[generator_type_steps]], [[generators]], [[sheet_type_generator_type]], [[skill_type_generator_type]]

---
type: database_table
tags: [db, table, mimic, sheet_type_sheet_type]
system_domain: "Fichas e mapas"
---

# Tabela: sheet_type_sheet_type

A tabela `sheet_type_sheet_type` organiza a parte do modelo de dados responsável por o comportamento e a persistência de sheet type sheet type no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_sheet_type_main | integer | PK, FK -> [[sheet_types]] | Chave estrangeira para a tabela relacionada. |
| id_sheet_type_children | integer | PK, FK -> [[sheet_types]] | Chave estrangeira para a tabela relacionada. |
| id_relationship_rule | integer | FK -> [[rules]] | Referência à regra associada. |

## Relacionamentos

- Outward Links: [[sheet_types]], [[sheet_types]], [[rules]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

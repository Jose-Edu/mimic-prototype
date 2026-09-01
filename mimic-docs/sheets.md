---
type: database_table
tags: [db, table, mimic, sheets]
system_domain: "Fichas e mapas"
---

# Tabela: sheets

A tabela `sheets` organiza a parte do modelo de dados responsável por o comportamento e a persistência de sheets no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_sheet | integer | PK, FK -> [[entities]] | Referência à ficha associada. |
| id_sheet_type | integer | FK -> [[sheet_types]] | Referência ao tipo de elemento. |

## Relacionamentos

- Outward Links: [[entities]], [[sheet_types]]
- Inward Links: [[sheet_group_sheet]], [[map_token]], [[sheet_generator]], [[sheet_skill]], [[sheet_sheet]], [[sheet_sheet]]

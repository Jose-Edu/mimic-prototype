---
type: database_table
tags: [db, table, mimic, sheet_skill]
system_domain: "Fichas e mapas"
---

# Tabela: sheet_skill

A tabela `sheet_skill` organiza a parte do modelo de dados responsável por o comportamento e a persistência de sheet skill no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_sheet_skill | integer | PK | Referência à habilidade relacionada. |
| id_sheet | integer | FK -> [[sheets]] | Referência à ficha associada. |
| id_skill | integer | FK -> [[skills]] | Referência à habilidade relacionada. |

## Relacionamentos

- Outward Links: [[sheets]], [[skills]]
- Inward Links: [[sheet_skill_attribute]]

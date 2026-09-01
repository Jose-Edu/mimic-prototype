---
type: database_table
tags: [db, table, mimic, sheet_groups]
system_domain: "Fichas e mapas"
---

# Tabela: sheet_groups

A tabela `sheet_groups` organiza a parte do modelo de dados responsável por o comportamento e a persistência de sheet groups no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_sheet_group | integer | PK, FK -> [[entities]] | Chave estrangeira para a tabela relacionada. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |

## Relacionamentos

- Outward Links: [[entities]]
- Inward Links: [[sheet_group_sheet]]

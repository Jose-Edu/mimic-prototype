---
type: database_table
tags: [db, table, mimic, sheet_group_sheet]
system_domain: "Fichas e mapas"
---

# Tabela: sheet_group_sheet

A tabela `sheet_group_sheet` organiza a parte do modelo de dados responsável por o comportamento e a persistência de sheet group sheet no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_sheet_group | integer | PK, FK -> [[sheet_groups]] | Chave estrangeira para a tabela relacionada. |
| id_sheet | integer | PK, FK -> [[sheets]] | Referência à ficha associada. |

## Relacionamentos

- Outward Links: [[sheet_groups]], [[sheets]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

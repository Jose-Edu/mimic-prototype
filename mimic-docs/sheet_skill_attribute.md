---
type: database_table
tags: [db, table, mimic, sheet_skill_attribute]
system_domain: "Fichas e mapas"
---

# Tabela: sheet_skill_attribute

A tabela `sheet_skill_attribute` organiza a parte do modelo de dados responsável por o comportamento e a persistência de sheet skill attribute no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_sheet_skill_attribute | integer | PK | Referência ao atributo relacionado. |
| id_sheet_skill | integer | FK -> [[sheet_skill]] | Referência à habilidade relacionada. |
| id_attribute | integer | FK -> [[attributes]] | Referência ao atributo relacionado. |
| attribute_entry | text | — | Campo textual ou estrutural usado para armazenar a lógica, entrada ou valor padrão. |
| order | integer | — | Valor numérico usado para ordenar itens em sequências ou listas. |

## Relacionamentos

- Outward Links: [[sheet_skill]], [[attributes]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

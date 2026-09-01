---
type: database_table
tags: [db, table, mimic, sheet_sheet]
system_domain: "Fichas e mapas"
---

# Tabela: sheet_sheet

A tabela `sheet_sheet` organiza a parte do modelo de dados responsável por o comportamento e a persistência de sheet sheet no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_sheet_sheet | integer | PK | Referência à ficha associada. |
| id_sheet_main | integer | FK -> [[sheets]] | Chave estrangeira para a tabela relacionada. |
| id_sheet_children | integer | FK -> [[sheets]] | Chave estrangeira para a tabela relacionada. |
| order | integer | — | Valor numérico usado para ordenar itens em sequências ou listas. |

## Relacionamentos

- Outward Links: [[sheets]], [[sheets]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

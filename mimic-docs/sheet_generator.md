---
type: database_table
tags: [db, table, mimic, sheet_generator]
system_domain: "Fichas e mapas"
---

# Tabela: sheet_generator

A tabela `sheet_generator` organiza a parte do modelo de dados responsável por o comportamento e a persistência de sheet generator no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_sheet_generator | integer | PK | Referência ao gerador relacionado. |
| id_sheet | integer | FK -> [[sheets]] | Referência à ficha associada. |
| id_generator | integer | FK -> [[generators]] | Referência ao gerador relacionado. |
| order | integer | — | Valor numérico usado para ordenar itens em sequências ou listas. |

## Relacionamentos

- Outward Links: [[sheets]], [[generators]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

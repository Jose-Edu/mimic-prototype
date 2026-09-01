---
type: database_table
tags: [db, table, mimic, sheet_type_generator_type]
system_domain: "Fichas e mapas"
---

# Tabela: sheet_type_generator_type

A tabela `sheet_type_generator_type` organiza a parte do modelo de dados responsável por o comportamento e a persistência de sheet type generator type no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_sheet_type_generator_type | integer | PK | Referência ao tipo de elemento. |
| id_sheet_type | integer | FK -> [[sheet_types]] | Referência ao tipo de elemento. |
| id_generator_type | integer | FK -> [[generator_types]] | Referência ao tipo de elemento. |
| order | integer | — | Valor numérico usado para ordenar itens em sequências ou listas. |

## Relacionamentos

- Outward Links: [[sheet_types]], [[generator_types]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

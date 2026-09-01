---
type: database_table
tags: [db, table, mimic, entity_attribute_entry]
system_domain: "Atributos e valores"
---

# Tabela: entity_attribute_entry

A tabela `entity_attribute_entry` organiza a parte do modelo de dados responsável por o comportamento e a persistência de entity attribute entry no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_entity_attribute_entry | integer | FK -> [[entity_attribute]] | Chave estrangeira para a tabela relacionada. |
| attribute_entry | text | — | Campo textual ou estrutural usado para armazenar a lógica, entrada ou valor padrão. |
| order | integer | — | Valor numérico usado para ordenar itens em sequências ou listas. |

## Relacionamentos

- Outward Links: [[entity_attribute]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

---
type: database_table
tags: [db, table, mimic, generator_step_skill_attribute]
system_domain: "Geradores"
---

# Tabela: generator_step_skill_attribute

A tabela `generator_step_skill_attribute` organiza a parte do modelo de dados responsável por o comportamento e a persistência de generator step skill attribute no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_generator_step_skill_attribute | integer | PK | Referência ao atributo relacionado. |
| id_generator_step_skill | integer | FK -> [[generator_step_skill]] | Referência à habilidade relacionada. |
| id_attribute | integer | FK -> [[attributes]] | Referência ao atributo relacionado. |
| attribute_entry | text | — | Campo textual ou estrutural usado para armazenar a lógica, entrada ou valor padrão. |
| order | integer | — | Valor numérico usado para ordenar itens em sequências ou listas. |

## Relacionamentos

- Outward Links: [[generator_step_skill]], [[attributes]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

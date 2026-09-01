---
type: database_table
tags: [db, table, mimic, rules]
system_domain: "Regras e mecânicas"
---

# Tabela: rules

A tabela `rules` organiza a parte do modelo de dados responsável por o comportamento e a persistência de rules no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_rule | integer | PK, FK -> [[entities]] | Referência à regra associada. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |
| type | enum("math", "validation", "action", "relationship", "trigger") | enum | Categoria ou enumeração que define a semântica do dado em uso. |
| id_trigger_rule | integer | nullable, FK -> [[rules]] | Referência à regra associada. |
| rule | jsonb /*ast*/ | — | Campo textual ou estrutural usado para armazenar a lógica, entrada ou valor padrão. |

## Relacionamentos

- Outward Links: [[entities]], [[rules]]
- Inward Links: [[sheet_types]], [[sheet_types]], [[generator_types]], [[generator_types]], [[generator_type_steps]], [[skill_types]], [[skills]], [[rules]], [[rule_entity]], [[rngs]], [[attributes]], [[tests]], [[game_states]], [[game_states]], [[sheet_type_sheet_type]]

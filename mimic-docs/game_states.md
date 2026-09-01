---
type: database_table
tags: [db, table, mimic, game_states]
system_domain: "Regras e mecânicas"
---

# Tabela: game_states

A tabela `game_states` organiza a parte do modelo de dados responsável por o comportamento e a persistência de game states no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_game_state | integer | PK, FK -> [[entities]] | Referência ao estado de jogo atual. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |
| turn_count_rule_id | integer | FK -> [[rules]] | Regra relacionada ao controle de turnos e ordem do jogo. |
| turn_order_rule_id | integer | FK -> [[rules]] | Regra relacionada ao controle de turnos e ordem do jogo. |

## Relacionamentos

- Outward Links: [[entities]], [[rules]], [[rules]]
- Inward Links: [[access]]

---
type: database_table
tags: [db, table, mimic, access]
system_domain: "Usuários, entidades e permissões"
---

# Tabela: access

A tabela `access` organiza a parte do modelo de dados responsável por o comportamento e a persistência de access no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_access | integer | PK, FK -> [[entities]] | Identificador único do registro desta tabela. |
| id_entity_to_access | integer | nullable, FK -> [[entities]] | Chave estrangeira para a tabela relacionada. |
| id_game_state | integer | nullable, FK -> [[game_states]] | Referência ao estado de jogo atual. |
| scope | enum("self", "same", "other") | enum | Categoria ou enumeração que define a semântica do dado em uso. |
| can_read | boolean | boolean | Flag booleana que indica o comportamento ou estado permitido do registro. |
| can_use | boolean | boolean | Flag booleana que indica o comportamento ou estado permitido do registro. |
| can_update | boolean | boolean | Flag booleana que indica o comportamento ou estado permitido do registro. |
| can_create | boolean | boolean | Flag booleana que indica o comportamento ou estado permitido do registro. |
| can_delete | boolean | boolean | Flag booleana que indica o comportamento ou estado permitido do registro. |
| can_overwrite | boolean | boolean | Flag booleana que indica o comportamento ou estado permitido do registro. |

## Relacionamentos

- Outward Links: [[entities]], [[game_states]], [[entities]]
- Inward Links: [[role_access]]

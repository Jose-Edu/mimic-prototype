---
type: database_table
tags: [db, table, mimic, entities]
system_domain: "Usuários, entidades e permissões"
---

# Tabela: entities

A tabela `entities` organiza a parte do modelo de dados responsável por o comportamento e a persistência de entities no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_entity | integer | PK | Referência à entidade que representa este registro. |
| created_at | timestamp | — | Registro de data e hora de criação ou atualização do item. |
| updated_at | timestamp | — | Registro de data e hora de criação ou atualização do item. |
| id_system | integer | FK -> [[systems]] | Referência ao sistema ao qual o registro pertence. |
| id_creator_user | integer | FK -> [[users]] | Referência ao usuário relacionado. |
| id_overrides_entity | integer | nullable, FK -> [[entities]] | Referência à entidade que representa este registro. |
| table_name | varchar /*ex: generators, rules, roles etc*/ | — | Campo de dados usado para armazenar o valor ou vínculo associado ao registro. |
| is_active | bool | — | Flag booleana que indica o comportamento ou estado permitido do registro. |

## Relacionamentos

- Outward Links: [[entities]], [[users]], [[systems]]
- Inward Links: [[roles]], [[access]], [[access]], [[sheet_types]], [[sheets]], [[sheet_groups]], [[generator_types]], [[generator_type_steps]], [[generators]], [[generator_steps]], [[skill_types]], [[skills]], [[rules]], [[rule_entity]], [[rngs]], [[attributes]], [[entity_attribute]], [[globals]], [[tests]], [[game_states]], [[tag_entity]], [[entities]], [[maps]], [[descriptions]]

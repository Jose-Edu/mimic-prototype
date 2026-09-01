---
type: database_table
tags: [db, table, mimic, generator_step_skill]
system_domain: "Geradores"
---

# Tabela: generator_step_skill

A tabela `generator_step_skill` organiza a parte do modelo de dados responsável por o comportamento e a persistência de generator step skill no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_generator_step_skill | integer | PK | Referência à habilidade relacionada. |
| id_generator_step | integer | FK -> [[generator_steps]] | Chave estrangeira para a tabela relacionada. |
| id_skill | integer | FK -> [[skills]] | Referência à habilidade relacionada. |

## Relacionamentos

- Outward Links: [[generator_steps]], [[skills]]
- Inward Links: [[generator_step_skill_attribute]]

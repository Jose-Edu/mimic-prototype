---
type: database_table
tags: [db, table, mimic, skills]
system_domain: "Habilidades"
---

# Tabela: skills

A tabela `skills` organiza a parte do modelo de dados responsável por o comportamento e a persistência de skills no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_skill | integer | PK, FK -> [[entities]] | Referência à habilidade relacionada. |
| id_skill_type | integer | FK -> [[skill_types]] | Referência ao tipo de elemento. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |
| id_action_rule | integer | FK -> [[rules]] | Referência à regra associada. |

## Relacionamentos

- Outward Links: [[entities]], [[skill_types]], [[rules]]
- Inward Links: [[generator_step_skill]], [[sheet_skill]]

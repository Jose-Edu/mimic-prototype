---
type: database_table
tags: [db, table, mimic, tags]
system_domain: "Usuários, entidades e permissões"
---

# Tabela: tags

A tabela `tags` organiza a parte do modelo de dados responsável por o comportamento e a persistência de tags no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_tag | integer | PK | Chave estrangeira para a tabela relacionada. |
| id_system | integer | FK -> [[systems]] | Referência ao sistema ao qual o registro pertence. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |

## Relacionamentos

- Outward Links: [[systems]]
- Inward Links: [[tag_entity]]

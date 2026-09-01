---
type: database_table
tags: [db, table, mimic, tag_entity]
system_domain: "Usuários, entidades e permissões"
---

# Tabela: tag_entity

A tabela `tag_entity` organiza a parte do modelo de dados responsável por o comportamento e a persistência de tag entity no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_tag | integer | PK, FK -> [[tags]] | Chave estrangeira para a tabela relacionada. |
| id_entity | integer | PK, FK -> [[entities]] | Referência à entidade que representa este registro. |

## Relacionamentos

- Outward Links: [[tags]], [[entities]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

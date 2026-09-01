---
type: database_table
tags: [db, table, mimic, user_role]
system_domain: "Usuários, entidades e permissões"
---

# Tabela: user_role

A tabela `user_role` organiza a parte do modelo de dados responsável por o comportamento e a persistência de user role no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_user | integer | PK, FK -> [[users]] | Referência ao usuário relacionado. |
| id_role | integer | PK, FK -> [[roles]] | Referência ao papel ou função vinculada. |

## Relacionamentos

- Outward Links: [[users]], [[roles]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

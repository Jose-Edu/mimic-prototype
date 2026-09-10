---
type: database_table
tags: [db, table, mimic, users]
system_domain: "Usuários, entidades e permissões"
---

# Tabela: users

A tabela `users` organiza a parte do modelo de dados responsável por o comportamento e a persistência de users no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_user | integer | — | Referência ao usuário relacionado. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |

## Relacionamentos

- Outward Links: Nenhuma referência direta a outras tabelas.
- Inward Links: [[user_system]], [[user_role]], [[systems]], [[entities]]

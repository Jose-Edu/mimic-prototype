---
type: database_table
tags: [db, table, mimic, roles]
system_domain: "Usuários, entidades e permissões"
---

# Tabela: roles

A tabela `roles` organiza a parte do modelo de dados responsável por o comportamento e a persistência de roles no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_role | integer | PK, FK -> [[entities]] | Referência ao papel ou função vinculada. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |
| is_default | bool | boolean | Flag booleana que indica o comportamento ou estado permitido do registro. |
| roleless_add | bool | boolean | Flag booleana que indica o comportamento ou estado permitido do registro. |

## Relacionamentos

- Outward Links: [[entities]]
- Inward Links: [[user_role]], [[role_access]]

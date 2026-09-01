---
type: database_table
tags: [db, table, mimic, user_system]
system_domain: "Usuários, entidades e permissões"
---

# Tabela: user_system

A tabela `user_system` organiza a parte do modelo de dados responsável por o comportamento e a persistência de user system no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_user | integer | PK, FK -> [[users]] | Referência ao usuário relacionado. |
| id_system | integer | PK, FK -> [[systems]] | Referência ao sistema ao qual o registro pertence. |

## Relacionamentos

- Outward Links: [[users]], [[systems]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

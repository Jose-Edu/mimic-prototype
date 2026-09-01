---
type: database_table
tags: [db, table, mimic, role_access]
system_domain: "Usuários, entidades e permissões"
---

# Tabela: role_access

A tabela `role_access` organiza a parte do modelo de dados responsável por o comportamento e a persistência de role access no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_access | integer | PK, FK -> [[access]] | Chave estrangeira para a tabela relacionada. |
| id_role | integer | PK, FK -> [[roles]] | Referência ao papel ou função vinculada. |

## Relacionamentos

- Outward Links: [[roles]], [[access]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

---
type: database_table
tags: [db, table, mimic, tests]
system_domain: "Regras e mecânicas"
---

# Tabela: tests

A tabela `tests` organiza a parte do modelo de dados responsável por o comportamento e a persistência de tests no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_test | integer | PK, FK -> [[entities]] | Referência ao teste ou caso de validação. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |
| id_rule | integer | FK -> [[rules]] | Referência à regra associada. |

## Relacionamentos

- Outward Links: [[entities]], [[rules]]
- Inward Links: [[test_rng]]

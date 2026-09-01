---
type: database_table
tags: [db, table, mimic, test_rng]
system_domain: "Regras e mecânicas"
---

# Tabela: test_rng

A tabela `test_rng` organiza a parte do modelo de dados responsável por o comportamento e a persistência de test rng no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_test | integer | PK, FK -> [[tests]] | Referência ao teste ou caso de validação. |
| id_rng | integer | PK, FK -> [[rngs]] | Referência ao gerador aleatório relacionado. |

## Relacionamentos

- Outward Links: [[tests]], [[rngs]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

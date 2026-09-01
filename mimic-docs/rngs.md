---
type: database_table
tags: [db, table, mimic, rngs]
system_domain: "Regras e mecânicas"
---

# Tabela: rngs

A tabela `rngs` organiza a parte do modelo de dados responsável por o comportamento e a persistência de rngs no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_rng | integer | PK, FK -> [[entities]] | Referência ao gerador aleatório relacionado. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |
| id_filter_rule | integer | nullable, FK -> [[rules]] | Referência à regra associada. |
| expected_value | integer | nullable | Metadado de versão, hash ou valor esperado do sistema ou módulo. |
| generator_start | integer | nullable | Parâmetros do gerador aleatório ou de sequência. |
| generator_end | integer | — | Parâmetros do gerador aleatório ou de sequência. |
| generator_step | integer | nullable | Parâmetros do gerador aleatório ou de sequência. |
| cached_values | integer | array | Campo de dados usado para armazenar o valor ou vínculo associado ao registro. |

## Relacionamentos

- Outward Links: [[entities]], [[rules]]
- Inward Links: [[test_rng]]

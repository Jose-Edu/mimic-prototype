---
type: database_table
tags: [db, table, mimic, rule_entity]
system_domain: "Regras e mecânicas"
---

# Tabela: rule_entity

A tabela `rule_entity` organiza a parte do modelo de dados responsável por o comportamento e a persistência de rule entity no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_rule | integer | PK, FK -> [[rules]] | Referência à regra associada. |
| id_entity | integer | PK, FK -> [[entities]] | Referência à entidade que representa este registro. |
| resolve_method | enum("manual", "context") | enum | Campo de dados usado para armazenar o valor ou vínculo associado ao registro. |
| value_type | enum("entity", "int", "float", "string", "bool") | enum | Categoria ou enumeração que define a semântica do dado em uso. |
| internal_name | varchar | — | Campo textual ou estrutural usado para armazenar a lógica, entrada ou valor padrão. |

## Relacionamentos

- Outward Links: [[rules]], [[entities]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

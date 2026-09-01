---
type: database_table
tags: [db, table, mimic, skill_type_generator_type]
system_domain: "Habilidades"
---

# Tabela: skill_type_generator_type

A tabela `skill_type_generator_type` organiza a parte do modelo de dados responsável por o comportamento e a persistência de skill type generator type no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_skill_type | integer | PK, FK -> [[skill_types]] | Referência ao tipo de elemento. |
| id_generator_type | integer | PK, FK -> [[generator_types]] | Referência ao tipo de elemento. |

## Relacionamentos

- Outward Links: [[skill_types]], [[generator_types]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

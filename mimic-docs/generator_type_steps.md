---
type: database_table
tags: [db, table, mimic, generator_type_steps]
system_domain: "Geradores"
---

# Tabela: generator_type_steps

A tabela `generator_type_steps` organiza a parte do modelo de dados responsável por o comportamento e a persistência de generator type steps no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_generator_type_step | integer | PK, FK -> [[entities]] | Chave estrangeira para a tabela relacionada. |
| id_generator_type | integer | FK -> [[generator_types]] | Referência ao tipo de elemento. |
| id_validation_rule | integer | FK -> [[rules]] | Referência à regra associada. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |

## Relacionamentos

- Outward Links: [[entities]], [[generator_types]], [[rules]]
- Inward Links: [[generator_steps]]

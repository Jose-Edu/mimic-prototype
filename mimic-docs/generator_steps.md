---
type: database_table
tags: [db, table, mimic, generator_steps]
system_domain: "Geradores"
---

# Tabela: generator_steps

A tabela `generator_steps` organiza a parte do modelo de dados responsável por o comportamento e a persistência de generator steps no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_generator_step | integer | PK, FK -> [[entities]] | Chave estrangeira para a tabela relacionada. |
| id_generator | integer | FK -> [[generators]] | Referência ao gerador relacionado. |
| id_generator_type_step | integer | FK -> [[generator_type_steps]] | Chave estrangeira para a tabela relacionada. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |

## Relacionamentos

- Outward Links: [[entities]], [[generators]], [[generator_type_steps]]
- Inward Links: [[generator_step_skill]]

---
type: database_table
tags: [db, table, mimic, generators]
system_domain: "Geradores"
---

# Tabela: generators

A tabela `generators` organiza a parte do modelo de dados responsável por o comportamento e a persistência de generators no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_generator | integer | PK, FK -> [[entities]] | Referência ao gerador relacionado. |
| id_generator_type | integer | FK -> [[generator_types]] | Referência ao tipo de elemento. |
| id_super_generator | integer /* nullable */ | nullable, FK -> [[generators]] | Referência ao gerador relacionado. |
| is_children | boolean | — | Flag booleana que indica o comportamento ou estado permitido do registro. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |

## Relacionamentos

- Outward Links: [[entities]], [[generator_types]], [[generators]]
- Inward Links: [[sheet_types]], [[generators]], [[generator_steps]], [[sheet_generator]]

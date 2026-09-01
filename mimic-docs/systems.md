---
type: database_table
tags: [db, table, mimic, systems]
system_domain: "Usuários, entidades e permissões"
---

# Tabela: systems

A tabela `systems` organiza a parte do modelo de dados responsável por o comportamento e a persistência de systems no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_system | integer | PK | Referência ao sistema ao qual o registro pertence. |
| mimic_version | varchar | — | Metadado de versão, hash ou valor esperado do sistema ou módulo. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |
| system_version | varchar | — | Metadado de versão, hash ou valor esperado do sistema ou módulo. |
| id_author_user | integer | FK -> [[users]] | Referência ao usuário relacionado. |
| system_hash | varchar | — | Metadado de versão, hash ou valor esperado do sistema ou módulo. |
| created_at | timestamp | — | Registro de data e hora de criação ou atualização do item. |
| updated_at | timestamp | — | Registro de data e hora de criação ou atualização do item. |
| type | enum("root", "delta") | enum | Categoria ou enumeração que define a semântica do dado em uso. |
| id_delta_origin | integer | nullable, FK -> [[systems]] | Chave estrangeira para a tabela relacionada. |

## Relacionamentos

- Outward Links: [[systems]], [[users]]
- Inward Links: [[user_system]], [[systems]], [[tags]], [[entities]], [[description_variant_types]]

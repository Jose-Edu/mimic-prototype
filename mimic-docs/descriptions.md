---
type: database_table
tags: [db, table, mimic, descriptions]
system_domain: "Descrição e narrativa"
---

# Tabela: descriptions

A tabela `descriptions` organiza a parte do modelo de dados responsável por o comportamento e a persistência de descriptions no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_description | integer | PK | Chave estrangeira para a tabela relacionada. |
| id_entity | integer | FK -> [[entities]] | Referência à entidade que representa este registro. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |
| description | text | — | Texto narrativo ou identificador do item na base. |
| id_description_variant | integer | FK -> [[description_variants]] | Chave estrangeira para a tabela relacionada. |

## Relacionamentos

- Outward Links: [[entities]], [[description_variants]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

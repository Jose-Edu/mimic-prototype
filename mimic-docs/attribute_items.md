---
type: database_table
tags: [db, table, mimic, attribute_items]
system_domain: "Atributos e valores"
---

# Tabela: attribute_items

A tabela `attribute_items` organiza a parte do modelo de dados responsável por o comportamento e a persistência de attribute items no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_attribute_item | integer | PK | Chave estrangeira para a tabela relacionada. |
| id_attribute_composer | integer | FK -> [[attributes]] | Chave estrangeira para a tabela relacionada. |
| id_attribute_composable | integer | FK -> [[attributes]] | Chave estrangeira para a tabela relacionada. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |

## Relacionamentos

- Outward Links: [[attributes]], [[attributes]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

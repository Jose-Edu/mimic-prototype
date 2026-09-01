---
type: database_table
tags: [db, table, mimic, entity_attribute]
system_domain: "Atributos e valores"
---

# Tabela: entity_attribute

A tabela `entity_attribute` organiza a parte do modelo de dados responsável por o comportamento e a persistência de entity attribute no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_entity_attribute | integer | PK | Referência ao atributo relacionado. |
| id_entity | integer | FK -> [[entities]] | Referência à entidade que representa este registro. |
| id_attribute | integer | FK -> [[attributes]] | Referência ao atributo relacionado. |

## Relacionamentos

- Outward Links: [[entities]], [[attributes]]
- Inward Links: [[entity_attribute_entry]]

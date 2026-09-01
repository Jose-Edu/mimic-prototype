---
type: database_table
tags: [db, table, mimic, attributes]
system_domain: "Atributos e valores"
---

# Tabela: attributes

A tabela `attributes` organiza a parte do modelo de dados responsável por o comportamento e a persistência de attributes no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_attribute | integer | PK, FK -> [[entities]] | Referência ao atributo relacionado. |
| id_value_rule | integer | FK -> [[rules]] | Referência à regra associada. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |
| value_type | enum("int", "float", "string", "bool") | enum | Categoria ou enumeração que define a semântica do dado em uso. |
| struct_type | enum("value", "enum", "list") | enum | Categoria ou enumeração que define a semântica do dado em uso. |
| default_value | varchar | nullable | Campo textual ou estrutural usado para armazenar a lógica, entrada ou valor padrão. |
| is_composable | boolean | — | Flag booleana que indica o comportamento ou estado permitido do registro. |
| is_constant | boolean | boolean | Flag booleana que indica o comportamento ou estado permitido do registro. |

## Relacionamentos

- Outward Links: [[entities]], [[rules]]
- Inward Links: [[generator_step_skill_attribute]], [[entity_attribute]], [[attribute_items]], [[attribute_items]], [[globals]], [[sheet_skill_attribute]]

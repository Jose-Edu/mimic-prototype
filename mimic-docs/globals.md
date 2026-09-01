---
type: database_table
tags: [db, table, mimic, globals]
system_domain: "Atributos e valores"
---

# Tabela: globals

A tabela `globals` organiza a parte do modelo de dados responsável por o comportamento e a persistência de globals no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_global | integer | PK, FK -> [[entities]] | Chave estrangeira para a tabela relacionada. |
| id_attribute | integer | FK -> [[attributes]] | Referência ao atributo relacionado. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |

## Relacionamentos

- Outward Links: [[entities]], [[attributes]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

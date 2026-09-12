---
type: database_table
tags: [db, table, mimic, descriptions]
system_domain: "Descrição e narrativa"
---

# Tabela: descriptions

A tabela `descriptions` armazena as descrições usadas como documentação manual do sistema.

## Estrutura

| Nome da Coluna         | Tipo    | Constraints                    | Descrição                                     |
| ---------------------- | ------- | ------------------------------ | --------------------------------------------- |
| id_description         | integer | PK                             | Identificador único do registro desta tabela. |
| id_entity              | integer | FK -> [[entities]]             | Referência à entidade documentada.            |
| name                   | varchar | -                              | Nome da descrição.                            |
| description            | text    | -                              | Descrição.                                    |
| id_description_variant | integer | FK -> [[description_variants]] | Variante de descrição.                        |

## Relacionamentos

- Outward Links: [[entities]], [[description_variants]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

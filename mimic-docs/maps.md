---
type: database_table
tags: [db, table, mimic, maps]
system_domain: "Fichas e mapas"
---

# Tabela: maps

A tabela `maps` organiza a parte do modelo de dados responsável por o comportamento e a persistência de maps no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_map | integer | PK, FK -> [[entities]] | Referência ao mapa relacionado. |
| name | varchar | — | Nome descritivo do registro, usado para identificação humana e organização. |
| x_size | integer | — | Coordenada ou dimensão espacial associada ao mapa ou token. |
| y_size | integer | — | Coordenada ou dimensão espacial associada ao mapa ou token. |
| z_size | integer | — | Coordenada ou dimensão espacial associada ao mapa ou token. |

## Relacionamentos

- Outward Links: [[entities]]
- Inward Links: [[map_token]]

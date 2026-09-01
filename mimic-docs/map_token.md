---
type: database_table
tags: [db, table, mimic, map_token]
system_domain: "Fichas e mapas"
---

# Tabela: map_token

A tabela `map_token` organiza a parte do modelo de dados responsável por o comportamento e a persistência de map token no motor de RPG. Ela funciona como um bloco de persistência central dentro do esquema, contribuindo para a representação de entidades, regras, permissões, fichas, habilidades e outros componentes do sistema universal.

## Estrutura

| Nome da Coluna | Tipo | Constraints | Descrição |
| --- | --- | --- | --- |
| id_map_token | integer | PK | Chave estrangeira para a tabela relacionada. |
| id_sheet | integer | FK -> [[sheets]] | Referência à ficha associada. |
| id_map | integer | FK -> [[maps]] | Referência ao mapa relacionado. |
| x | integer | — | Coordenada ou dimensão espacial associada ao mapa ou token. |
| y | integer | — | Coordenada ou dimensão espacial associada ao mapa ou token. |
| z | integer | — | Coordenada ou dimensão espacial associada ao mapa ou token. |
| x_size | integer | — | Coordenada ou dimensão espacial associada ao mapa ou token. |
| y_size | integer | — | Coordenada ou dimensão espacial associada ao mapa ou token. |
| z_size | integer | — | Coordenada ou dimensão espacial associada ao mapa ou token. |
| origin | integer | — | Informações de origem e rotação do token dentro do mapa. |
| angle_x | integer /*0-360*/ | — | Informações de origem e rotação do token dentro do mapa. |
| angle_y | integer /*0-360*/ | — | Informações de origem e rotação do token dentro do mapa. |
| angle_z | integer /*0-360*/ | — | Informações de origem e rotação do token dentro do mapa. |

## Relacionamentos

- Outward Links: [[sheets]], [[maps]]
- Inward Links: Nenhuma tabela referencia diretamente esta tabela.

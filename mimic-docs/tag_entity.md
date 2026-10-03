

A tabela `tag_entity` registra quais tags são aplicadas em quais entidades.

## Estrutura

| Nome da Coluna | Tipo | Constraints            | Descrição |
| -------------- | ---- | ---------------------- | --------- |
| id_tag         | uuid | PK, FK -> [[tags]]     | Tag.      |
| id_entity      | uuid | PK, FK -> [[entities]] | Entidade. |



A tabela `sheets` armazena as fichas existentes, seja como conteúdo padrão do sistema ou ficha de campanha. Seus demais dados vão em tabelas relacionamento.
## Estrutura

| Nome da Coluna | Tipo | Constraints            | Descrição                                     |
| -------------- | ---- | ---------------------- | --------------------------------------------- |
| id_sheet       | uuid | PK, FK -> [[entities]] | Identificador único do registro desta tabela. |
| id_sheet_type  | uuid | FK -> [[sheet_types]]  | Tipo de ficha.                                |

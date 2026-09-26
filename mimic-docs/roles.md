A tabela `roles` organiza os cargos do projeto. Cargos são conjutos de [[access]] que um usuário terá. A nível de sistema, define fuções de jogo como mestre ou jogador.
## Estrutura

| Nome da Coluna | Tipo    | Constraints            | Descrição                                                                                                    |
| -------------- | ------- | ---------------------- | ------------------------------------------------------------------------------------------------------------ |
| id_role        | integer | PK, FK -> [[entities]] | Identificador único do registro desta tabela.                                                                |
| name           | varchar | -                      | Nome do cargo.                                                                                               |
| is_default     | boolean |                        | Flag booleana que indica que o cargo deve ser dado por padrão para todo usuário criado.                      |
| roleless_add   | boolean |                        | Flag booleana que indica que esse cargo deve ser dado para todo usuário que é criado sem nenhum outro cargo. |

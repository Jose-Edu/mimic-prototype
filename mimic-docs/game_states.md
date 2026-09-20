

A tabela `game_states` armazena os possíveis estados do jogo do sistema. Ex: Roleplay, Combate, Exploração e etc. os estados de jogo são usados como forma de categorizar as diferentes formas que as regras do sistema são aplicadas, sendo um critério muito útil para se usar como controle de fluxo nas [[Mimic Rules]]. As regras de definição dos turnos dos [[Eventos Mimic]] são definidas e variam pelo game state.

## Estrutura

| Nome da Coluna     | Tipo    | Constraints            | Descrição                                            |
| ------------------ | ------- | ---------------------- | ---------------------------------------------------- |
| id_game_state      | uuid    | PK, FK -> [[entities]] | Identificador único do registro desta tabela.        |
| name               | varchar | -                      | Nome do estado de jogo.                              |
| turn_count_rule_id | uuid    | FK -> [[rules]]        | Regra que define a quantidade de usuários por turno. |
| turn_order_rule_id | uuid    | FK -> [[rules]]        | Regra que define a ordem dos turnos.                 |


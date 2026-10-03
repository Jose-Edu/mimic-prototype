

A tabela `event_logs` é usada para registrar os [[Eventos Mimic]] executados, tando na execução em si como para consulta de histórico.

## Estrutura

| Nome da Coluna  | Tipo                                                           | Constraints        | Descrição                                                                                      |
| --------------- | -------------------------------------------------------------- | ------------------ | ---------------------------------------------------------------------------------------------- |
| id_event_logs   | uuid                                                           | PK                 | Referência à entidade que representa este registro.                                            |
| created_at      | timestamp                                                      | -                  | Registro de data e hora de criação do evento.                                                  |
| id_entity       | uuid                                                           | FK -> [[entities]] | Entidade do evento.                                                                            |
| event_type      | enum("free", "narrative", "mimic")                             | -                  | Define o tipo de evento. Apenas eventos Mimic tem impacto, os demais são apenas para registro. |
| mimic_event     | enum("read", "use", "update", "create", "delete", "overwrite") | Nullable           | Tipo de evento Mimic. Preenchido se o evento for Mimic.                                        |
| narrative_event | enum("other", "dialog", "action", "narration")                 | Nullable           | Tipo de evento narrativo. Preenchido se o evento for narrativo.                                |
| entry           | text                                                           | -                  | Payload do evento.                                                                             |
| multi_part_id   | uuid                                                           | Nullable           | Id gerado para eventos multipart.                                                              |
| resolved        | boolean                                                        | -                  | Flag que diz se o evento foi executado.                                                        |


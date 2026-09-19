---
type: database_table
tags:
  - db
  - table
  - mimic
system_domain: Usuários, entidades e permissões
---

# Tabela: event_logs

A tabela `event_logs` é usada para registrar os [[Eventos Mimic]] executados, tando na execução em si como para consulta de histórico.

## Estrutura

| Nome da Coluna | Tipo                                                           | Constraints        | Descrição                                                                                                             |
| -------------- | -------------------------------------------------------------- | ------------------ | --------------------------------------------------------------------------------------------------------------------- |
| id_event_logs  | uuid                                                           | PK                 | Referência à entidade que representa este registro.                                                                   |
| created_at     | timestamp                                                      | -                  | Registro de data e hora de criação do evento.                                                                         |
| id_entity      | uuid                                                           | FK -> [[entities]] | entidade do evento.                                                                                                   |
| event_type     | enum("free", "mimic")                                          | -                  | Define se é um Evento Mimic ou um registro arbitrário. Eventos Free servem apenas para histórico, sem causar impacto. |
| mimic_event    | enum("read", "use", "update", "create", "delete", "overwrite") | Nullable           | Tipo de evento Mimic.                                                                                                 |
| entry          | text                                                           | -                  | Payload do evento.                                                                                                    |
| multi_part_id  | uuid                                                           | Nullable           | Id gerado para eventos multipart.                                                                                     |
| resolved       | boolean                                                        | -                  | Flag que diz se o evento foi executado.                                                                               |


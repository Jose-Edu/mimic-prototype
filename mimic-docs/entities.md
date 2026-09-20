

A tabela `entities` organiza todos os elementos internos do sitema, pratimamente todas as tabelas são possuem relacionamento 1:1 com essa tabela através de uma FK na própria PK. Servem para adicionar metadados padrão e permitir abstrações de acesso pela [[Mimic SDK]].

## Estrutura

| Nome da Coluna      | Tipo                                         | Constraints                  | Descrição                                                                                            |
| ------------------- | -------------------------------------------- | ---------------------------- | ---------------------------------------------------------------------------------------------------- |
| id_entity           | uuid                                         | PK                           | Identificador único do registro desta tabela.                                                        |
| created_at          | timestamp                                    | -                            | Registro de data e hora de criação da entidade.                                                      |
| updated_at          | timestamp                                    | -                            | Registro de data e hora de atualização da entidade.                                                  |
| id_system           | uuid                                         | FK -> [[systems]]            | Referência ao sistema ao qual a entidade pertence.                                                   |
| id_creator_user     | uuid                                         | FK -> [[users]]              | Referência ao usuário que criou a entidade, usado para mapear posse nos [[Eventos Mimic]].           |
| id_overrides_entity | uuid                                         | nullable, FK -> [[entities]] | Referência à entidade no qual essa sobrescreve. Usado para atualizações nos [[Mimic Deltas]]         |
| table_name          | varchar /*ex: generators, rules, roles etc*/ | -                            | Campo com o nome da tabela que possui o 1:1 com essa pela PK.                                        |
| is_active           | boolean                                      | Default True                 | Flag booleana que indica se a entidade não foi deletada. Usada para remoções nos [[Mimic Deltas]]    |
| is_featured         | boolean                                      | Default False                | Flag booleana que indica se essa entidade deve ser destaca ao consultar informações sobre o sistema. |

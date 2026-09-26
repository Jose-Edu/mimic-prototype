

A tabela `migrations` registra as mudaças estruturais do sistema de rpg. Não confundir com mudança do schema do banco em si, o mimic não muda o schema nunca. Serve para registrar mudanças de dados do sistema como mudar um bônus de um atributo em uma classe, por exemplo.

## Estrutura

| Nome da Coluna     | Tipo      | Constraints       | Descrição                                                               |
| ------------------ | --------- | ----------------- | ----------------------------------------------------------------------- |
| id_migration       | uuid      | PK                | Identificador único do registro desta tabela.                           |
| mimic_version      | varchar   | -                 | Versão do mimic usada. Ex: '1.0.0'.                                     |
| created_at         | timestamp | -                 | Momento de criação da migration.                                        |
| updated_at         | timestamp | -                 | Momento de atualização da migration.                                    |
| migration_name     | varchar   | -                 | nome da migration, igual ao nome do arquivo sem a extensão.             |
| resolved           | boolean   | Default false     | Flag booleana que indica se a migration já rodou.                       |
| new_system_version | varchar   | Nullable          | Atualização para o campo version do [[systems]], se null, não atualiza. |
| id_system          | uuid      | FK -> [[systems]] | Sistema que está sendo atualizado.                                      |



A tabela `descriptions` armazena as descrições de entidades. São usadas como documentação manual do sistema.

## Estrutura

| Nome da Coluna | Tipo    | Constraints        | Descrição                                     |
| -------------- | ------- | ------------------ | --------------------------------------------- |
| id_description | uuid    | PK                 | Identificador único do registro desta tabela. |
| id_entity      | uuid    | FK -> [[entities]] | Referência à entidade documentada.            |
| description    | text    | -                  | Descrição.                                    |
| illustration   | varchar | Nullable           | Link para imagem de ilustração. Opcional.     |


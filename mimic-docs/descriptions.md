

A tabela `descriptions` armazena as descrições de entidades. São usadas como documentação manual do sistema.

## Estrutura

| Nome da Coluna | Tipo                                                                                              | Constraints        | Descrição                                                                          |
| -------------- | ------------------------------------------------------------------------------------------------- | ------------------ | ---------------------------------------------------------------------------------- |
| id_description | uuid                                                                                              | PK                 | Identificador único do registro desta tabela.                                      |
| id_entity      | uuid                                                                                              | FK -> [[entities]] | Referência à entidade documentada.                                                 |
| description    | text                                                                                              | -                  | Descrição.                                                                         |
| image_type     | image_type enum("other", "illustration", "icon", "diagram", "full_page", "banner", "main_folder") | Nullable           | Tipo de imagem presente na descrição. Presente se houver uma imagem em image_link. |
| image_link     | varchar                                                                                           | Nullable           | Link para imagem de ilustração. Opcional.                                          |


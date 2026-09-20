

A tabela `map_token` registra um token num mapa, usando o seu sistema de posição, onde ABC generaliza as 3 variáveis de posição usadas.

## Estrutura

| Nome da Coluna | Tipo    | Constraints                | Descrição                                                     |
| -------------- | ------- | -------------------------- | ------------------------------------------------------------- |
| id_map_token   | uuid    | PK                         | Identificador único do registro desta tabela.                 |
| id_sheet       | uuid    | FK -> [[sheets]], Nullable | Ficha no qual o token referencia. Null se não representa uma. |
| id_map         | uuid    | FK -> [[maps]]             | Mapa onde o token está.                                       |
| position_a     | integer | -                          | Coordenada A do token no mapa.                                |
| position_b     | integer | -                          | Coordenada B do token no mapa.                                |
| position_c     | integer | -                          | Coordenada C do token no mapa.                                |
| size_a         | integer | -                          | Tamanho do token no eixo A.                                   |
| size_b         | integer | -                          | Tamanho do token no eixo B.                                   |
| size_c         | integer | -                          | Tamanho de token no eixo C.                                   |
| origin_a       | integer | -                          | Posição de origem no eixo A.                                  |
| origin_b       | integer | -                          | Posição de origem no eixo B.                                  |
| origin_c       | integer | -                          | Posição de origem no eixo C.                                  |
| angle_a        | integer | -                          | Rotação do token de 0 a 360 no eixo A.                        |
| angle_b        | integer | -                          | Rotação do token de 0 a 360 no eixo B.                        |
| angle_c        | integer | -                          | Rotação do token de 0 a 360 no eixo C.                        |


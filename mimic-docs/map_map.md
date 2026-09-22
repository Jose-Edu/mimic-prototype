

A tabela `map_map` representa as conexões entre diferentes mapas, podendo ser usado para conectar todo o mundo do rpg ou criar mapas em sistemas de zonas.
## Estrutura

| Nome da Coluna     | Tipo    | Constraints        | Descrição                                                            |
| ------------------ | ------- | ------------------ | -------------------------------------------------------------------- |
| id_map_origin      | uuid    | PK, FK -> [[maps]] | Mapa origem.                                                         |
| id_map_destination | uuid    | PK, FK -> [[maps]] | Mapa destino.                                                        |
| distance           | integer | -                  | Distância calculada entre um mapa e outro, usada como peso de grafo. |
| expand_a           | integer | Nullable           | Ponto de expansão partindo da origem no eixo A.                      |
| expand_b           | integer | Nullable           | Ponto de expansão partindo da origem no eixo B.                      |
| expand_c           | integer | Nullable           | Ponto de expansão partindo da origem no eixo C.                      |
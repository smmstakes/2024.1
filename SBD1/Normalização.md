###### Aula 05 - 16.04
**Aula Anterior:** [[Dependência Funcional]] (Aula 04 - 09.04)
**Próxima Aula:** [[]] (Aula 06 - 18.04)

---
# Normalização
É um processo fundamental para garantir a organização, consistência e eficiência do armazenamento de informações. Através da normalização, você elimina redundâncias de dados, minimiza anomalias e garante a integridade das informações ao longo do tempo. Foi proposto por Codd, em 1972 (1FN, 2FN e 3FN).

![[Modelagem_e_Normalização.png]]

A relação entre as normalizações e desempenho de consultas é:
![[Normalização_x_desempenho.png]]

## Primeira Forma Normal (1FN)
- **Não** permite **atributos multivalorados**.
##### Exemplo

![[1FN_tabela_exemplo.png]]

Para este caso temos 3 possíveis soluções:
###### Solução nº 1
Cada valor em **uma linha**.

| ***Numero*** | Nome      | Gerente | Localização  |
| ------------ | --------- | ------- | ------------ |
| 1DEP         | Pesquisa  | 111222  | Floripa      |
| 1DEP         | Pesquisa  | 111222  | Joinville    |
| 1DEP         | Pesquisa  | 111222  | Blumenau     |
| 2DEP         | RH        | 222333  | Joinville    |
| 3DEP         | Adm       | 333444  | Floripa      |
| 3DEP         | Adm       | 333444  | Porto Alegre |
| 4DEP         | Diretoria | 444555  | Floripa      |

###### Solução nº 2
Valores em **novas colunas**.

| ***Numero*** | Nome      | Gerente | Local_Central | Local_Apoio  | Local_Urgencia |
| ------------ | --------- | ------- | ------------- | ------------ | -------------- |
| 1DEP         | Pesquisa  | 111222  | Floripa       | Joinville    | Blumenau       |
| 2DEP         | RH        | 222333  | Joinville     | NULL         | NULL           |
| 3DEP         | Adm       | 333444  | Floripa       | Porto Alegre | NULL           |
| 4DEP         | Diretoria | 444555  | Floripa       | NULL         | NULL           |
###### Solução nº 3
**Criar duas novas tabelas.**

| ***Numero*** | Nome      | Gerente |
| ------------ | --------- | ------- |
| 1DEP         | Pesquisa  | 111222  |
| 2DEP         | RH        | 222333  |
| 3DEP         | Adm       | 333444  |
| 4DEP         | Diretoria | 444555  |

| ***Numero*** | ***Cod_Local*** | Localização  |
| ------------ | --------------- | ------------ |
| 1DEP         | LC01            | Floripa      |
| 1DEP         | LC02            | Joinville    |
| 1DEP         | LC03            | Blumenau     |
| 2DEP         | LC02            | Joinville    |
| 3DEP         | LC01            | Floripa      |
| 3DEP         | LC04            | Porto Alegre |
| 4DEP         | LC01            | Floripa      |


> **NOTA:** é a melhor opção dentre as 3 apresentadas.

## Segunda Forma Normal (2FN)
- **Não** permite **atributos multivalorados**.
- **Não** permite **dependência funcional parcial**

##### Exemplo


---
**tags:** #FN #BoyceCodd #Codd #normalização #desempenho 
**Home:** [[#Aula 05 - 16.04]]
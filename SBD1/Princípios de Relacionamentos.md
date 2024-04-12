###### Aula 03 - 04.04
**Aula Anterior:** [[Princípios de Cardinalidade]] (Aula 02 - 26.03)
**Próxima Aula:** [[Dependência Funcional]] (Aula 04 - 09.04)

---
# Princípios de Relacionamentos
## Relacionamentos Fortes
### 1:1 
Prefere-se que separe em 2 tabelas, para mais tarde na **normalização**.

![[Relacionamento_1_1.png]]

### 1:n
A chave primaria da entidade que se relaciona com "1" vai para a tabela como **chave estrangeira**.

![[Relacionamento_n_1.png]]

### n:n
O **relacionamento** vira uma **nova tabela** com *chaves primarias das duas entidades*.

![[Relacionamento_n_n.png]]

## Relacionamentos de Entidade Fraca
### Para todas as Cardinalidades
Pega as **chaves primarias da entidade forte** e *aloca na tabela da entidade fraca*.

![[Relacionamento_Entidade_Fraca.png]]

## Auto Relacionamento
### 1:1 e 1:n
A **chave primaria** vira uma *chave estrangeira da própria entidade*.

![[Auto_relacionamento_1_1_e_1_n.png]]

### n:n
Se cria uma **nova tabela da relação** com as *chaves primárias* da entidade.

![[Auto_relacionamento_n_n.png]]

## Relacionamento de Generalização/Especialização
Há três opções, as mais viáveis para fim de utilização são as duas primeiras para evitar *campos nulos*, dentro dessas duas opções a melhor será de acordo com a situação atual da modelagem.

![[Relacionamento_Generalizacao.png]]

## Relacionamento Ternário
### 1:1:1
Cria-se uma **tabela para a relação** com as *três chaves primárias*, porém é escolhido duas delas como **chaves primárias da tabela de relação**.

![[Relacionamento_ternario_1_1_1.png]]

### 1:1:n
Cria-se uma **tabela para a relação** com as *três chaves primárias*, porém é escolhido duas delas como **chaves primárias da tabela de relação e excepcionalmente a entidade com "n" relações deve ter sua chave  como primária**.

![[Relacionamento_ternario_1_1_n.png]]

### 1:n:n
Cria-se uma **tabela para a relação** com as *três chaves primárias*, porém é escolhido duas delas como **chaves primárias da tabela de relação e excepcionalmente as entidades com "n" relações deve ter suas chaves como primária**.

![[Relacionamento_ternario_1_n_n.png]]

### n:n:n
Cria-se uma **tabela para a relação** com as *três chaves primárias*, porém é escolhido **todas** delas como **chaves primárias da tabela de relação**.

![[Relacionamento_ternario_n_n_n.png]]

---
**tags:** #cardinalidade #relacionamento #autorelacionamento #entidade_fraca
**Home:** [[#Aula 03 - 04.04]]
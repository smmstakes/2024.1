###### Aula 05 - 16.04
**Aula Anterior:** [[Dependência Funcional]] (Aula 04 - 09.04)
**Próxima Aula:** [[Introdução a Linguagem SQL]] (Aula 06 - 18.04)

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
![[1FN_exemplo_solucao_1.png]]

###### Solução nº 2
Valores em **novas colunas**.
![[1FN_exemplo_solucao_2.png]]

###### Solução nº 3
**Criar duas novas tabelas.**
![[1FN_exemplo_solucao3.png]]

> **NOTA:** é a melhor opção dentre as 3 apresentadas.

## Segunda Forma Normal (2FN)
- **Não** permite **atributos multivalorados**.
- **Não** permite **dependência funcional parcial**
	- *Dependência Parcial* é quando uma coluna depende apenas de uma parte da **chave primária composta**.

> **NOTA:** **Toda** tabela que tenha **apenas uma chave primária** está automaticamente na **2FN**.
##### Exemplo
![[Dependencias_funcionais.png]]

Sua versão na 2FN é:
![[2FN_exemplo_solucao.png]]
## Terceira Forma Normal (3FN)
 - **Não** permite **atributos multivalorados**.
- **Não** permite **dependência funcional parcial**
	- *Dependência Parcial* é quando uma coluna depende apenas de uma parte da **chave primária composta**.
- **Não** permite *dependência funcional* entre **atributos não-chaves**.

> **NOTA:** **Toda** tabela que tenha apenas **uma chave primária** e **um único atributo** está na 3FN.

##### Exemplo

![[3FN_tabela_exemplo.png]]
- Existem 2 principais problemas: **i
	- *Inserção:* pode causar inconsistência na base de dados
	- *Remoção:* pode tirar completamente uma informação
	- *Atualização:* precisará percorrer todas as tuplas da tabela para realizar atualização

###### Solução
![[3FN_exemplo_solucao.png]]

## Forma Normal de Boyce-Codd (FNBC)
Considerando a seguinte tabela na 3FN.
![[FNBC_exemplo01.png]]

>**IMPORTANTE:** Nota-se algumas *anomalias* na tabela, mesmo que esteja na 3FN, da pra perceber que a agência é repetida para o mesmo gerente
>**NOTA:** ***Chaves Candidatas*** são atributos que poderiam ser chaves primárias da tabela. 

Nessa tabela, temos as seguintes chaves candidatas: 
- {Cliente, Agencia}
- {Cliente, Gerente}
- {Cliente, Gerente, Agencia}
E as seguintes dependências:
- Gerente -> Agencia 
	- Gerente não é chave candidata, logo quebra a FNBC
- {Cliente, Agencia} -> Gerente
- {Cliente, Gerente} -> Agencia

##### Regra da FNBC
Uma tabela **não** estará na FNBC se **existir alguma dependência funcional** *X* -> Y, tal que *X* **não é uma chave candidata**.

###### Solução
![[FNBC_exemplo01_solucao.png]]


---
**tags:** #FN #BoyceCodd #Codd #normalização #desempenho 
**Home:** [[#Aula 05 - 16.04]]
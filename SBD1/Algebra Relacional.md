###### Aula 07 - 07.05
**Aula Anterior:** [[Introdução a Linguagem SQL]] ()
**Próxima Aula:** [[]] ()

---
# Álgebra Relacional

## Operadores Relacionais
### Operadores de conjunto
1. **[[#União]]:** $Tabela1 \cup Tabela2$
2. **[[#Interseção]]:** $T1 \cap T2$
3. **[[#Diferença]]:** $T1 - T2$
4. **[[#Produto Cartesiano]]:** $T1$ $X$ $T2$
### Operadores Relacionais
1. **[[#Seleção]]:** $\sigma  Atributo =$ $'xxx'$
2. **[[#Projeção]]:** $\pi$  $Atributo(T1)$
3. **[[#Inner Join]]:** $T1 \Join T2$
4. **[[#Outer Join]]:** $T1$ $⟕$ $T2$
	1. **[[#Left Outer Join]]:** $T1$ $⟕$ $T2$
	2. **[[#Right Outer Join]]:** $T1$ $⟖$ $T2$
	3. **[[#Full Outer Join]]:** $T1$ $⟗$ $T2$
5. **[[#Divisão]]:** $T1 \div T2$
6. **[[#Renomeação]]:** $\rho$

#### União
Realiza a **junção** das duas tabelas em uma só, assim como em **conjuntos**.

> **NOTA:** As duas tabelas **devem** ter o *mesmo número de **colunas** e cada coluna **o mesmo domínio**(tipo)*.

![[Uniao.png]]

#### Interseção
Retorna uma *única tabela* contendo **apenas as tuplas que se repetem.**
![[Intercecao.png]]

> **OBS:** No exemplo acima mostra a recuperação dos dados dos funcionários que são clientes.

#### Diferença
Retorna uma tabela com os valores da *Tabela 1* que **não** estão presentes na *Tabela 2*.
![[Diferenca.png]]

#### Produto Cartesiano
Realiza a combinação de **todas as linhas da Tabela 2** com as linhas da **Tabela 1**.

![[Produto_Cartesiano.png]]
#### Seleção
#### Projeção
#### Inner Join
#### Outer Join
##### Left Outer Join
##### Right Outer Join
##### Full Outer Join
#### Divisão
#### Renomeação

---
**tags:** #relacional #algebra
**Home:** [[#Aula 07 - 07.05]]
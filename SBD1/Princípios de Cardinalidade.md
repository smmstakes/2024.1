###### Aula 02 - 26.03
**Aula Anterior:** [[Introdução]] (Aula 01 - 21.03)
**Próxima Aula:** [[]] (Aula 03 - 04.04)

--- 
# Princípios de Cardinalidade

## Tipos de Cardinalidade
Define a quantidade de relações que cada entidade pode ter com outra entidade. É representado como:
- cardinalidade **mínima** : cardinalidade **máxima**
>**NOTA:** a direção é invertida, como em X.

### 1:1
É quando uma *entidade A* está associada a **uma e somente uma** outra *entidade B*.

```mermaid
graph LR
A[Marido] -- 1:1 --> B[Esposa]
```

### 1:n
É quando uma *entidade A* está associada a **pelo menos uma** outra *entidade*.

```mermaid
graph LR
A[Faculdade] -- 1:n --> B[Alunos]
```

### Relacionamentos
#### 1:1 
Prefere-se que separe em 2 tabelas, para mais tarde na **normalização**

#### 1:n
A chave primaria do "1" vai para o "n"

#### n:n
Relacionamento vira uma nova tabela com chaves primarias das duas entidades

#### 1:n (Entidade Fraca)
Pega as chaves primarias da entidade forte e aloca na tabela da entidade fraca

### Mapeamento de Auto-relacionamento
##### 1:1 e 1:n
A chave primaria vira uma chave estrangeira da propria entidade

---
**tags:** #cardinalidade #herança 
**Home:** [[#Aula 02 - 26.03]]
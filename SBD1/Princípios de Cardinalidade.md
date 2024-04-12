###### Aula 02 - 26.03
**Aula Anterior:** [[Introdução]] (Aula 01 - 21.03)
**Próxima Aula:** [[Princípios de Relacionamentos]] (Aula 03 - 04.04)

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
A[Marido] --- 1:1 --> B[Esposa]
```

### 1:n
É quando uma *entidade A* está associada a **pelo menos uma** outra *entidade*.

```mermaid
graph LR
A[Faculdade] --- 1:n --> B[Alunos]
```

### n:n
É quando uma *entidade A* está associada a **várias** outras *entidades*.

```mermaid
graph LR
A[Professor] --- n:n --> B[Disciplina]
```

## Notações de Engenharia de Informação

![[Notacao_de_Engenharia_de_Informacao.png]]

---
**tags:** #cardinalidade #entidades
**Home:** [[#Aula 02 - 26.03]]
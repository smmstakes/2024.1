###### Aula 04 - 09.04
**Aula Anterior:** [[Princípios de Relacionamentos]] (Aula 03 - 04.04)
**Próxima Aula:** [[Normalização]] (Aula 05 - 16.04)

---
# Dependência Funcional
Seja **X** e **Y** *dois conjuntos de atributos de uma tabela*. Dizemos que Y é **funcionalmente dependente** de X se e somente se conseguimos obter Y sabendo apenas os valores de X. 
É representado como: **X -> Y**

###### Exemplo 01

| Cod_Funcionario | Nome    | Sobrenome | Departamento |
| --------------- | ------- | --------- | ------------ |
| 125             | Silvia  | Martins   | 003          |
| 236             | Ana     | Martins   | 016          |
| 555             | Antônio | Oliveira  | 003          |
- ==Cod_Funcionario -> Departamento==? **Sim!** Então *Departamento* é **dependente funcional** de *Cod_Funcionario*
- ==Departamento -> Cod_Funcionario==? **Não**, pois há departamentos que aparecem em duas *tuplas*
- ==Nome -> Cod_Funcionario==? **Não**, pois podem haver funcionários com o mesmo nome

###### Exemplo 02

| Numero | Depto         | Gerente |
| ------ | ------------- | ------- |
| 001    | RH            | Luisa   |
| 002    | Marketing     | Renato  |
| 003    | Diretoria     | Marcos  |
| 004    | Contabilidade | Marcos  |
- =={Depto, Gerente} -> Numero==? Sim! Então *Numero* é **dependente funcional** de *{Depto, Gerente}*
- ==Gerente -> Depto==? **Não**, pois há 2 gerentes chamados Marcos
- ==Depto -> Numero==? **Para esta instância, sim!**

## Regras da Dependência Funcional
### Regra da Separação

```
A --> BC
então,
A --> B e A --> C
```
###### Exemplo:
CPF --> {Nome, Endereço}
então,
CPF --> Nome 
CPF --> Endereço

### Regra da Acumulação

```
A --> B
então,
AC --> B
```
###### Exemplo:
CPF --> Endereço
então,
{CPF, Nome} --> Endereço

### Regra da Pseudo-Transitividade

```
A --> B e BC --> D
então,
AC --> D
```
###### Exemplo:
CPF --> Endereço
{Endereço, Cidade} --> Estado
então,
{CPF, Cidade} --> Estado

## Tipos de Dependência
### Dependência Funcional Total
Se uma tabela tiver uma chave primária composta, dizemos que esta tabela tem **dependência funcional forte** se todas as colunas dessa tabela depender funcionalmente de **todos** os *atributos da chave primária composta*.

### Dependência Funcional Parcial
Se uma tabela tiver uma chave primária composta, dizemos que esta tabela tem **dependência funcional parcial** se existir **alguma coluna** dessa tabela que dependa funcionalmente de *apenas parte da chave primária*.

###### Exemplo

![[Dependencias_funcionais.png]]

- As setas **verdes** representam as *Dependências Funcionais Totais* e as **vermelhas** as *Dependências Funcionais Parciais*.
	- Essas dependências mistas podem gerar problemas na **inserção** (duplicidade de informações e desperdício) e **deleção** (caso haja apenas uma ocorrência de algum campo pode ser deletado totalmente do banco).

---
**tags:** #dependencia_funcional
**Home:** [[#Aula 04 - 09.04]]
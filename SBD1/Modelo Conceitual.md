###### Aula 01 - Extra
**Aula Anterior:** [[Introdução]] (Aula 01 - 21.03)
**Próxima aula:** [[Princípios de Cardinalidade]] (Aula 02 - 26.03)

---
# Modelo Conceitual
Dessa forma o modelo conceitual irá descrever a realidade do ambiente real e o problema, sendo uma visão geral dos principais dados e suas relações, independente das restrições de implementação (JUKIC, N.; VRBSKY S.; NESTOROV, S, 2013).

## Passos
1. Identificar **entidades**
2. Identificar os **atributos** de cada entidade
3. Identificar os **relacionamentos**
4. Identificar a **cardinalidade dos relacionamentos**
5. Ajustar relacionamentos, entidades e atributos
6. Gerar as **tabelas**

## Composição
- **Retângulos:** representam as *entidades*
- **Elipses/Círculos:** representam os *atributos*
	- Aqueles que estiverem completamente pintados representam a **chave primária** da entidade
- **Losangos:** representam os *relacionamentos*

### Tipos de Entidades
1. **Forte:** existem por si só
2. **Fracas:** precisam de outra entidade para existir e **não** possuem *chave primária*. Representado por **retângulo com bordas duplas.**
	1. **Exemplo:** Suponha que um funcionário é demitido da empresa. Nesse caso, o funcionário e todos os seus dependentes serão removidos do banco de dados. Portanto, a entidade Dependente é uma entidade fraca porque ela depende da entidade Funcionário para existir.

>**NOTA:** a *Herança* nesta matéria apenas herda os atributos

---
**tags:** #entidades #relacionamento #tabelas #cardinalidade
**Home:** [[#Aula 01 - Extra]]
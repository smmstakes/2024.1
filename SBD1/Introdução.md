**Próxima aula:** [[]] (Aula 02 - 26.03)
# SGBD
“Um Banco de Dados é um objeto mais complexo, é uma coleção de dados armazenados e inter-relacionados, que atende às necessidades de vários usuários dentro de uma ou mais organizações, ou seja, coleções inter-relacionadas de muitos tipos diferentes de tabelas.” (TOREY et al,p.2,2007)”
--
#### Vantagens
- Controle centralizado dos dados
- Controle de redundância
- Compartilhamento de dados
- Facilidade de acesso
- Independência dos dados

# Modelagem de Dados
- **Dado:** é o componente básico de um arquivo, é um elemento com um significado no mundo real, que compõe um sistema de arquivos. Ex: nome, cidade, etc.
- **Informação:** Interpretação dos dados com um significado associado.
- **Conhecimento:** é todo discernimento, obtido por meio de critérios, e apreciação aos dados e informações

É o estágio inicial de manipulação de dados a serem armazenados, onde este estágio é dado pelos modelos a seguir:
1. [[#Modelo Conceitual]]
2. [[#Modelo Lógico ]]
3. [[#Modelo Físico]]

## Modelo Conceitual
Geralmente se utiliza do **Modelo Entidade Relacionamento** para descrever os requisitos que se deseja no banco, com um grande nível de abstração.
Dessa forma o modelo conceitual irá descrever a realidade do ambiente real e o problema, sendo uma visão geral dos principais dados e suas relações, independente das restrições de implementação (JUKIC, N.; VRBSKY S.; NESTOROV, S, 2013).

- Define o **escopo** do problema
- Identifica as principais entidades e suas relações
- Modelagem **UML**, aqui vemos os [[Princípios de Cardinalidade]]

### Passos
1. Identificar **entidades**
2. Identificar os **atributos** de cada entidade
3. Identificar os **relacionamentos**
4. Identificar a **cardinalidade dos relacionamentos**
5. Ajustar relacionamentos, entidades e atributos
6. Gerar as **tabelas**

## Modelo Lógico
Irá descrever quais estruturas devem contem no Banco de Dados, desconsiderando características específicas do SGBD, ele possui três abordagens possíveis:
1. **Modelo Relacional:** classifica os seus dados em tabelas que possuem seus relacionamentos.
2. **Modelo Hierárquico:** organizado em uma *árvore*, onde cada registro tem um *único pai* e seus *irmãos* são organizados em uma ordem específica.
3. **Modelo de Rede:** cada conjunto consiste em um registro proprietário, e um ou mais registros de membro. Um registro pode ser um membro, em vários conjuntos, permitindo que esse modelo transmita relações complexas (HEUSER, 2004).

## Modelo Físico
É o modelo que irá descrever as estruturas físicas do banco, assim podendo realizar a implementação do mesmo, que envolve *hardware* e *softwares* que serão utilizados. Suas estruturas são:
- Tamanho dos campos
- Tipos de campos
- Terminologias
- Eficiência dos recursos computacionais

---
### Conceitos da Modelagem (Glauco)
- **Atributos:** propriedade de uma tabela
- **Esquemas:** conjunto de *atributos*
- **Tuplas:** linhas da tabela
- **Instância:** conjunto de tuplas

**Ex:** Produto(==Cod_Produto==, Valor)

---
**tags:** #SGBD #Flask #CRUD #UML #SQL #NoSQL

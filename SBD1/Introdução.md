###### Aula 01 - 21.03
**Próxima aula:** [[Princípios de Cardinalidade]] (Aula 02 - 26.03)

---
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

- Define o **escopo** do problema
- Identifica as principais entidades e suas relações
- Modelagem **UML**, aqui vemos os [[Princípios de Cardinalidade]]
- Mais sobre [[Modelo Conceitual]] (**EXTRA**)

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
- **Chave Primária:** Identificador/atributo *único* 
- **Chave Estrangeira:** *chave primária* de uma outra entidade

**Ex:** Produto(*Cod_Produto*, Nome, ##Cod_Fornecedor)

---
**tags:** #SGBD #Flask #CRUD #UML #SQL #NoSQL
**Home:** [[#Aula 01 - 21.03]]

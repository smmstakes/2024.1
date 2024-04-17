###### Aula 06 - 18.04
**Aula Anterior:** [[Normalização]] (Aula 05 - 16.04)
**Próxima Aula:** [[]] ()
**Site:** https://sqliteonline.com/

---
# Introdução a Linguagem SQL
## Criar Tabela e Inserção

```sqlite
CREATE TABLE IF NOT EXISTS Aluno1(
	Id INTEGER PRIMARY KEY AUTOINCREMENT, -- Automaticamente inserido
	Nome TEXT
);

CREATE TABLE Aluno2(
	Id INTEGER,
	Nome TEXT,
	PRIMARY KEY(Id) -- Não é possivel utilizar o autoincrement
);

INSERT INTO Aluno1(Nome) VALUES("João");
INSERT INTO Aluno2 VALUES(1, "Maria");
INSERT INTO Aluno2 VALUES
(2, "João"),
(3, "Carlos);
```

> **NOTA:** `SELECT * FROM nome_tabela` mostra toda a tabela.

### Constrains
São regras aplicadas a tabela para configurar algumas características de uma determinada coluna.

#### NOT NULL
Faz que o campo não seja capaz de receber um valo nulo, ou seja, necessariamente ele deve receber um valor.

```sqlite
CREATE TABLE Aluno(
	Id INTEGER,
	Nome TEXT NOT NULL,
	PRIMARY KEY(Id)
);
```

#### DEFAULT
Faz com que o campo, caso não seja atribuído nenhum valor a ele, receba um valor padrão.

```sqlite
CREATE TABLE Aluno(
	Id INTEGER PRIMARY KEY,
	Nome TEXT DEFAULT "Aluno Sem Nome"
);
```

#### UNIQUE
Garante que **todos** os valores de uma coluna sejam diferentes.

```sqlite
CREATE TABLE Aluno(
	Id INTEGER PRIMARY KEY,
	Nome TEXT UNIQUE
);
```

#### CHECK
Realiza uma verificação de uma determinada condição.

```sqlite
CREATE TABLE Aluno(
	Id INTEGER PRIMARY KEY,
	Nome TEXT CHECK((length("Nome") >= 4))
);

INSERT INTO Aluno VALUES (1, "Isa"); -- Não será inserido
```

#### PRIMARY KEY
Transforma uma chave existente em uma chave estrangeira de outra tabela.

```sqlite
CREATE TABLE Biblioteca(
	CNPJ INTEGER,
	Sigla TEXT NOT NULL,
	PRIMARY KEY(CNPJ)
);

CREATE TABLE Livro(
	ISBN INTEGER,
	Titulo TEXT NOT NULL,
	CNPJ INTEGER,
	PRIMARY KEY(ISBN),
	FOREIGN KEY(CNPJ) REFERENCES Biblioteca(CNPJ)
);
```

##### ON DELETE e ON UPDATE
São ações para tratamento de **remoção** e **atualização** de chaves estrangeiras.

| Ação          | Descrição                                                                                           |
| ------------- | --------------------------------------------------------------------------------------------------- |
| **NO ACTION** | Não faz nada. Padrão                                                                                |
| **SET NULL**  | Colocar `NULL` no valor                                                                             |
| **CASCADE**   | Propaga a atualização/remoção para todas as tabelas que fazem referência à chave primária da tabela |
| **RESTRICT**  | Não permite a remoção/atualização do dado.                                                          |
## Atualização e Exclusão da Tabela

```sqlite
CREATE TABLE Aluno(
	Matricula INTEGER,
	Nome TEXT,
	Idade INTEGER,
	PRIMARY KEY(Matricula)
);

INSERT INTO Aluno VALUES
(111, "João", 18),
(222, "Maria", 20),
(333, "José", 22);

DELETE FROM Aluno; -- Remove TODOS os dados da tabela
DELETE FROM Aluno WHERE Nome = "Maria";

UPDATE Aluno SET Nome = "Joana"; -- Atualiza TODOS os "Nome" para Joana
UPDATE Aluno SET Nome = "Joana" WHERE Nome = "José";
```

## Modificando a Tabela
### ALTER TABLE
#### Adicionar e Remover Coluna

```sqlite
ALTER TABLE Aluno
ADD Sala INTEGER;

ALTER TABLE Aluno
DROP COLUMN Sala;
```
#### Renomear e Alterar o Tipo 

```sqlite
ALTER TABLE Aluno
RENAME COLUMN Nome TO NomeCompleto;

ALTER TABLE Aluno
ALTER COLUMN Id TEXT;
```

##### Exemplo
![[Exemplo_questao6.png]]

###### Solução
```sqlite
PRAGMA foreign_keys = ON;

CREATE TABLE Aluno(
	Cod_Aluno INTEGER PRIMARY key,
  	Nome_Aluno TEXT
);

CREATE TABLE Professor(
	Cod_Prof INTEGER PRIMARY KEY,
  	Nome_Prof TEXT
);

CREATE TABLE Disciplina(
  Cod_Disc INTEGER Primary KEY,
  Nome_Disc TEXT
);

CREATE TABLE Monitoria(
  	ano INTEGER,
  	Cod_Prof INTEGER,
  	Cod_Aluno INTEGER,
  	Cod_Disc INTEGER,
  	PRIMARY key(Cod_Aluno, Cod_Prof),
  	FOREIGN key(Cod_Aluno) REFERENCES Aluno(Cod_Aluno) on DELETE SET NULL ON UPDATE CASCADE,
  	FOREIGN key(Cod_Prof) REFERENCES Professor(Cod_Prof) on DELETE SET NULL ON UPDATE CASCADE,
  
  	FOREIGN key(Cod_Disc) REFERENCES Disciplina(Cod_Disc)	
);

INSERT INTO Aluno VALUES
(555, "Joaquim"),
(444, "José");

INSERT INTO Professor VALUES
(222, "Maria"),
(333, "João");

INSERT INTO Disciplina VALUES
(113, "SBD1"),
(112, "MD1");

INSERT INTO Monitoria VALUES
(2024, 222, 555, 113),
(2024, 333, 444, 112);
```

---
**tags:** #SQL #SQLite 
**Home:** [[#Aula 06 - 18.04]]
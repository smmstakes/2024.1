###### Aula 06 - 18.04
**Aula Anterior:** [[Normalização]] (Aula 05 - 16.04)
**Próxima Aula:** [[]] ()
**Site:** https://sqliteonline.com/

---
# Introdução a Linguagem SQL
## Criar Tabela e Inserir em uma
```sqlite
CREATE TABLE IF NOT EXISTS Aluno1(
	Id INTEGER PRIMARY KEY AUTOINCREMENT, # Automaticamente inserido
	Nome TEXT
);

CREATE TABLE Aluno2(
	Id INTEGER,
	Nome TEXT,
	PRIMARY KEY(Id) # Não é possivel utilizar o autoincrement
);

INSERT INTO Aluno1(Nome) VALUES("João");
INSERT INTO Aluno2 VALUES(1, "Maria");
```

> **NOTA:**   `SELECT * FROM nome_tabela` mostra toda a tabela.

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

---
**tags:** #SQL #SQLite 
**Home:** [[#Aula 06 - 18.04]]
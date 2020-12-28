**MYSQL  CMDS**
```mysql
mysql -u root -p

CREATE DATABASE <dataName>;
SHOW DATABASES;
USE <database>;
CREATE TABLE <tableName>;
SHOW TABLES;
SHOW COLUMNS FROM <tableName>;

// * = ALL
SELECT * FROM <tableName>;
SELECT nom,age FROM <tableName>;
SELECT * FROM <tableName> WHERE <columnName> >= 50;

CHAR_LENGTH(<columnName>)
```

**EXEMPLES**
```mysql
CREATE TABLE <tableName>(id INT AUTO_INCREMENT, nom CHAR(60) NOT NULL, age INT NOT NULL, PRIMARY KEY(id));

INSERT INTO etudiants (nom, age) VALUES("Maxime", 23);

INSERT INTO etudiants(nom, age) VALUES("Martin", 21),("Jordano", 20);
```

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE5NTIxMDA4XX0=
-->
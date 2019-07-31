MYSQL
https://doc.ubuntu-fr.org/mysql
https://www.linuxtricks.fr/wiki/guide-commandes-de-base-sql-mysql
https://sql.sh/cours/alter-table

sudo systemctl start mysql
demarrer le daemon en mysql

arreter le serveur 
sudo systemctl stop mysql

redemarrer le serveur
sudo systemctl restart mysql

connaitre sa version de mysql

mysql --version


si vous n'avez pas de mot de passe
mysql -u root

si vous avez un mot de passe 
mysql -u root -p


creer une database
CREATE DATABASE nom_de_la_base;

utiliser/connecter une table
USE nom_de_la_base;

supprimer une database
DROP DATABASE superbase;

creer un user en localhost
CREATE USER 'utilisateur'@'localhost' IDENTIFIED BY 'motdepasse';


Attribuer les droits d'auteurs au user
GRANT ALL PRIVILEGES ON * . * TO 'utilisateur'@'localhost' IDENTIFIED BY 'motdepasse' WITH GRANT OPTION MAX_QUERIES_PER_HOUR 0 MAX_CONNECTIONS_PER_HOUR 0 MAX_UPDATES_PER_HOUR 0 MAX_USER_CONNECTIONS 0 ;


changer un mot de passe
UPDATE mysql.USER SET password=PASSWORD("nouveau") WHERE USER="utilisateur";

afficher les tables
SHOW TABLES;

renommer une table
ALTER TABLE nom_table RENAME AS nouveau_nom;

supprimer une table
DROP TABLE nom_table;


creer une table
CREATE TABLE nom_table;

mettre a jour une table

UPDATE TABLE

selectionner une table
SELECT TABLE;

rennommer une table
RENAME TABLE table1 TO table2;


exemple :
CREATE TABLE matable (
id INT(20) NOT NULL AUTO_INCREMENT COMMENT 'id, autoincrémenté',
datecreation datetime NOT NULL,
titre VARCHAR(32),
contenu text,
PRIMARY KEY (id)
) DEFAULT CHARSET=utf8;


ajouter une colonne 

ALTER TABLE matable ADD COLUMN macol;

AND pour ajouter une condition a WHERE
WHERE condition1 AND condition2

OR pour mettre une condition 1 ou 2
WHERE condition1 OR condition2

WHERE une condition sur sa requete
WHERE condition1 AND (condition2 OR condition3)


LIKE serta recherche les donnes qui contienne ce caractere.
SELECT * FROM table WHERE colonne LIKE modele


















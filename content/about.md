  MariaDB Setup Commands  body { opacity: 0; transition: opacity 0.6s ease-in-out; } body.loaded { opacity: 1; } .copy-icon { cursor: pointer; color: #3B82F6; } .copy-icon:hover { color: #1E40AF; }

![MariaDB Logo](https://pub-c1de1cb456e74d6bbbee111ba9e6c757.r2.dev/logos--mariadb-2.svg)
=========================================================================================

[MariaDB on macOS](https://mariadb.org)
---------------------------------------

[Home](dashboard.php)

MariaDB is one of the most popular open source relational databases. It was created by the original developers of MySQL and guaranteed to stay open source.

![](https://pub-c1de1cb456e74d6bbbee111ba9e6c757.r2.dev/Screenshot%202024-10-09%20at%201.42.20%E2%80%AFAM.png) 

install mariadb Database

`sudo mariadb-install-db --user=$(whoami) --basedir=$(brew --prefix mariadb) --datadir=/opt/homebrew/var/mysql`

Start Safe Mode

`cd '/opt/homebrew/opt/mariadb' ; /opt/homebrew/opt/mariadb/bin/ mariadbd-safe --datadir='/opt/homebrew/var/mysql'`

Login as User

`mysql -u supercooldev`

Login as Root

`mysql -u root -p`

Create a New Database

`CREATE DATABASE my_database;`

Use the New Database

`USE my_database;`

Create Comments Table

`CREATE TABLE comments ( id INT AUTO_INCREMENT PRIMARY KEY, user_id INT, comment TEXT NOT NULL, created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP, FOREIGN KEY (user_id) REFERENCES users(id) );`

Show Table Creation SQL

`SHOW CREATE TABLE comments;`

Set Password for User

`SET PASSWORD FOR 'supercooldev'@'localhost' = PASSWORD('PaSSword5678');`

Grant Privileges

`GRANT ALL PRIVILEGES ON my_database.* TO 'supercooldev'@'localhost';`

Delete Comments

`TRUNCATE TABLE comments;`

[MariaDB](https://server.jessejesse.xyz/maria.php)
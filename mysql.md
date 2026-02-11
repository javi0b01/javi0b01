# :memo: Notes
## MYSQL
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
### Requirements
- [SQL](./sql.md)
### Resources
- [MySQL](https://www.mysql.com/)
- [Workbench](https://www.mysql.com/products/workbench/)
- [Keywords and Reserved Words](https://dev.mysql.com/doc/refman/8.4/en/keywords.html)
#### Help
- [How to Install MySQL WorkBench on Ubuntu?](https://www.geeksforgeeks.org/how-to-install-mysql-workbench-on-ubuntu/)
- [How To Install MySQL on Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-20-04)
### Terms and concepts
- MySQL
- IDE
- MySQL Functions
- Reports
* Stored Procedures
  * Variables
    - Data types
#### Basic setup
Installing MySQL
```
$ apt-get update
$ apt install mysql-server
$ dpkg -l mysql-server
$ mysql -V
$ systemctl is-active mysql
$ systemctl status mysql.service
$ systemctl start mysql.service
$ systemctl stop mysql.service
$ systemctl restart mysql.service
$ mysql
mysql> \q
$ mysql
mysql> exit
```
Configure MySQL server
```
$ mysql_secure_installation

$ mysql
mysql> SHOW VARIABLES LIKE 'validate_password%';
mysql> SET GLOBAL validate_password.policy=<0, 1, 2>;
mysql> SET GLOBAL validate_password.check_user_name = OFF;
mysql> SET GLOBAL validate_password.length = 0;
mysql> SET GLOBAL validate_password.mixed_case_count = 0;
mysql> SET GLOBAL validate_password.number_count = 0;
mysql> SET GLOBAL validate_password.special_char_count = 0;
mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
mysql> exit
$ mysql -h localhost -u root -p
```
Workbench Installation
```
$ sudo apt-get install mysql-workbench
$ apt update
$ apt install snapd
$ sudo snap install hello-world
$ hello-world
$ sudo snap remove hello-world
$ hello-world
$ snap install mysql-workbench-community
```
#### Basic commands
Working with databases
```
mysql> SHOW DATABASES;
mysql> SELECT DATABASE();
mysql> CREATE SCHEMA <db_name>;
mysql> CREATE DATABASE IF NOT EXISTS <db_name>;
mysql> CREATE DATABASE <db_name> DEFAULT CHARACTER SET utf8;
mysql> USE <db_name>;
mysql> DROP SCHEMA <db_name>;
mysql> DROP DATABASE IF EXISTS <db_name>;
```
Working with tables
```
mysql> SHOW TABLES;
mysql> CREATE TABLE <tb_name>;
mysql> CREATE TABLE <db_name>.<tb_name>(<attributes>);
mysql> CREATE TABLE <tb_name>(<attributes>);
mysql> SHOW COLUMNS FROM <tb_name>;
mysql> DROP TABLE <tb_name>;
mysql> DROP TABLE <db_name>.<tbe_name>;
```
Working with records
```
mysql> SELECT * FROM <tb_name>;
mysql> INSERT INTO <tb_name>(<attributes>) VALUES (<values>);
mysql> UPDATE <tb_name> SET <attribute> = <new_value> WHERE <condition>;
mysql> DELETE FROM <tb_name> WHERE <condition>;
mysql> ALTER TABLE <tb_name> ADD COLUMN(<attribute> <data type>);
```
Working with keys
```
mysql> ALTER TABLE <tb_name> ADD PRIMARY KEY(<attribute>);
```
Working with SELECT
```
mysql> SELECT * FROM <tb_name>;
mysql> SELECT <attribute> FROM <tb_name>;
mysql> SELECT <attribute>, <attribute> FROM <tb_name>;
mysql> SELECT <attribute> AS <alias> FROM <tb_name>;
mysql> SELECT <attribute> FROM <tb_name> LIMIT <number>;
```
Working with filters
```
mysql> SELECT * FROM <tb_name> WHERE <condition>;
mysql> UPDATE <tb_name> SET <attribute> = <new_value> WHERE <condition>;
mysql> DELETE FROM <tb_name> WHERE <condition>;
```
## Software Developer
Built by [JAVI](https://github.com/javi0b01/) :copyright: 2024  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).

# :memo: Notes
## POSTGRESQL
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
- [postgreSQL](https://www.postgresql.org/)
- [pgAdmin](https://www.pgadmin.org/)
#### Help
- [Create local server](https://stackoverflow.com/questions/53267642/create-new-local-server-in-pgadmin)
- [How to set the default user password in PostgreSQL](https://www.atlassian.com/data/admin/how-to-set-the-default-user-password-in-postgresql)
### Terms and concepts
- PostgreSQL
- IDE
- PostgreSQL Functions
- Reports
- Stored Procedures
#### Basic setup
Ubuntu includes PostgreSQL by default
```
$ apt install postgresql
$ pg_config --version
$ psql --version
$ psql -V
$ pg_isready
$ service postgresql status
```
Enter
```
$ sudo -u postgres psql
postgres=# \l
postgres=# \conninfo
postgres=# \c template1
postgres=# \q
```
Modify password for role postgres
```
$ sudo -u postgres psql postgres
postgres=# alter user postgres with password 'postgres';
ALTER ROLE
postgres=# 
```
Basics
```
$ sudo lsof -i :5432
$ sudo ss -tlnp | grep 5432
$ sudo systemctl stop postgresql
$ sudo systemctl disable postgresql
```
## Software Developer
Built by [JAVI](https://github.com/javi0b01/) :copyright: 2020 - 2026  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).

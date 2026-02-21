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

Inside the `psql` shell, create new database:
```
postgres=# CREATE DATABASE my_new_db;
```

List all the databases to prove they exist:
```
postgres=# \l
```

Exit the `psql` shell:
```
postgres=# \q
```

Test connection string (do not docker exec into the container). Just use your normal local terminal.
```
$ psql postgresql://postgres:mysecretpassword@localhost:5432/my_new_db
```

Exit the `my_new_db` shell:
```
my_new_db=# \q
```

---

The Connection String Format  
The standard format for a PostgreSQL connection string (also called a URI) looks like this:  
postgresql://<user>:<password>@<host>:<port>/<database_name>

- <user>: The username to connect with (e.g., postgres).
- <password>: The user's password (e.g., mysecretpassword).
- <host>: The address of the database server. Since you are running it in Docker and mapped the port, your applications will use localhost.
- <port>: The port to connect to. You mapped it to 5432.
- <database_name>: This is the crucial part. This tells the server which specific database you want to connect to.

Example  
postgresql://postgres:mysecretpassword@localhost:5432/my_new_db

A Very Important Security Tip  
Using the postgres user (which is a superuser) in your applications is a major security risk. If your application is compromised, an attacker could control your entire database server.  
The best practice is to create a separate user for each application with privileges only for its own database.

Here's how you would do that from the psql shell:  
Create a separate user for each application

Create a new user for the sales app
```
postgres=# CREATE USER sales_app_user WITH PASSWORD 'a_strong_password_for_sales';
```

Give that user full control ONLY on the sales_db database
```
postgres=# GRANT ALL PRIVILEGES ON DATABASE sales_db TO sales_app_user;
```

Now, your app1 would use a much more secure connection string:  
postgresql://sales_app_user:a_strong_password_for_sales@localhost:5432/sales_db

This user cannot access inventory_db or any other database, which is much safer.

---

CREATE USER gms_user WITH PASSWORD 'a_strong_password_for_gms';
GRANT ALL PRIVILEGES ON DATABASE gms_db TO gms_user;

CREATE USER op_user WITH PASSWORD 'a_strong_password_for_op';
GRANT ALL PRIVILEGES ON DATABASE op_db TO op_user;

## Software Developer
Built by [JAVI](https://github.com/javi0b01/) :copyright: 2020 - 2026  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).

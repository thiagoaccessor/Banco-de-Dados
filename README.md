# Banco-de-Dados - Postegres

## Realização de DUMP

To perform a dump in Postgres, you can use the command-line tool "pg_dump". This tool allows you to export a database or specific tables to a file, which can then be imported into another database using the "pg_restore" tool.

For example, to dump the entire "mydb" database to a file called "mydb.sql", you would use the following command:

#//Comando:
pg_dump mydb > mydb.sql
To dump only a specific table, such as "mytable", you can use the -t option:

#//Comando:
pg_dump -t mytable mydb > mydb.sql
You can also dump a specific schema

#//Comando:
pg_dump -n myschema mydb > mydb.sql
or specific format like custom or plain

#//Comando:
pg_dump --format=c mydb > mydb.sql
It's important to note that the dump file will contain SQL commands to create and populate the database, so it should not be used to backup binary files or large object data.

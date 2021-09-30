# How to Export & Import Databases;

To Export a database, open up terminal, making sure that you are not logged into MySQL and type

```text
mysqldump -u [username] -p [database name] > [database name].sql
```

To import a database, first create a new blank database in the MySQL shell to serve as a destination for your data

```text
CREATE DATABASE test;
```

Then log out of the MySQL shell and type

```text
mysql -u [username] -p newdatabase < [database name].sql
```


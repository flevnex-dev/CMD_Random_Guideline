# Create MySQL Database on Linux using Command Line

## Step 1: Login to MySQL

```bash
sudo mysql -u root -p
```

Note: You can [change the MySQL password](ChangeMySQLPass.md) for the root user here.

## Step 2: Create a new database

```bash
CREATE DATABASE new_database_name;
```

If a database of the same name already exists, the system will not create a new database, and you will receive this error.

```bash
ERROR 1007 (HY000): Can't create database 'new_database_name'; database exists
```

You can avoid this error by using the following command. It only creates the database tutorial_database if a database of that name does not already exist.

```bash
CREATE DATABASE IF NOT EXISTS new_database_name;
```

## View All Databases

```bash
SHOW DATABASES;
```

```bash
  mysql> show databases;
        +--------------------+
        | Database           |
        +--------------------+
        | febbms             |
        | information_schema |
        | mysql              |
        | performance_schema |
        | phpmyadmin         |
        | sys                |
        | wp                 |
        +--------------------+
        7 rows in set (0.01 sec)
```

[BACK Main](db-main.md)

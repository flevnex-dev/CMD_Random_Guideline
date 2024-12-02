# Change MySQL Password for the root user

## Step 1: Login to MySQL

```bash
sudo mysql -u root -p
```

## Step 2: Switch to the appropriate database

```bash
use mysql;
```

## Step 3: Change the MySQL password for the root user

```bash
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'new_password' BY 'new_password';
```

## Step 4: Flush the privileges

```bash
FLUSH PRIVILEGES;
```

## Step 5: Once all steps are completed, exit MySQL

```bash
exit;
```

[BACK MySQL Command Line](db-mysql.md)
[BACK PostgreSQL Command Line](db-postgresql.md)
[BACK Main](db-main.md)

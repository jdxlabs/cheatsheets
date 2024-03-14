# MySQL

## Mysql cli connect
```bash
mysql -p<pass> -u<user> -h <host> -P <port> <db_name>
mysql -A -p<pass> -u<user> -h <host> -P <port> <db_name>
```

## Install tools in Debian
```bash
apt install default-mysql-client
apt install mysql-workbench
```

## Kill a process
```bash
show full processlist;
kill <processId>;
```

It's also possible to kill a process with MySQL Administrator, in Server Connections.

## Change user password
```bash
mysqladmin -u any_user -p'newpwd' password 'oldpwd'
mysqladmin -u root -p'newpwd' password 'oldpwd'
```

## Create a backup table
```sql
CREATE TABLE results_bak LIKE results;
INSERT results_bak SELECT * FROM results;
```

## Drop a table
```sql
DROP TABLE IF EXISTS results_bak;
```

## Dumps

### Dump an entire database
```bash
mysqldump -p<pass> -u<user> -h <host> -P <port> <db_name> > dump.sql
```

### Dump the structure of a database
```bash
mysqldump -p<pass> -u<user> -h <host> -P <port> --no-data <db_name> > structure.sql
```

### Dump some tables of a database
```bash
mysqldump -p<pass> -u<user> -h <host> -P <port> <db_name> \
    table1 \
    table2 \
    table3 \
     > dump.sql
```

### Import the dump in a database
```bash
mysql -p<pass> -u<user> -h <host> -P <port> <db_name> < dump.sql
```

## Usefull links
* [MySQL Documentation](https://dev.mysql.com/doc/)
* [MySQL Cheatsheet](https://devhints.io/mysql)

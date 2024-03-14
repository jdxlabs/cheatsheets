# PostgreSQL

## Install the Postgres package
```bash
apt install postgresql
```

## Connect with the cli
```bash
psql -h <hostname> -p 5432 -U <username> -d <dbname> -W
```

## List databases
```bash
\l
```

## Connect to a database
```bash
\c <dbname>
```

## List tables
```bash
\dt
```

## Dump
```bash
pg_dump -h <hostname> -p 5432 -U postgre -W -F t <dbname> > ./<dumpname>.tar
```

## Restore
```bash
pg_restore -d <dbname> ./<dumpname>.tar -c -U <username> -h <hostname> -p 5432
```

## Usefull links
* [PostgreSQL Documentation](https://www.postgresql.org/docs/)
* [PostgreSQL Cheatsheet](https://www.postgresqltutorial.com/postgresql-cheat-sheet/)

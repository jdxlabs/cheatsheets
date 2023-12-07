# PostgreSQL

## Cheatsheet

```bash

# install package
apt install postgresql

# connect
psql -h <hostname> -p 5432 -U <username> -d <dbname> -W

\l  # list databases
\c <dbname>  # connect to a database
\dt  # list tables

# dump
pg_dump -h <hostname> -p 5432 -U postgre -W -F t <dbname> > ./<dumpname>.tar

# restore
pg_restore -d <dbname> ./<dumpname>.tar -c -U <username> -h <hostname> -p 5432

```

## Links
  * [[https://dzone.com/articles/postgresql-cheat-sheet-basics|PostgreSQL Cheat Sheet: Basics]]
  * [[https://gist.github.com/Kartones/dd3ff5ec5ea238d4c546|postgres-cheatsheet.md]]




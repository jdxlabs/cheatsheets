# SQL commands

## Insert
```sql
INSERT INTO nomtable (colonne_1, colonne_2, ...)
VALUES ('valeur 1', 'valeur 2', ...);
```

## Update
```sql
UPDATE nomtable
SET champ1 = 'valeur 1', champ2 = 'valeur 2'
WHERE champ3 = 'valeur 3';
```

## Delete
```sql
DELETE FROM nomtable 
WHERE champ1 = 'valeur 1';
```

## Delete (with optimized join)
```sql
delete results
from
    results,
    (
        select id
        from results
        join feeds on feeds.id = results.feed_id and feeds.name = 'toto'
    ) t1
where t1.id = results.id;
```

## Add a column
```sql
ALTER TABLE nomtable
ADD colonne varchar(20);

ALTER TABLE nomtable
ADD colonne number(1) default 0;
```

## Delete a column
```sql
ALTER TABLE nomtable DROP COLUMN colonne;
```

## Ignore case
```sql
select nom from nomTable where REGEXP_LIKE(nomColonne,'ERi','i');

select nom from nomTable where UPPER(nomColonne) like 'ERI%'
```

## Usefull links
* [W3schools - SQL syntax](https://www.w3schools.com/sql/sql_syntax.asp)
* [Codecademy - SQL Commands](https://www.codecademy.com/article/sql-commands)

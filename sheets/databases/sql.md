# SQL

## Technos
  * [[mysql|MySQL]]
  * [[oracle|Oracle]]
  * [[plsql|PL/SQL]]
## Général


### Requête "Insert"
```sql
INSERT INTO nomtable (colonne_1, colonne_2, ...)
VALUES ('valeur 1', 'valeur 2', ...);
```

### Requête "Update"
```sql
UPDATE nomtable
SET champ1 = 'valeur 1', champ2 = 'valeur 2'
WHERE champ3 = 'valeur 3';
```

### Requête "Delete"
```sql
DELETE FROM nomtable 
WHERE champ1 = 'valeur 1';
```

### Requête "Delete" avec un join (optimisé)
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

### Ajouter une colonne
```sql
ALTER TABLE nomtable
ADD colonne varchar(20);

ALTER TABLE nomtable
ADD colonne number(1) default 0;
```

### Supprimer une colonne
```sql
ALTER TABLE nomtable DROP COLUMN colonne;
```

### Ne pas prendre en compte la casse
```sql
select nom from nomTable where REGEXP_LIKE(nomColonne,'ERi','i');

select nom from nomTable where UPPER(nomColonne) like 'ERI%'
```

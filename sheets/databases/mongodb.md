# MongoDB

[[http://docs.mongodb.org/manual/reference/sql-comparison|SQL comparison]]

## Basic commands
```bash
mongo
mongo dbname
show dbs
use dbname
show collections
```

## Create a collection
```bash
db.createCollection("collectionName")
```

## List documents in a collection
```bash
db.collection.find()
db.collection.find({'id': '210228'})
```
## Add a document into the collection
```bash
db.collection.save({country:"England",GroupName:"D"})
```

## Delete all documents of a collection
```bash
db.collection.remove({})
```

## Delete a collection
```bash
db.collection.drop()
```

## Install MongoDB tools
```bash
brew list | grep mongodb-database-tools
brew tap mongodb/brew
brew install mongodb-database-tools
```


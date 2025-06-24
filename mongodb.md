# :memo: Notes
## MongoDB
### Learn
1. What is it
2. What does it do
3. Why to use it
4. Getting started
5. Concepts
6. Code samples
7. Documentation
### Resources
- [MongoDB](https://www.mongodb.com/)
- [MongoDB Documentation](https://www.mongodb.com/docs/)
- [Install MongoDB Community Edition on Ubuntu](https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-ubuntu/#install-mongodb-community-edition-on-ubuntu)
- [MongoDB CRUD Operations](https://www.mongodb.com/docs/manual/crud/#mongodb-crud-operations)
### Terms and concepts
- MongoDB Editions
- MongoDB Shell
- MongoDB Compass
- MongoDB Atlas
* MongoDB
  - Based on JS
  - BSON format (Binary Script Object Notation)
  * Documental (records)
    - Collections (tables)
    - 16Mb limit

* Database
  * Collections
    - Documents

- MQL | MongoDB Query Language

- adding new documents
- finding documents
- sorting
- limiting data
- nested
- operators
- complex queries
- $in & $nin
- querying arrays
- deleting documents
- updating documents

- Drivers
- Connecting

- mongodb (node package)
* ODM
  - Mongoose
#### Commands
Service
```
$ mongod --version
$ sudo systemctl start mongod
$ sudo systemctl daemon-reload
$ sudo systemctl status mongod
$ sudo systemctl enable mongod
$ sudo systemctl stop mongod
$ sudo systemctl restart mongod
$ mongosh
test> exit
```
Run
```
$ mongod
$ mongo
```
Basic
```
$ mongosh
> show dbs
> use <db name/new db>
> show collections
> db.<collection name>.insertOne({x: 1})
> db.<collection name>.insertMany([{a: 1}, {b: 2}, {c: 3}])
> db.<collection name>.find()
> db.<collection name>.find().pretty()
> db.<collection name>.find({_id: ObjectId("0x00")})
> db.<collection name>.updateOne({_id: ObjectId("0x00")}, {$set: {b: 20}})
> db.<collection name>.deleteOne({_id: ObjectId("0x00")})
> db.dropDatabase()
```
## Software Developer
Built by [javi](https://github.com/javi0b01/) :copyright: 2020 - 2025  
Found a bug or have an idea? [Contact me](https://www.linkedin.com/in/javi0b01/).

### Basic commands
- To start mongo
    > mongod
- To open shell
    > mongo
- Show databases
    > show  dbs
- Format data
  - db.<dbs_name>.find().pretty()
- Switch to database
    > use <dbs_name>
- To delete one
    > db.<dbs_name>.deleteOne({id: <id_number>)
- To delete in bulk
    > db.<dbs_name>.updateOne({distance: 12000}, {$set: {marker: "delete"}})
  - $set defines we need to update something in Mongo
    > db.<dbs_name>.updateMany({}, {$set: {marker: "toDelete"}})
  - try to use marker to delete data
- To insert many
    > db.<dbs_name>.insertMany([<data>])
- To find many
    > db.<dbs_name>.find({key: value}).pretty()
- To find many as array
    > db.<dbs_name>.find({key: value}).pretty()
- To find many in JS function
    > db.<dbs_name>.forEach((passengerData)=>{printjson(passengerData)})
- To replace
    > db.<dbs_name>.replaceOne({_id: ObjectId("12321#")}, {"data": value})
- To filter or projection
    > db.<dbs_name>.find({}, {name: 1, id: 0}).pretty()
- To dropDatabase
    > db.dropDatabase(). 
    - Similarly, you could get rid of a single collection in a database via db.myCollection.drop().
Starting Mongo 

>mongod --port 27017 --dbpath "C:\data\db"



Basic MongpDB Commands. 
> use database_name 

> s={Name:"Rajasekar"}
> db.testname.insert(s);

>Show dbs

### Connecting MongoDB

##Installing Mongo in Node 

>npm install mongodb -g
>cd /path/to/my/app/folder
>npm link mongodb

```

var MongoClient = require('mongodb').MongoClient;
var url = "mongodb://localhost:27017/testdatabase";


MongoClient.connect(url, function(err,db){
if(err) throw err;
console.log("DB Created");
db.close();
});

```
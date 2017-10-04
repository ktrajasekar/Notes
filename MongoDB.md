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

### Inserting OBJ in Collections

```
MongoClient.connect(url, function(err,db){
if(err) throw err;
var customersData ={Name : "Rajasekar", Empid:"548754"};
db.collection("customers").insertOne(customersData, function(err, res){
    if(err) throw err;
    console.log("one Instered Created");
    db.close(); 
}); 

});

```
### Inserting Many OBJ in Collections

```

MongoClient.connect(url, function(err,db){
if(err) throw err;
var customersData =[
    {Name : "Rajasekar", Empid:"548754"},
    {Name : "Thangavel", Empid:"548421"},
    {Name : "Prakash", Empid:"74548754"},
    {Name : "Raja", Empid:"548754"},
];
db.collection("customers").insertMany(customersData, function(err, res){
    if(err) throw err;
    console.log("No Of docs instered - " + res.insertedCount);
    db.close(); 
    }); 
});

```

### Finding in Collections

```
db.collection("customers").findOne({}, function(err, result){
    if(err) throw err; 
    console.log(result.Name);
    db.close;

});

```
```
db.collection("customers").find({}).toArray(function(err, result){
    if(err) throw err; 
    console.log(result);
    db.close;

});
```


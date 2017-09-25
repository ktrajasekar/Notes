# Notes

## Add ssh using CLI

``` 
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

##### Watch Function example
```
$scope.$watch(function() {
return $scope.name;
}, function(newValue, oldValue) {
console.log("change detected: " + newValue)
});
``` 
##### Highlight active navigation 
```
<body ng-controller="MainCtrl">
<ul class="menu">
<li ng-class="menuClass('persons')"><a href="#!persons">Home</a></li>
<li ng-class="menuClass('help')"><a href="#!help">Help</a></li>
</ul>
...
</body>
```

```
app.controller("MainCtrl", function($scope, $location) {
$scope.menuClass = function(page) {
var current = $location.path().substring(1);
return page === current ? "active" : "";
};
});

```

##Commit all messages in Git 

```
git commit --amend -m "New commit message"

git push --force origin <BRANCH-NAME>

```

and Thats it!

Cheers!!

NodeJS

### ASYNC and SYNC in NodeJS

```
var fs = require("fs");

// Asynchronous read
fs.readFile('input.txt', function (err, data) {
   if (err) {
      return console.error(err);
   }
   console.log("Asynchronous read: " + data.toString());
});

// Synchronous read
var data = fs.readFileSync('input.txt');
console.log("Synchronous read: " + data.toString());

console.log("Program Ended");

```
### Write Stream in NodeJS

````
var http = require("http");
var fs = require("fs");

var data = 'Simply Easy Learning';
var writerStream = fs.createWriteStream('test.txt');
  writerStream.write(data, 'UTF8');
  writerStream.end();
writerStream.on('finish', function(){
  console.log("write completed");
});

```

### Write Fn in NodeJS

```
var fs = require("fs");

console.log("Going to write into existing file");
fs.writeFile('input.txt', 'Simply Easy Learning!',  function(err) {
   if (err) {
      return console.error(err);
   }
   
   console.log("Data written successfully!");
   console.log("Let's read newly written data");
   fs.readFile('input.txt', function (err, data) {
      if (err) {
         return console.error(err);
      }
      console.log("Asynchronous read: " + data.toString());
   });
});

```

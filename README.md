# Notes-

## Add ssh using CLI

ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

## Watch Function example
```
$scope.$watch(function() {
return $scope.name;
}, function(newValue, oldValue) {
console.log("change detected: " + newValue)
});
``` 

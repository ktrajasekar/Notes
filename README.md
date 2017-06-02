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

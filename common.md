```

/* Test Services */

 myApp.controller('testservices', ['$scope', '$state', 'MainService','GlobalModel', function($scope, $state, MainService, GlobalModel) {
     
            var config = {
        headers: {
            'Accept': 'application/json;odata=verbose'
        }
    };
     
      MainService
          .getServiceData('http://www.omdbapi.com/?t=' + 'Mission', config)
          .then(function () {
            populateData();
        });
     
     MainService
     .postServiceData('http://jsonplaceholder.typicode.com/posts', {
         id: 150,
         text: "Hello"
     }, {}).then(function() {
         populateData();
     })
     
   function populateData() {
        $scope.TitleM = GlobalModel.getSuccessData;
        $scope.SuccessPostData = GlobalModel.postSucessData;
    }
    populateData();
    
 }]);
 
 ```
 
 -------------------------------------
 
 -------------------------------------
 
 ```
 
 // Common Model 

myApp.factory('MainService', function ($http, GlobalModel) {
    return {
        getServiceData: function (url, config) {
            return $http.get(url, config).then(function (response) {
                console.log('Data received');
                GlobalModel.getSuccessData = response.data;
            });
        },
        postServiceData: function (url, dataParameters, config) {
            return $http.post(url, dataParameters, config).then(function (response) {
                console.log("Post Data Success");
                GlobalModel.postSucessData = response.data;
            });
        }
    }
});

myApp.factory('GlobalModel', function () {
    return {};
});

```

### Backbone Ajax Call 

```
//definitions
var MyModel = Backbone.Model.extend({});
var MyCollection = Backbone.Collection.extend({
    model:Model
});

//wherever you need a collection instance
collection = new MyCollection();

//wherever you need to do the ajax
Backbone.ajax({
    dataType: "jsonp",
    url: "https://api.twitter.com/1/statuses/user_timeline.json?include_entities=true&include_rts=true&screen_name=twitterapi&count=25",
    data: "",
    success: function(val){
        collection.add(val);  //or reset
        console.log(collection);
    }
});

```

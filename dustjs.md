### Dust JS Get Started 

```
<ul>
{#friends}
  <li>{name}, {age}{~n}</li>
{:else}
  <p>You have no friends!</p>
{/friends}
</ul>

```

JSON

```
  {
   friends: [
      { name: "Moe", age: 37 },
      { name: "Larry", age: 39 },
      { name: "Curly", age: 35 }
    ]
   }
```

HTML Rendered 

```
 <ul>
  <li>Moe, 37</li>
  <li>Larry, 39</li>
  <li>Curly, 35</li>
 </ul>
```

If empty JSON then {else} will excuted


BackBone Ajax Call 

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


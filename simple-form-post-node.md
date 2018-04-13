
### Input 

` <input type="text" class="mytext" required autofocus autocomplete='false'/> `

### Ajax

```javascript

$.ajax({
	url: "/anyurl",
	data: { value: $('.mytext').val() },
	method: "POST",
	success: (data) => {
		console.log(data)
		// outputs "SUCESSSSS"
	}
});

```

### Node

```javascript
const app= require('express')()    // express module
const bodyparser = require('bodyparser')  // bodyparser module
const port = process.env.port || 3000    // port
 
// some middleware options for bodyparser
app.use(bodyparser.json())        
app.use(bodyparser.urlencoded({ extended: false }))
 
// Express route to the url we provided in the ajax method
app.post('/anyurl/', (req, res) => {
	console.log(req.body.value)
	// outputs input's value
	res.json("SUCESSSSS")   // send the response in the form of json
})
 
app.listen(port, () => {
	console.log('App running..')
}) 

```

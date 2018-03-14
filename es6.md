## ES6

### Variables
#### block-scoped variables
*const, let and var*
 - Var - Not an block level variable
 -  let - block level variable

Example : block-scoped variables
Var - Not an block level variable

```javascript

    function vartesting(){
    var testvar = 'Rajasekar',
    Today = 'monday';
    if(Today === 'monday'){
    	var testvar = "Prakash";
    	console.log('My Name ' + testvar);
    }
    console.log('My Name ' + testvar)
    }
  ```
o/p

    My Name Prakash
    My Name Prakash

Example : Let

```javascript

 function vartesting(){
        let testvar = 'Rajasekar',
        Today = 'monday';
        if(Today === 'monday'){
        	let testvar = "Prakash";
        	console.log('My Name ' + testvar);
        }
        console.log('My Name ' + testvar)
        }
   ```
o/p

    My Name Prakash
    My Name Rajasekar
const
Example : 

    const pi = 3.14159265359;

### promise in ES6
Promises — resolve/reject/.then: Promises became less clunky too. The resolve/reject feature is pretty cool (resolve = do this when the promise is resolved, reject = do this if there is an error and the function is rejected). Plus there’s ‘.then’ — this is saying ‘when you’re done and have all the information you need, then do this.’ This allows you to not have to pass in a parameter to the function that takes care of what happens when the promise has been fulfilled.

### Default Parameters in ES6

> Arrow function

```javascript

let mul = (num1, num2) => console.log(num1 * num2);

```
o/p : 
mul(10,10);
> 100

> Arrow function with default parameters 

```javascript

let mul = (num1, num2=10) => console.log(num1 * num2);

```

o/p : 
mul(10);
> 100



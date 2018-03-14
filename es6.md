## ES6

### Variables
#### block-scoped variables
*const, let and var*
 - Var - Not an block level variable
 -  let - block level variable

Example : block-scoped variables
Var - Not an block level variable

    function vartesting(){
    var testvar = 'Rajasekar',
    Today = 'monday';
    if(Today === 'monday'){
    	var testvar = "Prakash";
    	console.log('My Name ' + testvar);
    }
    console.log('My Name ' + testvar)
    }
o/p

    My Name Prakash
    My Name Prakash

Example : Let    

    function vartesting(){
        let testvar = 'Rajasekar',
        Today = 'monday';
        if(Today === 'monday'){
        	let testvar = "Prakash";
        	console.log('My Name ' + testvar);
        }
        console.log('My Name ' + testvar)
        }

o/p

    My Name Prakash
    My Name Rajasekar
const
Example : 

    const pi = 3.14159265359;

### promise in ES6
Promises — resolve/reject/.then: Promises became less clunky too. The resolve/reject feature is pretty cool (resolve = do this when the promise is resolved, reject = do this if there is an error and the function is rejected). Plus there’s ‘.then’ — this is saying ‘when you’re done and have all the information you need, then do this.’ This allows you to not have to pass in a parameter to the function that takes care of what happens when the promise has been fulfilled.

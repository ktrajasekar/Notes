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

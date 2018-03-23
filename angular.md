## Creating the component

```
import { Component } from '@angular/core';
Then create the class for your component:

class AppComponent {
  title:string = 'hello app';
}
Then decorate your class using the Component decorator:

@Component({
  selector: 'app',
  template: `<h1>{{ title }}</h1>`
})
export class AppComponent {  
  title: string = 'hello app';
}
```

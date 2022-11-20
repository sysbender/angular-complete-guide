


* components , databinding
* directives
* services and dependency injection
* routing - url
* observables - async
* forms
* pipes -output
* http - server DB
* authentication
* optimizations, ngModules
* deployment
* animations and testing
* 
* 

```javascript
$s=a

```

### bootstrap

```js
npm install --save bootstrap@3
#angular.json
"styles":[
"node_modules/bootstrap/dist/css/bootstrap.min.css",
"src/styles.css"
]

/*
ng serve
check html source
there is styles.css is used
*/

```
### how angular load and start app
* ng server load index.html ( inject some script js file)
* index.html has a app-root tag, created by angular/cli
* component - selector to a app-xxx tag in the config file

* main.js - bootstrap a module
* in xxx.module.ts - bootstrap a component

### ngmodule
is a empty class, with 
* import line on top -  where to find the code of the co
* NgModule decorator
* 4 properties
  * declarations - register all the component
  * imports - add other modules 
  * providers - service
  * bootstraps - which component in the index html?


### component
* selector -  in file,  routing 
  * could be element or attribute
    * element -  'app-server'
    * attribute - '[app-server]'
    * class - '.app-server'
    * not ID, psydo
    
  
* template - external file or inline  (use ` for multiple line string)
* style - extenal file or inline
* 






create component
* ng generate component servers
* manually 
  * create folder 
  * create files - .component.html, .component.ts
  * update app.module.ts - add import, declaration


# data binding

output : TS -> html

```js
// string interpolation 
{{data}}

// property binding
[property] = "data"

```

react to user event : event binding
```js
(event) ="expression"
```

two way binding
```js
 [(ngModel)] ="data"
```

### directives
 are instructions in the DOM
 * built-in 
 * custom
  
* structural directive - add or remove content
* attribute directive - change the element (like a normal attribute, without a star)


 typically add custom directive with attribute selector

 * selector - add content to html
 * component - is also directive


```js

<p appTurnGreen> receives a green background! </p>


@Directive({
    selector: '[appTurnGreen]'
})


export class TurnGreenDirective{
    ...
}
```
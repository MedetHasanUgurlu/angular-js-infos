# Angular js notes

``` html
<html ng-app>
<head>
    <title>
    Angular js notes
    <title>   
<head>

<body ng-init = "name='Medet'">
    <div ng-hide = "isHidden">
            Name: <input type="text" ng-model="name"/> {{name}}
    </div>
    Hide: <input type="checkbox" ng-model="isHidden"/>
    </br>
    <button ng-click="name='Michellengo'">Change name</button>
    
    ******************
    <div ng-init= "data= {name:'Medet', isVisible:true}">
       <div ng-switch-on="data.isVisible"
            <div ng-switch-when="true">
                Welcome {{data.name}}
            </div>
        </div>
    </div>    
    
  ***********************
  
  
  // Iterating
  
  <div ng-init= "names = ['foo','bar','baz']">
    <div>
        <li ng-repeat= "name in names">{{name}}</li>
    </div>
    // Result foo
              bar
              baz
  </div>
    <script src="angular.js"></script>
<body>
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
```
### Filters and pipes
Uses | 

* currency
* data
* filter
* json
* limitTo
* lowercase
* number
* orderBy
* uppercase


``` angular2html
<ul>
    <li data-ng-repeat="cust in customers | orderBy:'name'">
        {{cust.orderTotal | currency}}
    </li>

</ul>

```

#### filtering data
``` angular2html
<input type= "text" data-ng-model= "nameText"/>
<ul>
    <li data-ng-repeat = "cust in customers | filter:nameText | orderBy:'name'">
    {{cust.name}}- {{cust.city}}</li>
</ul>   

```


#### creating controller
``` angular2html
<input type= "text" data-ng-model= "nameText"/>
<script>
    function SimpleController($scope){
        $scope.customers = [{name:'Medet',surname:'Ugurlu'},{name:'Medet',surname:'Ugurlu'},{name:'Medet',surname:'Ugurlu'}];
       
    }
</script>   



```
``` angularjs
<div ng-controller = "Customer Controller  as ctrl">
<input type= "text" data-ng-model= "nameText"/>
<div ng-repeat = "cust in ctrl.customers"></div>
<script>
    function SimpleController(){
        this.customers = [{name:'Medet',surname:'Ugurlu'},{name:'Medet',surname:'Ugurlu'},{name:'Medet',surname:'Ugurlu'}];
    }
</script>   
</div>

```

* ya scope kullan ya da this
``` angularjs
var demoApp = angular.module('demoApp',[]);
var demoApp = angular.module('demoApp',['helperModule']);
```
### module controller ekleme

``` angularjs
var demoApp = angular.module('demoApp',[]);
demoApp.controller('SimpleController',function($scope){
this.customers = [{name:'Medet',surname:'Ugurlu'},{name:'Medet',surname:'Ugurlu'},{name:'Medet',surname:'Ugurlu'}]
})

```





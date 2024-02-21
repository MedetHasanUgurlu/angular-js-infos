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


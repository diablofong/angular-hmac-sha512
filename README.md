# angular-hmac-sha512

AngularJS Module. that integrate cryptography functionality offers from the [crypto-js](https://code.google.com/p/crypto-js/) project. A Simple Service to Encrypt Use Hmac-sha512.

#required

- [AngularJS 1.1.4 + ](http://angularjs.org/) (tested with 1.3.9)

#install(bower)

* bower install angular-hmac-sha512

```html
<script type='text/javascript' src="[bower_components/]angular-hmac-sha512/src/angular-hmac-sha512.js"></script>
```

#install(manual)

* download [angular-hmac-sha512.js file](https://github.com/diablofong/angular-hmac-sha512/blob/master/src/angular-hmac-sha512.js)
* added javascript file to your app html file

```html
<script type='text/javascript' src="src/angular-hmac-sha512.js"></script>
```

#usage

- add encrypt module to angular

```javascript
 var myApp = angular.module('app', ['angular-hmac-sha512']); 
```
- set Secret in config or controller

```javascript
 //in config
 angular.module.('app').config(['$crypthmacProvider', 	function($crypthmacProvider){
   		$crypthmacProvider.setCryptoSecret('jfoiwjfwoifje83');
 });
 
 //in controller
 App.controller('demo_nosecret',['$scope','$crypthmac',function($scope,$crypthmac){
	$scope.execute = function () {
		var encrypttext = $crypthmac.encrypt($scope.plantext,"");
	};
}]);
```
-  example to use encrypt

```javascript
 //in controller
 App.controller('demo_nosecret',['$scope','$crypthmac',function($scope,$crypthmac){
	$scope.execute = function () {
		var encrypttext = $crypthmac.encrypt($scope.plantext,"");
		console.log(encrypttext);
	};
}]);
```

#demo

###[demo site](http://diablofong.github.io/angular-hmac-sha512/)

#License

###The MIT License (MIT)

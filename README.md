#jcache

##What is it?
Use jcache as a proxy to localStorage. It contains many useful methods not part of localStorage.

##Usage
jscache is dependant on JSON-js, you only need [json2.js](https://github.com/douglascrockford/JSON-js/blob/master/json2.js)

###Set
```javascript
jcache.set( 'somekey', 'some value' );
```
###Get
```javascript
if ( jcache.has( 'somekey' ) {
    value = jcache.get( 'somekey' );
}
```
###Copy
```javascript
jcache.copy( 'somekey', 'newkey' );
```
###Rename
```javascript
jcache.rename( 'somekey', 'newkey' );
```
###Delete
```javascript
jcache.remove( 'somekey' );
```
###Clear all cache
```javascript
jcache.clear();
```

###Storing objects
```javascript
var obj = { key: 'myvalue' };
jcache.set( 'myobject', obj );
```
###Get object
```javascript
var obj = jcache.get( 'myobject' );
alert( obj.key ); // alerts 'myvalue'
```
###Set expiration time
```javascript
var today = new Date();
var tomorrow = new Date();
tomorrow.setDate( today.getDate() + 1 );
jcache.set( 'myobject', obj, {expiry: tomorrow} );
```
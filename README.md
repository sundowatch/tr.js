### Features

- Simple variable operations :tw-2705:
- Tested Functions :tw-2705:
- Used on dozens of projects :tw-1f4aa:
- Easy to use :tw-1f44d:
- For JavaScript lovers :tw-1f609:

# Truncgil JavaScript Library

![](https://www.truncgil.com.tr/tr.png)


Usage
=============
Download and include truncgil.js with `<script>` tag
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Truncgil.js</title>
</head>
<body>
	<script type="text/javascript" src="truncgil.js"></script>
	<script type="text/javascript">

	</script>
</body>
</html>
```

Functions
-------------

###replaceAll
----
Replaces all matched values even if it's non string type.
```javascript
let val = _('asdasd');
console.log(val.replaceAll('a','www'));		// wwwsdwwwsd
let val = _(123123);
console.log(val.replaceAll(1, 5));		// 523523
let val = _(['lorem', 'ipsum', 'dolor', 'sit', 'amet']);
console.log(val.replaceAll('e','T'));		// [ 'lorTm', 'ipsum', 'dolor', 'sit', 'amTt' ]
let val = _( {a: 'lorem', b: 'ipsum'} );
console.log(val.replaceAll('e', 'T'));		// { a: 'lorTm', b: 'ipsum' }
let val = _( true );
console.log(val.replaceAll(true, false));	// false
```
###typeof
----
Returns specified detailed type of variable
```javascript
console.log( _('asd').typeof() );		// string
console.log( _(1234).typeof() );		// integer
console.log( _(123.5).typeof() );		// float
console.log( _([ 'asd', 123 ]).typeof() );		// array
console.log( _({ a: 'asd', b: 123} ).typeof() );		// object
console.log( _(true).typeof() );		// boolean
console.log( _(null).typeof() );		// null
console.log( _(undefined).typeof() );		// undefined
```

###typeofBlank
----
Returns Blank object for easy equality
```javascript
console.log( _('asd').typeofBlan() );		// ''
console.log( _(1234).typeofBlank() );		// 0
console.log( _(123.5).typeofBlank() );		// 0
console.log( _([ 'asd', 123 ]).typeofBlank() );		// []
console.log( _({ a: 'asd', b: 123} ).typeofBlank() );		// {}
console.log( _(true).typeofBlank() );		// True
console.log( _(null).typeofBlank() );		// null

let a = [ 'asd', 'qwe', 123 ];
if( _(a).typeofBlank === []){
	console.log( 'YES' );		// YES
}
```

###parseAll
----
Parses variable to all combinations
```javascript
console.log( _(123.45).parseAll() );
/*
{
	integer: 123
	int: 123
	float: 123.45
	string: "123.45"
	str: "123.45"
	array: [123.45]
	arr: [123.45]
	arrayInteger: [123]
	arrayFloat: [123.45]
	arrayString: ["123.45"]
	object: {value: 123.45}
	obj: {value: 123.45}
}
*/
```
###reverse
----
Reverses everything :tw-1f606:
```javascript
console.log( _('asd').reverse() );		// dsa
console.log( _(123456).reverse() );		// 654321
console.log( _(['a','b','c']).reverse() );		// ['c','b','a']
console.log( _(true).reverse() );		// false
```

###slugify
----
Return slug value of text
```javascript
console.log( _('SLugify Slug').slugify() );		// slugify-slug
```

###pushIfNotExists
----
Push Element to Array if not exists
```javascript
let arr = ['asd', 'qwe', 'zxc'];
console.log( _(arr).pushIfNotExists('asd') );		// ['asd', 'qwe', 'zxc']
console.log( _(arr).pushIfNotExists('aaa') );		// ['asd', 'qwe', 'zxc', 'aaa']
```

###toArray
----
Converts an Object to Array
```javascript
let obj = { a: 'asd', b: 'qwe' };
let arr = _(obj).toArray();		['a': 'asd', 'b': 'qwe']
console.log(arr['a']);		//asd
```

###toObject
----
Converts an Array to Object
```javascript
let arr = [];
arr['a'] = 'asd';
arr['b'] = 'qwe';
let obj = _(arr).toObject();		{'a': 'asd', 'b': 'qwe'}
console.log(obj.a);		//asd
```

###wordCount
----
Returns count of words in a sentence
```javascript
let sentence = 'Lorem ipsum dolor sit amet';
console.log( _(sentence).wordCount() );		//5
```

###wordCount
----
Returns count of words in a sentence
```javascript
let sentence = 'Lorem ipsum dolor sit amet';
console.log( _(sentence).wordCount() );		//5
```

###sleep
----
In `async` functions delays next process in given time
```javascript
(async () => {
    await console.log('Hello');
    await res.sleep(5000);				// delay 5 seconds
	await console.log('world');
})();
```

###printExecutionTime
----
In `async` functions delays next process in given time
```javascript
(async () => {
    await console.log('Hello');
    await res.sleep(5000);				// delay 5 seconds
	await _().printExecutionTime();			// Execution Time: 5083ms
})();
```

###getUnique
###log









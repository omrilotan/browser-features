# Detect syntax support


Example using destructuring assignment syntax: rest arguments
```js
const supportsES6 = function() {
	try {
		eval('const o={a:1},{a,...r}=o;');
		return true;
	} catch (_) {
		return false;
	}
}()
```

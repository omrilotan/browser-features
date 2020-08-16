# Cookie string as object

```js
const cookies = Object.fromEntries(
	document.cookie
		.split('; ')
		.filter(Boolean)
		.map(
			i => i.split('=')
		)
);
```

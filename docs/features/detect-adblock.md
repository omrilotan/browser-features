# Detect Adblocker

```js
/**
 * Check if there is, probably, an AdBlocker installed
 * @returns {Promise<boolean>}
 */
const adblocked = new Promise(resolve => {
	const img = new Image();
	img.onload = () => resolve(false);
	img.onerror = () => resolve(true);
	img.src = 'https://ads.google.com/home/static/home/images/gads_logo.gif';
});
```

Usage
```js
(async() => {
	const blocked = await adblocked();
	const meta = document.createElement('meta');
	meta.setAttribute('name', 'probably-adblocked');
	meta.setAttribute('content', blocked.toString());
	document.head.appendChild(meta);
})();
```

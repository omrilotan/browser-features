# Detect mobile browsers without user agent string parsing

```js
const uaDataIsMobile = window.navigator.userAgentData?.mobile
const isMobile = typeof uaDataIsMobile === 'boolean'
	? uaDataIsMobile
	: legacyIsMobileCheck(window.navigator.userAgent)

function legacyIsMobileCheck (useragentstring) { ... }
```

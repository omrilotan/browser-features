# Check web app installation state

Installed web app
```js
window.chrome?.app?.isInstalled === false
```

CSS Query
```js
window.matchMedia('(display-mode:standalone)').matches === false
```

Running state of the app
```js
(window.chrome?.app?.runningState() ?? '') === window.chrome?.app?.RunningState?.CANNOT_RUN
```
Options: `'cannot_run'`, `'ready_to_run'`, `'running'`

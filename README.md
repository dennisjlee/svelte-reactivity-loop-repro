# To reproduce the bug

* Initialize packages
```bash
npm i
```
* Start the app
```bash
npm run dev -- --open
```

* Navigate to /foo by clicking the link.
* Note that the page loads correctly via SPA
* Refresh the page so that it renders via SSR

Expected: the page should load

Actual: the SSR goes into an infinite loop (the terminal will show an endless
loop of console.logs)

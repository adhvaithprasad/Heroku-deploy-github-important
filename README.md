# Heroku-deploy-github-important
Important files I have to use to be able to deploy node.js application every time to heroku via github

make sure to include a package.json file with command

 
```
$ npm init -y
```
Procfile code
```
web: node ./app.js
```

App .js code(node.js)
```
const http = require('http')
const fs = require('fs')

const server = http.createServer((req, res) => {
  res.writeHead(200, { 'content-type': 'text/html' })
  fs.createReadStream('index.html').pipe(res)
})

server.listen(process.env.PORT || 3000)

```

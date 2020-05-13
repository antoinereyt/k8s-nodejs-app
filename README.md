Basic nodejs app based on express to learn k8s deploys.

The app:

```js
const express = require('express')
const app = express()
const port = 3000

app.get('/', (req, res) => res.send('Hello World!'))

app.listen(port, () => console.log(`Example app listening at http://localhost:${port}`))
```

# Test the image

build the image

```bash
docker build -t antoiner/k8s-nodejs-app .

Step 1/6 : FROM node
 ---> a511eb5c14ec
...
Successfully built 927d3c26133b
```

Run it

```bash
docker run -p 3000:3000 -it antoiner/k8s-nodejs-app
```
make server directory 

make package.json file in new directory with following: 

```
{
    "name": "devops-project2",
    "version": "1.0.0",
    "description": "Node express with Docker",
    "author": "Isac Haglund <isacha@kth.se>",
    "main": "server.js",
    "scripts": {
        "start": "node server.js"
    },
    "dependencies": {
        "express": "^4.17.3"
    }
}

```


run npm install 

run express install 

create file called server.js containing: 

"use strict";

const express = require("express");

// Constants
const PORT = 8080;
const HOST = "0.0.0.0";

// App
const app = express();
app.get("/", (req, res) => {
  res.send("Hello World");
});

app.listen(PORT, HOST);
console.log(`Running on http://${HOST}:${PORT}`);


running npm start should print "Running on http://0.0.0.0:8080"

# Express Notes

### References

1. [Express JS Website](https://expressjs.com/)
2. [Hello World Example](http://expressjs.com/en/starter/hello-world.html#hello-world-example)

---

### Topics Covered

1. Creating an Express Server
2. Responding with HTML files

---

## Creating an Express Server

### `Step 1`

Create a server.js file

### `Step 2`

Run `npm init` command

### `Step 3`

Run `npm install express` command

### `Step 4`

Create `const express = require("express");`
* Incorporate express to server.js file

### `Step 5`

Create `const app = express();`
* A function that represents the express module
* Bind it to the word app

### `Step 6`

Create `const port = 3000;`
* Port number

### `Step 7`

Call `app.listen(port)`
* Listen to this port for any http request that get sent to this server
* Server will tune into the channel `port`

### `Step 8`

On browser type `localhost:3000`
* Browser makes get request will see `Cannot GET /`

---

## Responding with HTML Files

### `Step 1`

Use respond.sendFile()
* __dirname is a constant that will with return string of pwd

```javascript
app.get("/", function(req, res){
    res.sendFile(__dirname + "/index.html");
})
```

### `Step 2`

If using form than action needs to get changed to "/"
* To instead send form data to the server
* Sends data to "home route" -> "/"
* Gives home route "server" access to data

```javascript
<form action="index.html"></form>
// Change to this
<form action="\"></form>
```

### `Step 3`

Add app.post() method

```javascript
app.post("/", function(req, res){
    res.send("Thanks for posting that!");
})
```

### `Step 4`

Run `npm install body-parser` command
* Adds body-parser dependency

### `Step 5`

Add bodyParser through require and app.use()

```javascript
const bodyParser = require("body-parser");
app.use(bodyParser.urlencoded({extended: true}));
```

### `Step 6`

Use req.body to access data within app.post()
* Forms: Data will be in array

```javascript
req.body // Returns array
req.body.num1 // Returns data stored in num1
```


## `Other Notes`

HTTP codes cheat sheet:

1. Hold on
2. Here you go
3. Go away (Security)
4. You fucked up (error)
5. I fucked up (error)
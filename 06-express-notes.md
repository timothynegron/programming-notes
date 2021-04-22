# Express Notes

### References

1. [Express JS Website](https://expressjs.com/)
2. [Hello World Example](http://expressjs.com/en/starter/hello-world.html#hello-world-example)
3. [HTTP response status code](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status)
4. [HTTP Status Dogs](https://httpstatusdogs.com/)

---

### Topics Covered

1. Creating an Express Server
2. Responding with HTML files
3. Making GET Request with Node HTTPS Module

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

## Making GET Request with Node HTTPS Module

### `Step 1`

Create variable to hold native https library
* HTTPS is a native module
* Making a get request across the internet using the HTTP protocol

```javascript
const https = require("https");
```

### `Step 2`

Call `https.get()`

```javascript
app.get("/", function(req, res){

    const url = "https://api.openweathermap.org/data/2.5/weather";

    //
    https.get(url, function(response){
        console.log(response.statusCode)
    })


    res.sendFile(__dirname + "/index.html");
})
```

### `Step 3`

Use response.on() to get data

```javascript
// Fetch from external server
    https.get(url, function(response){
        console.log(response.statusCode)

        response.on("data", function(data){

            // Convert data from HEX to JSON
            const weatherData = JSON.parse(data)

            // Collect data of interest
            const temp = weatherData.main.temp;
            const feelsLike = weatherData.main.feels_like;
            const weatherDescription = weatherData.weather[0].description;
            
            // Response to give the browser
            res.send("<h1>The temperature in New York is " + temp + " degrees Fahrenheit</h1>")
        })
    })
```


## `Other Notes`

HTTP codes cheat sheet:

1. 100 - 199: Hold on (Informational responses)
2. 200-299: Here you go (Successful responses)
3. 300-399: Go away (Security) (Redirects)
4. 400-499: You fucked up (error) (Client errors)
5. 500-599: I fucked up (error) (Server errors)

* HTTP code 200: Successful response
* HTTP code 404: Resource not found (Could mean typo on url)
* HTTP code 401: Unauthorized HTTP request (Could mean wrong API key)

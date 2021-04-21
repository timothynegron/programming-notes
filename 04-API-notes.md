# API notes

### References

1. [Postman](https://www.postman.com/)
2. [OpenWeatherMap](https://openweathermap.org/)
3. [JokeAPI](https://sv443.net/jokeapi/v2/)
4. [JSON Viewer Pro](https://chrome.google.com/webstore/detail/json-viewer-pro/eifflpmocdbdmepbjaopkkhbfmdgijcc)

### Topics Covered

1. APIs
2. API endpoint, paths, and parameters
3. API Authentication and Postman
4. JSON
5. Putting APIs into Practice

### API's

An Application Programming Interface (API) is a set of commands, functions, protocols, and objects that programmers can use to create software or interface with an external system.

* Allows developers to access certain data.

* Gives developers functions, protocols, etc, things to use to access that data.

* Programmers use APIs to create software or interact with an external system.

![alt API picture](assets/apis.png )


### API endpoint, paths, and parameters

Endpoint - Every API that interacts with external systems, like a server, will have an endpoint. After the endpoint you can enter parameters.

Example:

```javascript
api.openweathermap.org/data/2.5/weather
```

Paths | Parameters - use in order to narrow down on a specific piece of data you want to use from an external server. Through the use of path and parameters you can get what data you want from the API.
* Parameters go at the end of a URL after a question mark
* Parameters have key value pairs: example `?contains=debugging`
* You can enter multiple parameters.
* Ampersand - & - separates key value pairs

Example:

```javascript
api.openweathermap.org/data/2.5/weather?q={city name}&appid={API key}
```

### API Authentication and Postman

Authentication - API creators will charge you more money based on your use of their API.

Postman - An application that allows you to see API request and add key-value pairs.

### JSON

JSON = JavaScript Object Notation.

Data Presented as Object.

Favored format because:
* It's lighter weight than XML and HTML.
* It's easy to turn back into a JavaScript object.

### Putting APIs into Practice


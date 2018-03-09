# Login-with-Node.js
A simple login application using Node.Js, Mongodb and Passport for authentication.
<img src="https://github.com/GhostPolymer/Login-with-Node.js/blob/master/capture1.JPG">

## There is not a www file within the bin nor a server.js file but...
 you can create your own with this little template:
## server.js:
```
var http = require('http');
var fs = require('fs');

function onRequest(request, response) {
  response.writeHead(200, {'Content-Type': 'text/html'});
  fs.readFile('./index.html', null, function(error, data) {
    if (error) {
        response.writeHead(404);
        response.write('File not found');
    } else {
        response.write(data);
    }
    response.end();
  });
}
//A request to 'listen' or get access to the port as per requested via .listen() variable
http.createServer(onRequest).listen(3000);
```

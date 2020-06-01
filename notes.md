Modules: like JS libraries-- a set of functions to include in application
    -To include a module: use require, ie http = require('http) gives access to
     http module and can create server
    -many built-in modules, such as http module
    -Can create own modules using exports.moduleName = function () {return x}
        -save this in own file, exports keyword makes it available outside module file
    
Http module    
    -http is built-in module that creates http server & allows requests & responses 
    -use createServer() to create http server
            var http = require('http');
            //create a server object:
            http.createServer(function (req, res) {
            res.write('Hello World!'); //write a response to the client
            res.end(); //end the response
            }).listen(8080); //the server object listens on port 8080
        -function in createServer will be run when someone navigates to port 8080
    -if response to request is to be displayed as html, add header using 
            writeHead(200,{'Content-Type': 'text/html'})
    -req argument in createServer() represents request from client as object 
            http.incomingMessageObject      
        -req has property called url (req.url) which holds part of url that comes after domain name: can use this to read query strings and customize
      
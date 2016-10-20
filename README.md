# remote-ip

A simple function for get the client ip on http request

#Get started


Install:

 npm install remote-ip


Usage:

    var getIp = require('remote-ip');
    
    getIp(request); //ip address
    
    
#Example:

    var http = require('http');
    
    var getIp = require('remote-ip');

    http.createServer(function(req,res){
        res.writeHead(200,{
            "content-type":"text/plain"
        });
        
        var ip = getIp(req); //your client ip
        console.log(ip);
        
        res.end();
    }).listen(3000);
    
or on express
    
    var getIp = require('remote-ip');
    
    router.get('/',function(req,res,next){
        
        var ip = getIp(req); //your client ip
        console.log(ip);
        
    });
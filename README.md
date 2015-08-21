# NodeJS

![NodeJS](http://thinking.bohdanvorona.name/wp-content/uploads/2014/07/Node_Js.png)

##What is Node.js?

* This is not a web server. It is not Apache, and not Nginx.
* It itself does absolutely nothing.
* It does not contain any config-files.
* The most important thing - it is not a programming language. <br />

> Node.js - a framework for the execution of your JavaScript code. <br />
it's just another way to execute code on your computer. And yet. <br />
Node or Node.js - a software platform based on the [V8 engine](https://code.google.com/p/v8/) <br />

The official website can be found at [nodejs.org](http://nodejs.org)

## Installing NodeJS
*Windows/Mac OS:*

* [The official website](http://nodejs.org)
    
*Debian/Ubuntu:*

    $ aptitude install nodejs

## Check and install additional modules

    $ node -v
    $ npm install nodemon -g
    $ npm install 
    
## Install Express generator and create you're first application

[Express ](http://nodejs.org) - Fast, flexible, minimalistic web framework for Node.js

    $ npm install express-generator -g
    $ express myapp
    $ cd myapp
    $ npm install
    
*For detail option use:*
    
    $ express -h
        
*To view the command options, use the -h option:*
    
    $ DEBUG=myapp nodemon ./bin/www 

# Redis

[Official site](http://redis.io/)
>Redis is an open source, BSD licensed, advanced key-value cache and store.

###Install

*Windows:*

[Download 32 or 64](https://github.com/rgl/redis/downloads)

*Debian/Ubuntu:*

    $ wget http://download.redis.io/redis-stable.tar.gz
    $ tar xvzf redis-stable.tar.gz
    $ cd redis-stable
    $ make
    
*Mac OS:*
    
    $ brew install redis
    
###Starting Redis

*Debian/Ubuntu:*

    $ redis-server
    [28550] 20 Aug 01:29:28 # Warning: no config file specified, using the default config. 
    [28550] 20 Aug 01:29:28 * Server started, Redis version 2.8.7
    [28550] 20 Aug 01:29:28 * The server is now ready to accept connections on port 6379
    ... more logs ...
    
*Mac OS:*

    $ brew services start redis
    
###Check if Redis is working
    
    $ redis-cli                                                                
    redis 127.0.0.1:6379> ping
    PONG
    redis 127.0.0.1:6379> set mykey somevalue
    OK
    redis 127.0.0.1:6379> get mykey
    "somevalue"
    
#Node-Redis-Socket.io

    $ git clone https://github.com/lifeIsGame/node-redis-socket.io
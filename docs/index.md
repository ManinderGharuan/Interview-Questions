# Nodejs

## How to handle concurrency in NodeJS?

- Nodejs can support concurrency by concept of event, callbacks, Promises and async/await.
- Nodejs uses an event loop to maintain concurrency and perform non-blocking I/O operations.

## What is Event Loop?

The event loop allows nodejs to perform non-blocking I/O operations.

- Event loop is an endless loop, which waits for tasks, executes them and then sleeps until it receives more tasks.
- Event loop execute tasks from ==event queue== only when ==call stack== is empty.
- Event loop allow us to use callbacks and promises.

<figure markdown="span">
  ![Event Loop Diagram](/images/event-loop.png)
</figure>

## What is callback hell?

- The asynchronous function requires callbacks as a return parameter.
- When multiple asynchronous functions are chained together then callback hell situation comes up.

``` js linenums="1"
getData(function(a){
    getMoreData(a, function(b){
        getMoreData(b, function(c){ Reactor Pattern in Node.js
            getMoreData(c, function(d){ 
	            getMoreData(d, function(e){ 
		            ...
		        });
	        });
        });
    });
});
```

## What is package.json file?

- The package.json file in Nodejs projects contains valuable information, such as project metadata and dependencies.
- File used to managing project modules, scripts, version control.

## What is JWT?

- JWT (JSON Web Token) is an open standard that defines a compact and self-contained way for securily transfer information as JSON object.
- JWT token can be trusted because it is digitaly signed.

## How to build a microservices architecture?

- Microservices are many small services responsible for one functionality.

<figure markdown="span">
  ![Monolithic vs Microservices](/images/monolithic-and-microservices-architecture.jpg)
</figure>

## What are the middleware functions?

- Functions that have access to the ==request object (req)==, the ==response object (res)== and the **next** function.
- Middleware can
    * Execute any code
    * Make changes to the request and response
    * End the request-response cycle
    * Call the next middleware in the stack

## How to handle cache in Nodejs?

- Cache is used to store frequently accessed data in the temporary storage.
- Redis is used to cache data in Nodejs

# Serverless

## Advantages and Disadvantages of Lambda
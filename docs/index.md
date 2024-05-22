## Nodejs

### What is package.json file?

- The package.json is a metadata file that contains information about project, such as name, description and most important dependencies.
- File used to managing project modules, scripts, version control.
- File is used by npm to install, manage, update dependencies.

### What is package.lock.json file?

- The package.lock.json file that npm generates after installing packages.
- This file contain details description of dependencies, including versions and dependencies of dependencies.

### What is preflight request?

- A preflight request is a ==CORS== request that checks to see if the CORS protocol is understood.
- Preflight is a OPTIONS request.

### Use of options method in http?

- HTTP OPTIONS method is used to request information about the communication options available for the target resource.
- Response include an header indicating allowed HTTP methods on the resource.
- HTTP OPTIONS request is automatically issued by browser.

### What is CORS?

- CORS means cross origin resource sharing.
- It is a security feature that allows the webapplications from one domain to request the resources like API's from other domain
- CORS works by adding http headers to control which origins have accesss to the resource and under what condition.

### Difference between import and require?

- Require is non-lexical, it stays where they have put the file.
- Import is lexical, it gets sorts to the top of the file.

### Nodejs is single-threaded. Can I make main thread as multi-thread?

- We can't directly convert main thread to multi-threaded execution.
- Nodejs provides mechanisms to achieve similar effects by using ==event loop== for non-blocking I/O.
- Nodejs offers experimental module called ==Worker Threads==.
- **Worker Threads** creates child processes for CPU-bound tasks, share memory with main thread, enable paraller processes.
- We can also achive this by using cluster.

### How to handle concurrency in NodeJS?

- Nodejs can support concurrency by concept of event, callbacks, Promises and async/await.
- Nodejs uses an event loop to maintain concurrency and perform non-blocking I/O operations.

### What is Event Loop?

The event loop allows nodejs to perform non-blocking I/O operations.

- Event loop is an endless loop, which waits for tasks, executes them and then sleeps until it receives more tasks.
- Event loop execute tasks from ==event queue== only when ==call stack== is empty.
- Event loop allow us to use callbacks and promises.

<figure markdown="span">
  ![Event Loop Diagram](/interview-questions/images/event-loop.png)
</figure>

### What is callback hell?

- The asynchronous function requires callbacks as a return parameter.
- When multiple asynchronous functions are chained together then callback hell situation comes up.

```js linenums="1"
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

### What is authrentication vs authorization?

- **Authentication**: is the process of verifying who the user is.
- **Authorization**: is the process of verifying what they have access to. What files and data user has access to.

### What is JWT?

- JWT (JSON Web Token) is an open standard that defines a compact and self-contained way for securily transfer information as JSON object.
- JWT token can be trusted because it is digitaly signed.

### How to build a microservices architecture?

- Microservices are many small services responsible for one functionality.

<figure markdown="span">
  ![Monolithic vs Microservices](/interview-questions/images/monolithic-and-microservices-architecture.jpg)
</figure>

### What are the middleware functions?

- Functions that have access to the ==request object (req)==, the ==response object (res)== and the **next** function.
- Middleware can
  - Execute any code
  - Make changes to the request and response
  - End the request-response cycle
  - Call the next middleware in the stack

### How to handle cache in Nodejs?

- Cache is used to store frequently accessed data in the temporary storage.
- Redis is used to cache data in Nodejs

### In microservice architecture what are the different ways to communicate between services?

### In API I have 3 database queries 2 seconds response each and API takes 6 deconds to execute. How we can optimize this?

```js
const query = () => {
  new Promise((resolve) => {
    setTimeout(resolve, 2000);
  });
};

(async () => {
  await query();
  await query();
  await query();
})(); // Response time 6 seconds
```

- We can optimize response time by using Promise.all

```js
(async () => {
  await Promise.all(query(), query(), query());
})(); // Response time 2 seconds
```

### What is Test Driven Development (TDD)?

- TDD is a software development approach where tests are written before the actual code.

### What is Behaviour-Driven Development (BDD)?

## Serverless

### Advantages and Disadvantages of Lambda?

### What is cold start in lambda?

### What is lambda layer?

- Layers usually contain library dependencies, a custom runtime, or configuration files.
- Layers can be used to reduce size of deployment, separate core function logic, share dependencies, lambda console code editor.

## Cloud Services

## Messaging queues

## CICD Tools

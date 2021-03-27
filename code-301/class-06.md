# Node, Express, and APIs
## npm
We can also install packages locally to a project, as opposed to globally, on our system.
```
npm init -y
```
This will create and auto-populate a `package.json` file in the same folder.
The node_modules folder shouldn’t be checked in to version control, and can, in fact, be re-created at any time by running npm install from within the project’s root.

## Node
Node.js is single-threaded and event-driven. For example, when a new request comes in the server will start processing it. If it then encounters a blocking I/O operation, instead of waiting for this to complete, it will register a callback before continuing to process the next event. 

When the I/O operation has finished the server will execute the callback and continue working on the original request. However when you connect to a traditional server, such as Apache, it will spawn a new thread to handle the requests.

Node is particularly suited to building applications that require some form of real-time interaction or collaboration — for example, chat sites.

### Advantages of Node.js

- do everything in the same language
- understands JSON 

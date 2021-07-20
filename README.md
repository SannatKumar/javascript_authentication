Part 1: Creating our backend
i. Initializing our project
Set the current directory to wherever you want your project to live and initialize the project using npm.
➜  ~ mkdir mern-auth
➜  ~ cd mern-auth
➜  mern-auth npm init
After running the command, a utility will walk you through creating a package.json file.
You can enter through most of these safely, but go ahead and set the entry point to server.js instead of the default index.js when prompted (can do this later in our package.json).

ii. Setting up our package.json
1. Set the “main” entry point to “server.js” instead of the default “index.js”, if you haven’t done so already (for conventional purposes)
2. Install the following dependencies using npm
➜  mern-auth npm i bcryptjs body-parser concurrently express is-empty jsonwebtoken mongoose passport passport-jwt validator
A brief description of each package and the function it will serve
bcryptjs: used to hash passwords before we store them in our database
body-parser: used to parse incoming request bodies in a middleware
concurrently: allows us to run our backend and frontend concurrently and on different ports
express: sits on top of Node to make the routing, request handling, and responding easier to write
is-empty: global function that will come in handy when we use validator
jsonwebtoken: used for authorization
mongoose: used to interact with MongoDB
passport: used to authenticate requests, which it does through an extensible set of plugins known as strategies
passport-jwt: passport strategy for authenticating with a JSON Web Token (JWT); lets you authenticate endpoints using a JWT
validator: used to validate inputs (e.g. check for valid email format, confirming passwords match)


3. Install the following devDependency (-D) using npm
➜  mern-auth npm i -D nodemon
Nodemon is a utility that will monitor for any changes in your code and automatically restart your server, which is perfect for development. The alternative would be having to take down your server (Ctrl+C) and stand it back up every time you made a change. Not ideal.
Make sure to use nodemon instead of node when you run your code for development purposes.



# Node.js e-Portfolio

Click [here](https://docs.google.com/presentation/d/1Tm1IUSWCnfUb12hg95PgUJf7wHheR3O5XdE3-fdsyPg/present?slide=id.p) to get to the slides  
Install Node.js from [nodejs.org](https://nodejs.org)

## Live-coding

We'll try to create a small webserver that prints `Hello World` using the [express](http://expressjs.com) framework

__NOTE:__ If you are using the solution I provided here, you need to install the dependencies using `npm install` for it to run!

### Step 1: Create a project

Create a new Node.js project using by running 
```
npm init
```
You will be asked to enter project information like a project name, an author, a description and so on.  
You can either fill out all information accordingly or use the predefined values by just hitting enter all the time.  
After the creation has finished, you will see a `package.json` file that contains all the information.

Next to it, __create__ an `index.js` file. It will contain our code.


### Step 2: Install the express framework

Express allows to create a simply webserver in just a few lines of code.
To install it run
```
npm install express -s
```
This will add the dependency to your `package.json` file and install the module  
into a folder called `node_modules`.  

Now we will include it in our code, so open the `index.js` file and add this line at the top
```javascript
var express = require('express');
```

### Step 3: Create the webserver
To create a webserver, we have to create a so called Express Application, which represents our server
```javascript
var app = express();
```

In order for it to run, we have to tell it to listen for connections on a specified port, e.g. 8080
```javascript
app.listen(8080);
```

### Step 4: Serve `Hello World`
Now that the server is running, we can send our message - `Hello World` - to the user
```javascript
app.get('/', function(req, res) {
    res.send('Hello World');
});
```

What this does is that as soon as a user visits our server on the main page,  
we will send a response containing the text `Hello World`.  

### Step 5: Run it
At the end, our code should look like this
```javascript
var express = require('express');
var app = express();

app.listen(8080);

app.get('/', function(req, res) {
    res.send("Hello World!");
});
```

To run it, just execute
```
node index.js
```

You should be able to view the result by visiting http://localhost:8080 in your browser.  
If so, congratulations, you just built your first webserver using Node.js and express 😊🎉


## Exercises - learnyounode
Now it's your turn!  
With the help of [learnyounode](https://github.com/workshopper/learnyounode) you can teach yourself some Node.js

Just install it using
```
npm install learnyounode -g
```

This will install `learnyounode` as commandline tool on your system.
After the installation has finished, you can run it in your shell or cmd
```
learnyounode
```

Simply select the task you want to do and follow the instructions on screen!  
Good luck 😉

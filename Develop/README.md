# Reverse_Engineering_Code

# Unit 14 Sequelize Homework: Reverse Engineering Code

Reverse engineer the starter code provided and create a tutorial for the code.

In the `Develop` folder, there is starter code for a project. Begin inspecting the code to get an understanding of each file's responsibility. Then, in a Google Doc, write a tutorial explaining *every* file and its purpose. If one file is dependant on other files, be sure to let the user know.

At the end of the tutorial, add instructions for how you could now add changes to this project.

Following the [common templates for user stories](https://en.wikipedia.org/wiki/User_story#Common_templates), we can frame this challenge as follows:

```
AS A developer

I WANT a walk-through of the codebase

SO THAT I can use it as a starting point for a new project
```

## Business Context

When joining a new team, you will be expected to inspect a lot of code that you have never seen before. Rather than having a team member explain every line for you, you will dissect the code by yourself, saving any questions for a member of your team.

## Acceptance Criteria

```md
GIVEN a Node.js application using Sequelize and Passport
WHEN I follow the walkthrough
THEN I understand the codebase

Server.js 

This file provides the code to make a call to the server using JS's express package.  We call the server and then receive a response from that call. We need to create a variable to call the express package.We also require the routes used in the app.  We also set up a port, which is used to call the server and we call a variable used to sync our models. 

html-routes.js

This route is used to connect our routes to the html files in our pulic folder. The html route responds to a particular endpoint (html) using a request method. This could be a GET, POST, PUT, and DELETE method. It then directs this request to the html page of its choice with an if statement that calls on the response received from our middleware, which in this case is the isAuthenticated middleware. 

api-routes.js

This route is used to display how an application responds to a client request from a particular endpoint/API using the 'app' express instance, which is used for running the server and initializing the different routes methods. It also interacts with the models files (index.js/user.js) to manipulate or edit the data received from the user. 

isAuthenticated.js 

This is the middleware, which is the request intercept checkpoint or stop, between the request and the database storing the data provided by the user in their request. 

config.json

This file enables the mySQL database and provides us with a connection between our app and our database in mySQL. 

package.json 

The package.json file stores all the packages used in the app. 
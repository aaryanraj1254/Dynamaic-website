<script>
app.js (Express Server)

This code sets up an Express server that listens for incoming requests and interacts with the MongoDB database using the Mongoose model.


express: a web framework for building web applications.
path: a library for working with file paths.
hbs: a templating engine for rendering HTML templates.
User: the Mongoose model defined in usermessage.js.

In short, this code is:

Serving Bootstrap and jQuery files as static resources.
Configuring Express to parse URL-encoded request bodies.
Setting up Handlebars as the view engine and configuring it to use specific directories for templates and partials.
Serving static files from a specific directory.



Setting up the Express server:
app is an instance of the Express server.
port is set to 3000 (or a custom port if specified in the environment).


Configuring middleware:
app.use() is used to add middleware functions to the Express server.
Middleware functions are executed in the order they are added.
In this case, middleware is added for:
Serving static files from the public directory.
Serving Bootstrap CSS and JS files from the node_modules directory.
Serving jQuery files from the node_modules directory.
Parsing URL-encoded request bodies.



Setting up routing:
app.get() and app.post() are used to define routes for the Express server.
In this case, two routes are defined:
A GET route for the root URL ("/") that renders the index template.
A POST route for the /contact URL that creates a new User document in the database.



Starting the server:
app.listen() is used to start the Express server.
The server listens on the specified port and logs a message to the console when started.
In summary, the usermessage.js file defines a Mongoose model for a User document, while the app.js file sets up an Express server that interacts with the MongoDB database using the Mongoose model and serves HTML templates to clients.


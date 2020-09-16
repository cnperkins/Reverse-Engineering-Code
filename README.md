Reverse Engineering Code
Description: This app allows users to create an account, log into the account and sign back out securely. All user data is stored in a mysql database.
As someone who wants to safely log in to a site, I want to know my personal information is safely stored so that I don’t have to worry about using the site.
To use this app first create a mysql db called "passport_demo".
Then go into the config file, open config.js and insert your personal data ie username, password.
Next, open the terminal and run "npm i" to install all node packages.
Next, run "node server.js".
Then, open the browser to localhost:8080.

----Technologies/Packages----
node express, 
express-session, 
mysql2,
passport,
passport-local, 
bcryptjs,
sequelize.

Files:
----config----
----middleware----
isAuthenticated.js: Restricts routes that the user is not allowed to visit if not logged in. If the user is logged in, it continues with the request.

config.json: has the connection to connect to the server.
passport.js: Has the js that tells passport we want to log in with an email address and password.
----models----
index.js: Connects to database and imports users log in.
user.js: Requires "bcrypt" for password hashing. This makes the database secure even if compromised. This also has the js that defines what is stored on our database.
----routes----
api-routes.js: Has the routes for signing in, logging out and gets users specific data to be displayed on the browser.
html-routes.js: Checks if the user is signed in or if their account exists and then sends them to the html page.
package.json: Has all of the packages info, node modules and versions.
server.js: Requires packages, sets up a PORT and heroku, creates express and middleware, creates routes and connects databases / console logs a message in the terminal when it connects to the server.

# MEAN_Authentication_Application

use npm start in the angular-src file and in the meanauthenticationapp file to load localhost ports 3000 and 4200. 3000 is for the backend and 4200 is for the front end. This is for the raw MEAN stack.

The upload of the raw files did not work for some reason so I am including a link to a Google drive folder with the files in it. Feel free to download the whole thing...

For getting the mongodb database up and running, first download mongodb here: https://www.mongodb.com/download-center.
Then navigate to your mongodb folder (please use custom install to make the file paths easier), then mongodb\bin.
Then mongod --directoryperdb --dbpath C:\mongodb\data\db --logpath C:\mongodb\log\mongo.log --logappend --install.
Then netstartMongoDB.Then mongo.
Look here for the shell commands: https://docs.mongodb.com/v3.4/reference/mongo-shell/
Look here for more info. on mongoDB quickstarting https://www.youtube.com/watch?v=pWbMrx5rVBE&t=1504s.

Look here for instructions on how to get everything installed for node.js via npm: https://www.youtube.com/watch?v=uONz0lEWft0&t=5s

Mongodb:
show dbs
use <> //whatever db you want - if it's not there it is added, and you are now in that database
db.createUser({}); - creates user with json data
db.createCollection('String'); - this makes a collection of individuals
db.customers.insert({first_name: "Josh"}); - this inserts users of first_name "Josh" into the collection customers
db.customers.find(); - prints out all of the customers
db.customers.find().pretty(); - This prints the customers out nicely
db.customers.insert([{}, {}]); - This inserts two users into the customers, with parameters defined in the {}
db.customers.remove({firstname:"Josh"}) - this removes any customers with the given parameter
db.customers.update({firstname:"Josh"}, {lastname:"Schmi"}) - this updates anyone with the first name Josh to have that last name
db.customers.update({firstname:"Josh"}, {$set:{lastname:"Schmi"}}) - this keeps whatever was there previously and adds the last name on
db.customers.update({firstname:"Josh"}, {$inc:{age:5}}) - this increments the age by 5 for all Josh's
db.customers.update({firstname:"Josh"}, {$unset:{age:1}}) - this gets rid of the age in all Josh's

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
db
show colletions

db.createUser({}); - creates user with json data
db.createCollection('String'); - this makes a collection of individuals
db.customers.insert({first_name: "Josh"}); - this inserts users of first_name "Josh" into the collection customers
db.customers.find(); - prints out all of the customers
db.customers.find().pretty(); - This prints the customers out nicely
db.customers.insert([{}, {}]); - This inserts two users into the customers, with parameters defined in the {}
db.customers.remove({firstname:"Josh"}); - this removes any customers with the given parameter
db.customers.remove({firstname:"Josh"}, {justOne: true}); - this removes just one
db.customers.update({firstname:"Josh"}, {firstname:"Josh", lastname:"Schmi"}); - this updates anyone with the first name Josh to have that last name
db.customers.update({firstname:"Josh"}, {$set:{lastname:"Schmi"}}); - this keeps whatever was there previously and adds the last name on
db.customers.update({firstname:"Josh"}, {$inc:{age:5}}); - this increments the age by 5 for all Josh's
db.customers.update({firstname:"Josh"}, {$unset:{age:1}}); - this gets rid of the age in all Josh's
db.customers.update({firstname:"Josh"}, {firstname:"Josh", lastname:"Schmi"}, {upsert: true}); - this updates Josh but if there is no Josh it makes one
db.customers.update({firstname:"Josh"}, {$rename:{age:old}}); - this changes the category of age to old of all Josh's
copy from text file to db to bulk write a lot of users with db.customers.insert([{},{},{},{},{}...]);
db.customers.find({$or:[{}, {}]}); finds customers with one parameter or the other
db.customers.find({age: {$lt: 40}}); finds customers less than 40
db.customers.find({"address.city":"Boston"}); finds in address object city of Boston
db.customers.find().sort({last_name:-1}); sorts in opposite of alphabetical order, from Z to A
db.customers.find().count(); number of people in database
db.customers.find({gender: "male"}).count(); number of people in database
db.customers.find().limit(4); prints out the first 4 in the database
db.customers.find().forEach(function(doc){print("Customer Name: " + doc.first_name)}); prints the first name for each customer

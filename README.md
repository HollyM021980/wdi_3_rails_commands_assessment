# Rails Commands Quiz

Fork, clone, and write your answers directly in this file. Then submit a pull request.

NOTE: I had to refer to my notes for exact command syntax but know the rest.
### Question 1

I want to start a new Rails project/app called `BunnyApp`. What command should I type in the terminal?

rails new BunnyApp
  OR (preferred)
rails new BunnyApp --database=postgresql -T #to define postgresql as the database and not generate the test directories

### Question 2

I want to create a new model called `Bunny`, with the following attributes: name (string), color (string), and age (integer). What command should I type in the terminal?

-- Was confused by this question
rails g migration CreateBunny name color age:integer

-- Expected: rails g model Bunny name color age:integer

### Question 3

What does the command in Question 2 do, exactly? What files are created, where are they located, and what does the database look like at this time? Explain.

This will create a timestamped migration file in the db/migrate folder of the current app which contains ruby code to create a table with the three columns listed above
There is nothing in the database at this time.

-- Expected rails g model:
--- Creates a file app/models/bunny.rb
--- This defines the Bunny as a ruby class AND creates a migration file in /db/migrate with the columns
--- and datatypes expected in the generate command

### Question 4

I want to create a database and make it reflect the new model I created in Question 2. What command(s) should I type in the terminal?

-- 1/2 credit Missing the part to create a app/models/bunny.rb given I chose to go the path of rake g migration...

rake db:create
rake db:migrate

### Question 5

I want to look at the actual database that has been created. What command should I type in the terminal?
rails db


### Question 6

I want to see a list of all the URLs available in my app, along with the HTTP requests and controllers associated with them. What command should I type in the terminal?
rake routes

### Question 7

I have worked on my app and finally want to see it in action. What command should I type in the terminal, and where should I navigate to in my browser?
rails s
http://localhost:3000


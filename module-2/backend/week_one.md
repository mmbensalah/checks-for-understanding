## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
  1. GET  - renders/displays page
  2. POST - redirects - sends new data to page
  3. PUT  - redirects - changes all specified data
  4. PATCH  - redirects - changes only some parts of specified data
  5. DELETE - redirects - deletes data
  
GET = Retrieve a resource
POST = Create new resource
PATCH = Update a part of a resource
PUT = Update all of a resource
DELETE = Destroy a resource

2. What is Sinatra?
  Sinatra is a framework that allows you to use Ruby to create an application that can be used on the internet.

A lightweight Rack-based, Ruby framework that allows to easily interact with the web. It has a Domain Specific Language that facilitates this interaction.

3. What is MVC?
  A pattern that is used when creating web applications, splits up program responsibilities b/w 3 components.
  1. Model   - holds classes and methods related to classes
  2. View    - dictates HTML layout
  3. Controller - main task designator that contains all http methods
 
 

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  Following convention allows for readability and ease when another person needs to make changes.
  
Model = Interacts with the database
View = What we display on the browser
Controller = The middleman between what is displayed (views) and gathering the information from the database (models)

5. What types of variables are accessible in our view templates without explicitly passing them?
  instance variables as stipulated in controller
  
 Because REST is implemented across the web and provides a consistent and easy-to-follow interface for the client.

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    <------------------ @count = 1
    erb :index
  end
  ```
Instance Variables

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
  @name = 'Mr. Ed'
  
  get '/horses' do 
    @count = 1
   erb :index
  end
  
  locals: { name = "Mr. Ed" }
8. What's the purpose of ERB?
  Allows app to insert ruby code into HTML in order to insert content in a structured format on page

Embedded RuBy = allows us to use ruby and html in the same file.

9. Why do I need a development AND test database?
  The programmer does not want to use all the db data to run tests. The programmer knows what the expected result is of a test    when they create and use their own data, while they would probably not know when using thousands of db entries. Also, it is    much faster to run a test with 2 data entries vs. hundreds or thousands etc.

To keep responsibilities clear. Having a shared database would make brittle code that is harder to test.

10. What is CRUD and why is it important?
  The four actions that applications should be able to do.
  1. Create
  2. Read
  3. Update
  4. Destroy

Create, Read, Update, Destroy = it is how we interact with a resource such as horses

11. What does HTTP stand for?
  Hypertext Transfer Protocol
  
12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  <%= this "prints" to page %> <% does not print to page %> 
  
13. What's an ORM? What does it do?
  Object Relational Mapper i.e. Active Record 
  It allows programmer to use programming language like Ruby to access a database, generates SQL for programmer.

Object Relational Mapper = a way for us to create objects from rows of a database table for easy interaction.

14. What's the most commonly used ORM in ruby (Sinatra & Rails)?
  Active Record 

15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  1. get '/merchants' - render merchants page
  2. get '/merchants/new' - render new merchant page
  3. post '/merchants' - create new merchant
  4. get '/merchant/:id' - render specific merchant page
  5. get '/merchant/:id/edit - render edit page for specific merchant 
  6. put '/merchant/:id' - update merchant info
  7. delete '/merchant/:id' - delete a merchant 
  
GET /restaurants = See all restaurants
GET /restaurants/:id = See restaurant with :id
GET /restaurants/new = See a form to create new restaurant
POST /restaurants = Create new restaurant
GET /restaurants/:id/edit = See a form to edit restaurant with :id
PUT /restaurants/:id = Update restaurant with :id
DELETE /restaurants/:id = Destroy restaurant with :id

16. What's a migration?
  Sending data into db.
  
  Instructions for how to modify the database.


17. When you create a migration, does it automatically modify your database?
  No, you still have to run rake db:migrate


18. How does a model relate to a database?
  DB queries are kept in models
  
  The model fetches information from the database.


19. What is the difference between `#new` and `#create`?
  #new makes a new item
  #create makes a new item and saves it to the db
  
  new creates a new instance but does not save unless .save is called. create both creates a new instance and saves it all at once

20. Given a table named `animals`, What is the SQL query that will return all info from that table?
  SELECT * from animals;
  
    `id     name        number_of_legs
    -----   ------      --------------
      1     panda       4
      2     giraffe     4
      3     whale       0
      4     bird        2
    

21. Using the same table, What is the SQL query that will return only the animals that has 4 legs?
  SELECT number_of_legs FROM animals WHERE number_of_legs = 4

### Review Questions:  
22. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
  CSV.foreach ('csvpath.csv', headers: true, header_converters: :symbol) do |item|
    id: row[id]
    title: row[:title]
    
 CSV.foreach("db/csv/films.csv", :headers => true, header_converters: :symbol) do |row|
film = Film.create(title: row[:title],
                description: row[:description])

23. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```
How would I add 'granola bar' to things you should have when hiking?
activities[:hiking][:supplies] = "granola"

activities[:hiking][:supplies] << 'granola bar'

24. What are the 4 Principles of OOP? Give a one sentence explanation of each.
  1. Encapsulation - keeping data isolated in classes
  2. Inheritance - parent/child classes
  3. Abstraction - hide complexity from user 
  4. Polymorphism - ability of an object to be more than one thing 
  
Encapsulation -- Only expose information and behavior that must be exposed to get your functionality
Abstraction -- Creating objects with simple logical interfaces that represent your item
Inheritance -- The ability to bring in methods from a single parent class
Polymorphism -- Methods of the same name on different objects, creating the ability to build dynamically


### Self Assessment:
Choose One: (erase the others)

* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:

* I feel somewhat comfortable, but also overwhelmed with the content presented this week



## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
It allows you to access database without using SQL, it translates ruby code in to SQL

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
The methods are saved in Active Record. You could enter in to Tux and call "Team.all" and get back all the entries in the Team table. Team.all.count would give you a total of entries in Team table.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
Team.find(4)

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
team = Team.find(4)
team.owner

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
Teachers - has_many :students
ID - Name

Students - belongs_to :teachers
ID - Name - TeacherID

6. Define foreign key, primary key, and schema.
Primary key - the ID of the table in question
Foreign key - the ID that relates to the above table
Schema - outline of what tables contain and how they relate to each other 

7. Describe the relationship between a foreign key on one table and a primary key on another table.
Teachers - has_many :students
ID - Name

Students - belongs_to :teachers
ID - Name - TeacherID

for this example, in the table Teachers, the ID is a primary key. In the table Students, the TeacherID is a foreign key that relates back to the ID from the Teachers table.

8. What are the parts of an HTTP response?
  1. Status Code
  2. Headers (Example – Content-Type: html)
  3. empty line
  4. option message


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
  1. .join
  2. .create
  3. .new / .save
  4. .order by
  5. .find(id)
  6. .find_by(name: "")
  
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
  1. rake db:test:prepare - uploads created test data for tests to run
  2. rake db:{drop,create,migrate,seed} - drops data already in db, uploads new data from seeds file
  
3. What two columns does `t.timestamps null: false` create in our database?
created_at and updated_at 

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
schools - has_many :teachers
teachers - belongs_to :schools 

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?

6. Give an example of when you might want to store information besides ids on a join table.
not sure

7. Describe and diagram the relationship between patients and doctors.
patients - has_many :doctors 
doctors - has_many :patients 

8. Describe and diagram the relationship between museums and original_paintings.
musuems - has_many :original_paintings
originalpaintings - belongs_to :museums

9. What could you see in your code that would make you think you might want to create a partial?
not sure

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
* I was able to answer most questions independently, but utilized outside resources for a few
* I was able to answer a few questions independently, but relied heavily on outside resources 

Choose One:
* I feel confident about the content presented this week
* I feel comfortable with the content presented this week
* I feel overwhelmed by the content presented this week
* I feel quite lost by the content presented this week

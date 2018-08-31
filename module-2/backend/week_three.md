## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?

 rails new greenhouse -T -d="postgresql" --skip-turbolinks --skip-spring
 
2. What do Models generally inherit from in rails?

the database(ActiveRecord)

3. What do Controllers generally inherit from in a rails project?

ApplicationController < ActionController::Base - contains all the rails routes methods

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

resources :horse
horse_path(horse)

5. What rake task is useful when looking at routes, and what information does it give you?

rails routes - gives a list of available routes and the html file they correspond to

6. What is an example of a route helper? When would you use them?

i.e. get 'post/:id' => 'posts#show'
use when the route you want does not fit the paths outline in rails routes

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?



8. What are strong params and why are they necessary?

restricts what attributes a user is able to input for more security

9. What role does `form_for` play in helping us create our forms?

it is a shortcut to making an html form

10. How does `form_for` know where to submit the user's input?

it submits user input from the text_field 

11. Create a form using a `form_for` helper to create a new `Horse`.

<%= form_for @horse do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>
 <%= f.submit %>

12. Why do we want to validate our models?

so that we make sure they are being created with the correct attributes

13. What are the steps of the DNS lookup?

1. computer sends request to DNS server
2. DNS server looks for website IP address
3. If it has it, it sends it back to computer
4. Computer uses IP address to access website


### Review Questions
14. Within a feature test and given the following HTML, write the code necessary to target the following section and check the person's name?

  `<section id="personal-info">
    <h3><%= @person.name%></h3>
   </section>
  
  within (#personal-info) do
    expect(page).to have_content(@person.name)
  end
  `
15. How would you call the method `prance` from within the method `move` on a `Horse` instance?

horse.move

16. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  

furniture[purchased]
furniture[table][height]

17. What is inheritance?

getting characteristics from another class 

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week


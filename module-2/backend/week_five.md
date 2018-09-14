### Week 5 Questions

Re-pull from this repository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
  put them in the controller

2. Where is cart information/temporary information usually stored?
  session

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
  1. a lot of extra data to store in the db when unless a cart is checked out, no need for that data
  2. if a visitor creates a cart and then creates a sign in, you would want that cart to persist

4. What is the purpose of the asset pipeline?
  a framework to compress CSS/JS/stylesheets to production

5. Why do we precompile our assets?
  to reduce space they take up

6. What do each of the following tags do?
  they allow program to access assets

```ruby 
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?

  1. how to install
  2. tools used
  3. version used
  4. purpose of tool/project
  5. how to use

8. What are the top four accessibility issues that we as developers should be aware of?
  not sure what this is referring to

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
  a callback
  allow you to sequence certain methods

10. Given the following object, how would we create a scope for all users who are active?

```ruby 
User.create(name: "Happy", active: true)

```
scope :true_user -> { where(:user => true)}

11. What is the difference between a scope and a class method?
a scope always returns an AR relation object
scope methods are accessible in controller?

### Review Questions:  
12. Given the following hash:  

```ruby
example = {cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?  
    example[:cart]['48'] = 4
    
  12b. How would you increase the quantity of item 29? 
    example[:cart]["29"] + 1
    
  12c. How would you find out how many items your user is thinking about purchasing?   
    example[:cart].values.sum
    
13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
    subclass can override method inherited from base class
    duck-typing - as long as object can use method, does not matter which object it is specifically
    
14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
  unsure

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week


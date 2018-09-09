## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
 data about a user saved in the user's browser
 
2. What’s the difference between a session and a cookie?
 a cookie is stored on the user's broswer and corresponds to a session on the website server

3. What’s a flash and when do you want to use flashes?
   a notification that is triggered when a user interacts with a page, you want to use flashes to let a user know when something they have done has triggered a change

4. Why do people say “HTTP is stateless”?
   HTTP does not store information about a user/user's activities

5. What’s authentication? Explain.
   Logging in
   
6. What’s the difference between authentication and authorization?
   Authentication deals with a user's ability to log in to a website, authorization deals with the permissions a user has once logged in
7. What’s a before filter?
   creates a hierarchy of methods to perform
   
8. How do we keep track of a user once they’ve logged in?
   session
   
9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
   namespace to change URI - requires nested folders for controller and view
   nest to keep URI the same
   
10. At a high level, what tools can you use to implement authorization? How would you use them?
    bcrypt? 
    
11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
    An enum sets a value equal to an integer, you need an array, declare in the model

12. What are some strategies you can use to keep your views DRY?
    partials

### Reviews Questions 
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
holidays = [
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  
14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300? 


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

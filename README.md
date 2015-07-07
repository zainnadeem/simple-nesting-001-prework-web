# Simple Nesting Lab

## Objectives

1. Practice access data from nested hashes
2. Practice adding data to/changing data within nested hashes

# Instructions

1. Fork and clone this lab, run the test suite to get started. 
2. You'll be filling out the content of a series of methods that we've defined for you. All of the methods expect you to operate on the `programmer_hash`, which we've defined and included in the body of each method. Use the test suite to guide you––each test is designed to tell you how to pass it. 

**Important:** You are expected to get these tests to pass by adding information to/changing information in your hash *programmatically*. In other words, if you're asked to, for example, change the value of a certain hash key *don't just re-write the hash with the new value!*. That is cheating. Use the methods we've learned and practiced in previous lessons

Changing a hash like this is good: 

```ruby
my_hash = {first: "i'm first!", second: "i'm second!"}
my_hash[:third] = "i'm third!"

puts my_hash
# => {first: "i'm first!", second: "i'm second!", third: "i'm third!"}
```

Changing a hash by simplye re-defining it is bad: 

```ruby
my_hash = {first: "i'm first!", second: "i'm second!"}
my_hash = {first: "i'm first!", second: "i'm second!", third: "i'm third!"}
```


**Reminder:** When defining methods, return values matter! Use Pry to drop into your methods and understand what is going on/what it is return and why if you are having trouble getting tests to pass. 
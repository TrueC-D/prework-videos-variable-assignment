# Variable Assignment

## Learning Goals
+ Describe how expressions are used in programming
+ Identify the return value of an assignment expression
+ Describe the Variable Lookup Expression
+ Describe the Assignment Expression
+ Identify the constant expression

## Lesson

+ Hi guys, this is Ian from Flatiron School. In this video, we're going to look at variable assignment in Ruby.
+ By the end of this video, you should be able to:
  + Describe how expressions are used in programming
  + Identify the return value of an assignment expression
  + Describe the Variable Lookup Expression
  + Describe the Assignment Expression
  + Identify the constant expression
+ So I'm in the Learn IDE Sandbox here, with a ruby file called `app.rb`. This gives me a place to play around with code and to test stuff out.
+ Remember that all code is just text in a file that can be interpreted by a computer.
+ In Ruby, when we execute a file, the ruby interpreter is running through the file from top to bottom and looking at expressions.
+ An expression is just some combination of data or operators that will eventually evaluate to some value
+ For example, if I write 1 + 1, Ruby will evaluate that expression to `2` - basic math is something that Ruby knows how to do
+ So expressions have `return values` - the return value is what the expression will end up as.
+ Now, if all of our programs used constant data like this, they wouldn't be very interesting.
+ Programming becomes really useful when you can do different things in different cases, or store different values
+ One way to do that is using a variable - a variable is something that holds a value that can change over the course of our program.
+ We can define a variable using a single `=` sign.
+ Here, I'll make a variable called `name` and assign it to my name, `name = "Ian"`
+ Anytime I access this variable from this point forward in my program, it will be set to the string "Ian"
```ruby
name = "Ian"
puts name # "Ian"
```
+ We can change the value again by using the `=` sign

```ruby
name = "Ian"
puts name # "Ian"
name = "Ian Candy"
puts name # "Ian Candy"
```
+ Makes sense, right? So variables are great for things where, maybe when we're programming, we don't quite know what the value is going to be yet.
+ One other note here: Ruby will throw an error if it gets a reference to a variable that hasn't been defined yet.
+ If I type `dog` into IRB - this will throw an error (undefined local variable or method dog for main object) - I haven't told Ruby what dog is, so it doesn't know what to do when it sees this.
+ Let's use what we know about variables to write a program that tells you how old someone is in dog years. One hint - we usually say that your age in dog years is about 7 times what it is in regular years. How might we do this?
+ So first, let's set a variable called age. `age = 42`
+ Now, we can make another variable called `age_in_dog_years` and set it equal to age * 7 `age_in_dog_years = age * 7`
+ Lastly, we can print out our age in dog years: `puts age_in_dog_years`
+ So this works great, and we can change the age to a different value and it also works well. Something we'll look at in a future video is - how do we actually get this age from someplace else? Like, how do we have a user type in their age? That would make this even more interesting.
+ One last thing to note - there's a special kind of variable in Ruby called a Constant. A constant works just like any other variable, except it's value should stay the same throughout the program. Once it gets set, it will give us a warning if it ever changes.
+ In Ruby, you'll typically see this to call attention to important stuff that doesn't really change. In the example here, we're doing something called a `magic number`
+ If you were reading this file but didn't watch this video, you might be confused as to why the number 7 is here. So this number is a good candidate for a constant variable. Let's create that variable now:
+ I can define a constant the same way I do a variable, only it must start with a capital letter. By convention, for constant values like this, I'll use all caps.
```ruby
DOG_YEARS_PER_YEAR = 7
```
+ Now, while running the program, if Ruby sees this constant change, it will give us a warning.
```ruby
DOG_YEARS_PER_YEAR = 7
DOG_YEARS_PER_YEAR = 4 # Gives us a warning
```
+ So, the programmer can change this before it runs, but the value can't change mid-course so to speak.
```ruby
DOG_YEARS_PER_YEAR = 7
age = 42
age_in_dog_years = age * DOG_YEARS_PER_YEAR
puts age_in_dog_years
```
+ So that makes things a bit more clear. Now, if the programmer needs to change that constant, they can do so. For example, some people say 4 dog years per year is actually more accurate. We can easily change that if we need to, and it works well.
+ That's it for this one - to recap:
+ We talked about how expressions are used in programming, such as math expressions and variable assignment
+ We looked at the return values of different expressions
+ We described the Variable Lookup Expression, and how ruby finds a variable value
+ We looked at how to use the variable assignment expression and how that works in our applications
+ And we also looked at how to use constants and why they are useful.
+ So thanks so much for watching - happy coding!

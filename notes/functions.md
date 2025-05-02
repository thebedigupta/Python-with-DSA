# Functions

1. __Defining Functions__

Until that point we are using built in functions. Now we are going to know how to create functions but before that there is one more important question to ask why we need to create functions.
Because until that point we are writing code in a single file but when our code is getting much longer which was not able to handle,readability & manage then we have to divide in small chunks which is easy to maintainable and reading.

So,Now let's see how to create function inside python 

```
def greet():
    print("Hi there")
    print("Welcome Aboard")


greet()  
```
__When you are naming any functions then you have to follow all naming conventions that you learned from naming variables__

2. __Arguments__

Argument is what you pass in the middile of the function example ```greet("Bedi","Gupta")```. Here, Bedi & Gupta is the argument for the greet function.

__Parameter__

```
greet(first_name,last_name):     // first_name & last_name is the parameter of the function of greet 
  print(f"Hello {first_name} {last_name}")
  print("Welcome Board")

greet('Bedi','Gupta') // Here, Bedi & Gupta is the arguments for the function 'greet()'
```
* Whenever you missed to pass any one argument it throws error.
* In the upcoming videos we are going to learn how to pass optional arguments.

3. __Types Of Functions__

In programming there are two functions 

A. Perform a task. (```greet()``` function is the example as shown above)

B. Calculate and Return a value. (round(1.9) is the mathematical operation which did some mathematical calculation and then return a value )

* In Python all functions return none unless you specifically mention to the function to return value.

![function return none](../assets/functions%20return%20none.png)

* When you don't want to return none

```
def greet(name):
return "...."

print(greet("Mosh"))
```
4. __Keyword Arguments__

__Example__  
```
def increment(number,by):

return number + by

print(increment(2,1))
```
![keyword Arugument](../assets/keyword%20arguments.png)

In the above picture passing arguments with defining what was it is called keyword Argument as shown above Image ```by = 1```.

5. __Default Argument__

![Default Arguments](../assets/default%20Arguments.png)

In the above image as you can see ```by = 1``` is a default parameter in the function.So whenever you don't want to second argument then it automatically fils 1 in that place and if you pass something then 1 is replace by your provided number in the above image case it is 5.

__Note : Optional Parameter always come after the required paraemeter. (required parameter = 2, optional parameter = 1)__

6. __*Args__

Let's understand this with example :

```
def multiply (x,y)
      return x * y

  multiply(2,3,4,5)
```
This above is not going to run because there are multiple numbers to pass through which causes the function can't understand what it means because there are two parameters.

__Important Terms__

* Square Brackets Contain Lists [2,3,4,5] 
* Paranthesis Contain Tuples (2,3,4,5) tuples are similar to list the only difference between them is notations they are collection of object. We will learn more about tuples in the upcoming lessons.

```
def multiply(*numbers):
print(numbers)

multiply(2,3,4,5) // Output (2,3,4,5 ) this we called as tuples but they are not like list they are iterable
```
As Shown Below
```
def multiply(*numbers):
    for number in numbers:
    print(number)

multiply(2,3,4,5) // Output we will get 2,3,4,5
```
Now, We will do what we wanted to do 

```
Qusetion : All I want to do is when we pass multiple no of arguments then multiplication was happen until the end of numbers that we are passing.

def multiply(*numbers):
    total = 1
    for number in numbers
      total *= number
    return total

print(multiply(2,3,4,5)) // Output 120
```

7. __**Args__

 Let's try to understand with example:

 ```
 def save_user(**user):
      print(user)   // Output {'id':1, 'name':'John', 'age' : 22}

      save_user( id = 1, name = John, age = 55)     
 ```
 __The Output will be converted into dictionary or you can say object which value you can read like this print(user['name'])__ 

 * Dictionary is like another data structure in python.

 All we want to tell is whenever there is double asterik ('**') inside a function then we can pass multiple keyword arguments or arguments and that value converted into object or dictionary.

8. __Scope__

In this topic we will talk about global and local variable global variable is what you aceess anywhere in the program but in local variable that variable only exist inside that function.

Note : Aviod invalid practices like changing global value inside the function like shown below.

![Invalid Way To Declare Global Variable](../assets/invalid%20practice%20for%20global%20variable.png)

9. __Debugging__

In this topic we are going to learn how to debug the code we are going to look how to debug with the help of debugger

Learn to use debugger in python that's how you understand things much faster and deeply.

Completed ✅
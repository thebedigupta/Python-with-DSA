# Quick Notes of Python

|S.No | Column 2    | Column 3 |
| --- | ----------- | -------- |
| 0   | [Flow Charts Notes](./notes/flow_charts_notes.md) | Done  |
| 1   | Basic setup | Skipped  |
| 2   | Control Flow | Done    |
| 3   | [Functions](./notes/functions.md)  | Done    |

0. [Flow Charts Notes](./notes/flow_charts_notes.md)

1. __Convention for giving variables a name__

* First Letter of any word must be smaller.
* Always give meaningful names.
* There is no space between two words
* Variable name never be start with any number.

### In-Built Functions

1. __len()__

__There is a in-built function which help in calculating the length of the string__ that is called ```len()``` function and here how you used it.

```
len(course) // here, Course is a argument for that function.
```
* How to get one word from from the string

```
course = 'Python Programming'
print(len(course))

print(course[0]) // Accessing first word of the string which is __P__
```
* There are few examples realted to the strings.

![Play with the strings](./assets/Play%20with%20Strings.png)

2. __Escape Sequence__

This is called escape Character ```\``` and you might be thinking how you can use it.

```
course = "Python \"Programming" // 
```
As you can see escape character help to escape from double quotes which is used in between double quotes ```Python 🫴\" Programming```

* ```\"``` It shows like this ```Python "Programming```
* ```\'``` It shows like this ```Python 'Programming```
* ```\\``` It shows like this ```Python \Programming```
* ```\n``` It shows like this ```Python (on a new line) -->   Programming```

3. __Formatted Strings__

Let's Understand this with Example

```
Example:

first = "Mosh"
last = "Hamedani"
full = first +""+last
print(full)
```
Let's write above code in more simple and consice way

```
first = 'mosh'
last = 'Hamedani'
full = f"{first} {last}"
print(full)
```

4. __String Methods__

If you wanted to know about methods below is the example :

```
course = "python programming"

As we know "course" is a variable

If you write " course. " inside your editor you will see multiple methods of strings.
```
* Below is the example of multiple string Methods

![String Methods Example](./assets/String%20Methods%20Example.png)

Let's talk little bit about above picture

In __First Case__ ```.upper``` means it convert every alphabet into upppercase.

In __Second Case__ ```.lower``` means it convert every alphabet into lowercase.

In __Third Case__  ```.title``` makes every starting alphabet into Uppercase.

In __Fourth Case__ ```.strip``` clear extra space from left and right of the string not in b/w.

In __Fifth Case__ ```.find``` it helps to find index of the "Pro" which is 9. If not find return -1 means Not Found.

In  __Sixth Case__ ```.replace``` it helps find that word and replace with whatever passed as a second argument.

In __Seventh Case__ ```in``` help find that word is in the course variable or not.

In __Eight Case__ ```not in``` it tells that swift keyword is not found inside course string.

5. __Numbers__

Number can be many types like integer,float and complex numbers. If you are learning python for web developement you never going to use complex numbers.

```
Example:

x = 1      // Integer
x = 1.1    // Floating nunber
x = i + bj // Complex Numbers
```
__Now let's see few expressions with different operators__

```
print(10 + 3)   // Addition
print(10 - 3)   // Subtraction
print(10 / 3)   // Divide (Given Quotient in the output)
print(10 // 3)  // Divide (Given Round off Quotient in the output)
print(10 * 3)   // Multiply 
print(10 ** 3)  // 3 is the power of 10 (exponent)

Another Important term

x = x + 3
x += 3 (Argumented Assignment Operator "+=")
Above both lines are same meaning and work.
```
6. __Working With Numbers__

In python for working with number there are few small modules that are exist but if we have to work wth complex mathmatical operations we have to import math module in our python file.

For Example: 

print(round(2.9)) // 3
print(abs(-2.9))  // Absolute 

For Example: 

print(math.ceil(2.2)) // Here, 2.2 simply means round to the nearest greater number or equal to it's nearest number 

```
If you wanted to know more about mathmatics module then simply search for "Python 3 Math Module"
```

7. __Type Conversion__

Type Conversion is a method in which we convert data type from one to another type.

__Let's Understand with Example__
```
x = input("x: ")
y = x + 1       // Error 
```
Because we are very well know that x that we get from the input of the user is in the form of string and string and number never be add. So for adding string and number we have to make sure every data is same type like for performing addiition we need two number not one string and one number as shown above.

```
Correct Algorithm

x = input("x: ")
y = int(x) + 1
print(f"x: {x},y: {y}")
```
__there are other methods also:__

* #int(x)   // For converting into Integer
* #float(x) // For Converting into float number
* #bool(x)  // For Converting into boolean
* #str(x)   // for converting into string

__(a) Truthy & Falsy__

In these we are going to consider those values as a falsy which belong from any in the below list:

* ""
* 0
* None 

In these case in context of boolean we consider them as falsy.

Example:

![falsy example](./assets/falsy%20example.png)

### Control Flow

1. __Comparsion Operator__

Here we will talk about different operators that we use very often like ```+,-,/,*``` for perform various opeartions.

For Example: 

![conditional Opearator Example](./assets/conditional%20Opearators%20example.png)

2. __Conditional Statements__

Understand with Example :

```
temperature = 35
if temperature > 30: // Whenever you use condtional statement you have to use colon at the end
 print("It's warm")
 print("Drink Water")

print("Done")

Example:

temperature = 35
if temperature > 30: // Whenever you use condtional statement you have to use colon at the end
 print("It's warm")
 print("Drink Water")

print("Done")
elif temperature > 20:  // This is how you used If else statement
 print("It's Nice")
else:
 print("It's Cold")
print("Done")
```

Here this above algorithm says if temperature is greater then 30 then print "It's warm & Drink Water" so there conditional statement apply if temperature is greater then that then print this.

3. __Tenary Operator__

Let's Understand with Example:

```
age = 22

if age >= 18:
  message = "Eligible"

else:
message = "Not Eligible"
  
print(message);
```
__Above code tells how this questions solve with if else condition,Now let's see how ternary Opearator Help:__

```
message = "Eligible" if age >= 18 else "Not Eligible"

print(message)
```

4. __Logical Operator__

Here are Logical Opearator's:

A. AND
B. OR
C. NOT


A. In __and__ Operator both conditional has to be true or else it given false :

```
high_income = True
good_credit = True

if high_income and good_credit:
print("Eligible")
else:
print("Not Eligible")

Note: If any of the conditions is not true then it return false
```
B. In __or__ Operator only one condition has to be true then code is print true

```
high_income = True
good_credit = True

if high_income or good_credit:
print("Eligible")
else:
print("Not Eligible")
```
C. In __not__ Operator it basically inverses the value of the boolean like shown below example:

```
student = false

if not student:         // Means here person is not the student
print("Eligible")
else
print("Not Eligible")
```
__Now look another example__

```
high_income = ture
good_credit = flase
student = false

if high_income or good_credit and not student:
print("Eligible")
else:
print("Not Eligible")
```

5. __Short-circuit Evaluation__

Let's understand this with example:

```
high_income = ture
good_credit = flase
student = false

if high_income or good_credit and not student:
print("Eligible")
else:
print("Not Eligible")
```
__Note :__ One thing you have to know that these boolean opearators is short-circuited. 

What actually happen is when first condition is true then python interpreator continue to check all the way of that expression to the last but when it found first statement false then it already interpret that statement consider as false and return false as a output that we called as __Short-Circuit__.

Example given below :

![logical Operator](./assets/Short%20Circuit%20Example%201.png)

But,When initial condition is false then that expression gives output will be ```false``` already.

Example below

![logical Operator](./assets/short%20circuit%20example%202.png)

__Note :__ We have same concept for AND or OR Opearator. See OR Operator Example Below 

![Logical Opearator Example 2](./assets/Short%20Circuit%20Example%203.png)

With OR Operator it only check first condition and if already false then it only check second Condtion not going to check third condition as show above.

__Note : In Python Logical Opearator is short circuited__

6. __Chaining Comparsion Opearator__

Let's Try to Understand with Example :

```
#age should be between 18 and 65

Without Chaining Method

age = 22
if age >= 18 and age < 65:
  print ("Eligible")

With Chaining Method

age = 22
if 18 <= age < 65:
print("Eligible")
```
7. __For Loops__

As you know for loops help repeat the task " N " times.

Example:

```
if number in range(3): // this statement help in printing "Attempt 3 times"
print("Attempt")

Note : Range is the built in function.
```
__You might be thinking what is the number here number automatically consider himself "0" and it start from zero and increases with attempt__ and as you would see 3 is not included here.

A. You can also pass two arguments.

![For loop example one](./assets/For%20loop%20example%201.png)

__In the above shown image first argument tells start from there and second arguments tell end before here__

B. You can also pass third arguments.

![For loop Example Two](./assets/For%20loop%20example%202.png)

Result of the above image

![Result of the third argument](./assets/For%20loop%20example%203.png)

__Inside python Range(start from, End Here, Step )__

8. __For ..Else__

Understand this with previous example

```
sucessful = false

for numbers in range(3):
    print("Attempt")
    if sucessful:
      print("Sucessful")
      break
else:
print("I tried 3 times but failed")
```
This above expression tells he is tried 3 time but failed when boolen value is false and that algorithm we called as for else algorithm.

9. __Nested Loops__

![Nested Loop Example](./assets/Nested%20loop%20example.png)

When x start executing then y holds until y complete its 3 iteration. That's why when x is 0 and reached to the y then y hold it and not go until y complete it's three iteration thus output shown like that in the left side.

10. __Iterables__

```
Whenever we have to check any data type in python that's how we can see

print(type(5))   // output  <class 'int'>
```
Now let's look the type of the range()

```
print(type(range(5)))  // Output <class 'range'>
```
range is also one of the complex types and what is interesting about range object is it's iterable.

```
#Iterable

for x in 'range(5)':
for x in  'Python':
print(x)   // Each time when iteration happen x is carry one word of string python.
```
![iterable example](./assets/iterable%20example.png)

Range Object are not the only to iterable in python strings are also iterable in each iterable each time it carries one string as shown above we have another complex type __called Lists__. Square brackets indicates the lists ```[]```.

![Lists example](./assets/Lists%20Example.png)

As you can see we can iterate over list and and in each iteration we get object in this list.

__Later In the Course we will learn how to create our own coustom objects and make it iterable__

![Coustom Objects](./assets/Coustom%20Objects.png)

In the above example you can see coustom Object(i.e shopping_cart) and each time when for loop run it iterate one item from the shopping_cart coustom object.

11. __While Loop__

While loop is more like a for loop it is not stop until a required condition true.

```
number = 100

while number > 0 :
   print(number)
   number //= 2 [number = number // 2 (half the number)]


// Output 100,50,25,12,6,3,1
```
Let me show you behind the scene use of while loop :

As you know when you are running in a python shell then there is a only oneway to exit from there and that is __Ctrl + D__  as shown below image here maybe while loop is running in the background to check if the user is pressed these buttons or not. If user pressed these buttons then user exit from python shell interpreter.

![While Loop Example](./assets/While%20loop%20exmaple%202.png)

Now, let's see the behind the scene thing

```
Here we have to write a program where user have to write quit for exit.

command = ""
while command.lower() != "quit":
  command = input('>')
  print('ECHO',command)
```
12. __Infinte Loop__

An Infinite loop is the loop that runs forever.

![Infinte Loop](./assets/Infinte%20loop.png)

Control flow complete ️✅

From Here if you wanted to read further then go and continue from Content of table while tapping to the link.
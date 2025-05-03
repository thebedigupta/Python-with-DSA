# Data Structures

In this section we are going to learn built in data Structures that are extremely important for python.

First we are going to look at lists, tuples and then Dictionary

## 1. Lists

Eariler we have see square brackets conatin objects that we called Lists. That Object Might be anything numbers, strings, boolen e.t.c or even a list of lists.

__Example__

![list example](../assets/lists%20example1.png)

In above example print(len(chars))  // Output will be 11
Because there are 11 alphabets in the string.

## 2. Accessing Items 

In this section we are going to learn different ways to accessing items in the list.

__Example__

```
letters = ["a',"b","c","d"]
print(letter[1])             // Output a
print(letter[-1])            // Output d
letters[0] = 'A'             // Output ["A","b","c","d"]
print(letters[ 0 : 3 ])      // Output ["A","b","c"]
print(letters[ : 3 ])        // Output ["A","b","c"]
print(letters[ 0 :  ])       // Output ["A","b","c","d"]
print(letters[ ::2 ])        // Output ["A","c"]   (b and d will be skipped)
```
__Example__

```
numbers = list(range(20))
print(numbers[::-1])   // Output Will be [19,18,17,16,15 ...until 0] (reverse Order)
```
## 3. List Unpacking

Let's Try to Understand :

```
numbers = [A,B,C,D,E]

first = (numbers[0])
second = (numbers[1])
third = (numbers[2])
four = (numbers[3])
five = (numbers[4])
```
Instead of storing each alphabet in seperate variable there is a method through which do it easily that we called as __list unpacking__.

```
first,second,third,fourth,five = numbers
```
After above step each numbers value stored in each variable with a name of first,second and so on this we called as list unpacking.

* Let suppose there are five values and you give only four variable then like shown below then it gives error

```
first,second,third,fourth = numbers // Output gives error
```
__Another Method of list Unpacking__

first, second, *others = numbers // Output will be first = A, Second = B , others = [C,D,E]

__What if we only want first and last item__

```
number = [1,2,3,4,4,4,4,4,9]

first, *others, last = numbers

print(first,last) // 1,9 

print(others)     // [2,3,4,4,4,4,4]
```
## 4. Looping Over Lists

Let's Understand this with example:

__A. Loop over Lists__

```
letters = [a,b,c,d,e]

for letter in letters:
    print(letter)  // Output a,b,c,d,e
```

__B. Now want Index Number & Letter.__

```
for letter in enumerate(letters):
    print(letter)           // Output (0,a) (1,b) (2,c) (3,d) (4,e) these we called as Tuples
```
__C. Now want iterate simply without forming tuples__

```
for index, letter in enumerate(letters):
    print(index,letter)     // Output 0,a  1,b 2,c 
```

* Tuples is read only we can't add items in it.
* tuples also follow list unpacking same as list does.

## 5. Adding or Removing Items

letters = ['a','b','c','d']

* ADD

```
letters.append('e') // Output Add 'e' at the end of the list
```
* INSERT

```
letters.insert(0,'-') // Output At first index '-' will be add in the list
```
* REMOVE

```
letters.pop(0) // Output last alphabet will be removed
```
* When you wanted to remove something but don't know the index.

```
letters.remove('b')
print(letters)  // Output serach that alphabet and remove it
```
__Let suppose you have multiple b in the list then you have remove each b individualy__

* DELETE

Delete One item

del letters[0]   // Remove Zero index alphabet.

del letters[0:3] // Remove a range of alphabets.

letters.clear()  // When you wanted to remove all objects in the list.

## 6 Finding Items

Let's understand with example:

This method show the index number of the alphabet if it was there or gives error.

```
letters = ['a','b','c','d']
print(letters.index('d'))  // Output this gives some kind of error means not exist
```
__For Removing Error__

This method is usually much better because here if statement check if it exist then print or else do nothing

```
letters = ['a','b','c','d']
if 'd' in letters:
    print(letters.index('d'))
```
## 7. Sorting Lists


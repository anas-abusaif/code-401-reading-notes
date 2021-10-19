# List Comprehensions in Python

## Create a List with range()

```
# construct a basic list using range() and list comprehensions
# syntax
# [ expression for item in list ]
digits = [x for x in range(10)]

print(digits)
```

output:

```

[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

## Create a List Using Loops and List Comprehension in Python

```
# create a list using a for loop
squares = []

for x in range(10):
    # raise x to the power of 2
    squares.append(x**2)

print(squares)
```

output:
```
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

The same thing can be done using a list comprehension, but with a fraction of the code. Let’s take a look at how to create a list of squares using the list comprehension method.

```
# create a list using list comprehension
squares = [x**2 for x in range(10)]

print(squares)
```

## Multiplying Parts of a List

```
# create a list with list comprehensions
multiples_of_three = [ x*3 for x in range(10) ]

print(multiples_of_three)
```

output:
```
[0, 3, 6, 9, 12, 15, 18, 21, 24, 27]
```

Adding a filter to the list comprehension allows for greater flexibility. By using filters, we can select certain items from the list, while excluding others. This is an advanced feature of lists in Python.
```
even_numbers = [ x for x in range(1,20) if x % 2 == 0]
```
output:
```
[2, 4, 6, 8, 10, 12, 14, 16, 18]
```

## Show the first letter of each word using Python

```
# a list of the names of popular authors
authors = ["Ernest Hemingway","Langston Hughes","Frank Herbert","Toni Morrison",
    "Emily Dickson","Stephen King"]

# create an acronym from the first letter of the author's names
letters = [ name[0] for name in authors ]
print(letters)
```

output:

```
['E', 'L', 'F', 'T', 'E', 'S']
```
 Separating the characters in a string.

```
# use list comprehension to print the letters in a string
letters = [ letter for letter in "20,000 Leagues Under The Sea"]

print(letters)

```
output:

```
['2', '0', ',', '0', '0', '0', ' ', 'L', 'e', 'a', 'g', 'u', 'e', 's', ' ', 'U', 'n', 'd', 'e', 'r', ' ', 'T', 'h', 'e', ' ', 'S', 'e', 'a']
```

## Lower/Upper case converter using Python

```
lower_case = [ letter.lower() for letter in ['A','B','C'] ]
upper_case = [ letter.upper() for letter in ['a','b','c'] ]

print(lower_case, upper_case)
```

output:

```
['a', 'b', 'c'] ['A', 'B', 'C']
```

## Print numbers only from a given string

```
# user data entered as name and phone number
user_data = "Elvis Presley 987-654-3210"
phone_number = [ x for x in user_data if x.isdigit()]

print(phone_number)
```

output:

```
['9', '8', '7', '6', '5', '4', '3', '2', '1', '0']
```


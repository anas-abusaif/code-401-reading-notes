# Modifying the Behavior of a Python Scope

## The global Statement

The statement consists of the global keyword followed by one or more names separated by commas. You can also use multiple global statements with a name (or a list of names). All the names that you list in a global statement will be mapped to the global or module scope in which you define them.

Here’s an example where you try to update a global variable from within a function:

``` python
counter = 0 
 def update_counter():
     global counter  
     counter = counter + 1  
```

## The nonlocal Statement

Similarly to global names, nonlocal names can be accessed from inner functions, but not assigned or updated. If you want to modify them, then you need to use a nonlocal statement. With a nonlocal statement, you can define a list of names that are going to be treated as nonlocal.

The nonlocal statement consists of the nonlocal keyword followed by one or more names separated by commas. These names will refer to the same names in the enclosing Python scope. The following example shows how you can use nonlocal to modify a variable defined in the enclosing or nonlocal scope:

```python
 def func():
     var = 100  # A nonlocal variable
     def nested():
         nonlocal var  # Declare var as nonlocal
         var += 100

     nested()
     print(var)
```


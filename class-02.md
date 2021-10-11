# In Tests We Trust - TDD with Python


thing to care about is the structure. A convention widely used is the AAA: Arrange, Act and Assert.
1. Arrange: you need to organize the data needed to execute that piece of code (input);
2. Act: here you will execute the code being tested (exercise the behaviour);
3. Assert: after executing the code, you will check if the result (output) is the same as you were expecting.

## The Cycle

The cycle is made by three steps:

🆘 Write a unit test and make it fail (it needs to fail because the feature isn’t there, right? If this test passes, call the Ghostbusters, really)

✅ Write the feature and make the test pass! (you can dance after that)

🔵 Refactor the code — the first version doesn’t need to be the beautiful one (don’t be shy)


# What does the if __name__ == “__main__”: do?

If the python interpreter is running that module (the source file) as the main program, it sets the special __name__ variable to have a value “__main__”. If this file is being imported from another module, __name__ will be set to the module’s name. Module’s name is available as value to __name__ global variable. 


```
print ("Always executed")
 
if __name__ == "__main__":
    print ("Executed when invoked directly")
else:
    print ("Executed when imported")
```

All of the code that is at indentation level 0 [Block 1] gets executed. Functions and classes that are defined are, well, defined, but none of their code runs.

Here, as we executed ```script.py``` directly __name__ variable will be __main__. So, code in this if block[Block 2] will only run if that module is the entry point to your program. 

Thus, you can test whether your script is being run directly or being imported by something else by testing __name__ variable.

If script is getting imported by some other module at that time __name__ will be module name.

 ## Advantages : 

1. Every Python module has it’s __name__ defined and if this is ‘__main__’, it implies that the module is being run standalone by the user and we can do corresponding appropriate actions.

2. If you import this script as a module in another script, the __name__ is set to the name of the script/module.

3. Python files can act as either reusable modules, or as standalone programs.

4. if __name__ == “main”: is used to execute some code only if the file was run directly, and not imported.

# Recursion

What is Recursion? 
The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function. Using recursive algorithm, certain problems can be solved quite easily.


## What coding languages should I learn?


Well honestly any, but I would highly recommend starting out with python and javascript as they are incredibly similar and will give a lot of room for webapp pentesting and making fun projects.

Let's start you off with the basics.

At the top of almost every python file (ending with a .py extension) you will find the import statements. These imports are either other files that contain code in the same folder you are working out of or will be packages you can install using ```pip install packagename```

Pip packages come from https://pypi.org/ and you can manually download them and add them to your code if you don't want to import them all the time. One of the most common problems you will encounter when running python code is 
```
Traceback (most recent call last):
  File "test.py", line 5, in <module>
    import test123
ModuleNotFoundError: No module named 'test123'      
```

This means that package doesn't exist or you don't have it installed. You can simply install it using the pip install command however sometimes it might be ```from test import test123``` in which case you would install test and not test123.

In that instance, test123 would be a function in python. That might look like this:
```
def test123():
	print("Hello World!")
```

By itself a function will never run until it is called upon, so if you had just that in a file nothing would happen. However if you do:

```
def test123():
	print("Hello World!")

test123()
```

That will now work as we are calling on the test function.

So what are the brackets for? Well those are for passing information into the function.

```
def test123(randominfo):
    print(randominfo)

test123(randominfo="Hello World!")
```

So in that example we are passing in "Hello World!" as a variable called "randominfo" and then printing it out.

That could also be written in a more complex way:
```
def test123(randominfo):
    print(f"Hello {randominfo}")

randominfo="World!"
test123(randominfo)
```

Not so bad right? We set the variable "random info" with the word "World!" and then we run t he function. This time however we use `fstrings` which is the f before the quotes in the print statement.

The def is still how we define the function and will still not run by itself until we call on it.

This is something to explore on your own testing out how things work but don't be scared! It truly is simple once you understand it, it's just hard to convey it in a way that everyone can understand straight away.
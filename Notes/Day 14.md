## Day 14

### Tesla Exercise

```python
def checkDriverAge(age=0):

  if int(age) < 18:
    print("Sorry, you are too young to drive this car. Powering off")
  elif int(age) > 18:
    print("Powering On. Enjoy the ride!");
  elif int(age) == 18:
    print("Congratulations on your first year of driving. Enjoy the ride!")
checkDriverAge(25)

```

### Methods vs Functions

- Functions like
  - list()
  - print()
  - max()
  - These are all built in
- Methods look like dot notation, so you can attach it to a string or smoething like that
  - 'hellloooo'.capitalize()

### Docstrings

```python

def test(a):
    '''
    Info: this function tests and prints param a
    '''
    print(a)

test()s

```

- If you do test(), the function will have a popup in your IDE where it tells you what this function does. Kinda like a readme
- There's a help() function, if you plug in another function, you are able to tell it what it does.
- Dunder method print(test.\_\_doc\_\_) (double underscore) this will print out the information
- So docstring is great to add more details

### Clean Code

```python
def is_even(num):
    if num % 2 == 0
        return True
    elif num % 2 != 0:
        return False

```

- The code above is kinda messy, we have a way to clean up the code

```python
def is_even(num):
    return num % 2 == 0:
    return False

```

- In the above statement, you don't need elif since if is true, you don't need the second part
- And since return exits the function, you don't even need return
- You also don't need the if statement either, because you can just return it directly rather than defining an if statement
- You can always clean up code, but no perfect solution

### Args and Keyword Args

```python
def super_func(args):
    return sum(args)

super_func(1,2,3,4,5)

```

- Python uses \*args and \*\*kwars
- The above example, will error because super_func will only take 1 parameter which is a positional argument, so we're giving it 4 additional keywords
- by adding a star in \*args, it can accept as many arguments as you want

```python
def super_fun*args):
    print(*args)
    return sum(args)
super_func(1,2,3,4,5)

```

- The aboe will actually return a tuple
- You can actually name args to anything \*hallooo is possible but not recommended
- \*\*kwargs allows you to put in keywords

```python
def super_func(*args, **kwargs):
    total = 0
    for items in kwargs.values():
        total += items
    return sum(args) + sum()

print(super_func(1,2,3,4,5, num1=5, num2=10))

```

- star args grabs positional arguments and sums everything
- Keyword arguments and gets a dictionary as keyword args and use them however you want.
- We should also consider the ordering too, here are some rules
  - params, \*args, default parameters, \*\*kwargs
  - Basically how all of these are defined within te function parenthesis

```python

def super_func(name, *args, i='hi', **Kwargs)

```

Excercise

- highest_even, takes a list

```python
def highest_even(li):
  even_num = []
  for item in li:
    if item % 2 == 0:
      even_num.append(item)
  return max(even_num)


print(highest_even([10,2,3,4,8,11]))

```

### Scope

- What variables do I have access to
- When we do total = 100, this has global scope, meaning everyone can use this if you put it outside of a function

```python
def some_func():
    total = 100

```

- In the example above, the variable only has function scope, meaning it's not visible outside of the function itself

### Scope Rules

- Start with local scope
- If there's nothing in the local scope, is there a parent local scope
- Then after all this, you can look for global scope
- Last one is built-in python functions
  - Comes with pre-defined functions such as sum()

### Gobal Keywords

- parameters are considered local parameters

```python
a = 10
def confusion(b):
    print(b)
    return b
```

- what if you're trying to access the global variable inside of a function

```python
total = 0

def count():
    total += 1
    return total

```

- The above would error out because it's not able to reference the global variable.
- You can use a global keyword in python

```python
total = 0

def count():
    global total
    total += 1
    return total

```

- By using a global keyword, you can now use it.
- However, an opinion is that this can get confusing to use
- A better way of doing this is dependancy injection

```python

def count(total):
    total += 1
    return total

count(total)
#or if you need to run it multiple tmes

print(count(count(total)))

```

- In the above, you eliminat the dependancy, and focus on itself. Basically, give a count of a total of 0, and then you wrap it around again

### Non local keyword

- this is a new keyword in python3
- This is a way of defining the parent keyword without dipping into global keyword

```python
def outer():
    x = 'local'
    def inner():
        nonlocal x
        x = 'nonlocal'
        print('inner:', x)
    inner()
    print('outer:', x)
outer()

```

- In the above example, the inner function is reaching out to the x value in the outer function and changes it
- We need scope because of resources. For the most part, you want to make it efficient. It's less of a concern now because we have so much memory, but something good to think about
- We also need scope because when the function ends, it will destroy the entire function and go to the garbage collector in Python, this is actually good so you don't clog up the computer's memory

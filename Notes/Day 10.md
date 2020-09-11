## Day 10

---

### What we'll cover now

- Conditions
- Looping
- This is what makes machines really powerful

### Conditional Logic

```python

is_old = True
is_license = True

if is_old:
    print('you are old enough to drive!')
print('check check')
```

- If a condition evalutes to true or false, it will be evaluated
- You add a colon here, which splits the condition to the respones. It automatically sends the indentation, that is so important becuase it is considered part of the if block
- If the next line does not have the indentation, then the code block ends. in the above example, the check and check will also print separately even if the above print line is false

```python

is_old = True
is_license = True

if is_old:
    print('you are old enough to drive!')
else:
    print('check check')
```

- In the above example, you see that it will choose one or the other

```python

is_old = True
is_license = True

if is_old:
    print('you are old enough to drive!')
elif is_licensed:
    print('you can drive now!')
else:
    print('check check')
```

- In the above example, it will run the first condition first, and then runs the second one, and if both conditions aren't true, it will print out check check

```python

is_old = True
is_license = True

if is_old and is_licensed:
    print('you are old enough to drive, and you hav a license')

else:
    print('you are not of age!')
```

- The and value allows you to combine different conditions together
- one thing to note here, elif statement. You can have as many conditions as you want

### Indentation in Python

- Python is qunie in that indentation actually interprets indentation since that is how it defines it as a block
- Other languages in JS will have a a curly braces which means indentations are usually styles

### Truthy vs. Falsey

```python

is_old = 'hello'
is_license = 5

if is_old:
    print('you are old enough to drive!')
elif is_licensed:
    print('you can drive now!')
else:
    print('check check')
```

- In the above example, they'll evaluate to true, that is because Python will convert this to a Booleon for you, so it does this bool(is_old) which defaults to true and thus why it passes through
- This is a Truthy value
- A Falsey value is if the bool of empty string'' or 0 which evaluates to false, meaning that this is falsey. There are actually more falsey values, you can see those in this ![Stack Overflow thread](https://stackoverflow.com/questions/39983695/what-is-truthy-and-falsy-how-is-it-different-from-true-and-false)
- One way to use this is you can do if username and password: because of this is present, you can get a truthy value

### Ternary Operator

- These can be called conditional expressions

```python

condition_if_true if condition else condition_if_else

```

- It starts with the if value first, it will see if it's true or false, so if its true, it goes left, if false, it goes right

```python
is_friend = True
can_message = 'message allowed' if is_friend else 'not allowed to message'

print(can_message)

```

- The above evaluates as true, so you'll get the 'message allowed' message.

### Short Circuiting

```python

is_user = True
is_friend = True

if is_friend or is_user:
    print('best friends forever')

```

- So there's a difference between or and and value performative. OR is more performative because the python interpreter will first check the first condition and stop if it's met already.
- And means that python will check both conditions. HOWEVER, if it evaluates as false, python interpreter short circuit if it's false and not check the other condition

### Logical Operators

- AND is one example of a logical operator
- Some other ones
  - >
  - <
  - =

```python

print(4 > 5) becomes TRUE
print(4 == 5) becomes FALSE

```

- We used the == sign because keyword can't be an expression meaning that since a single equal will assign a variable. A double equal here would just compare two things

```python

print('a' > 'b')

```

- The above will evaluate to False, this is because Python will convert these into integers, specifically to the ASCII Table, so since a is 97 and b is 98. The above expression will evaluate to false

```python

print( 1 < 2 < 3 < 4 < 5) becomes TRUE
print( 1 > 2 < 3 < 4 < 5) becomes FALSE

```

- The last example above short circuits so it detects the FALSE and then stops the interpreter from going further
- Some other operators here:
  - <=
  - > =
  - != means not equal to
  - not keyword: not is the opposite. Not is also a function print (not(TRUE)) which will evaluate to false

## Day 13

### break, continue, pass

```python
for item in my_list:
    print(item)
    continue

i = 0
while i < len(my_list):
    print(my_list[i])
    i+= 1
    continue

```

- Continue will go back to the for loop or while loop, which will also end the cycle
- There is also pass, this doesn't really do anything, it just passes to the next line
  - it's a good way for a placeholder while coding

### First GUI

- Make a christmas tree
  Solution:

```python
picture = [
  [0,0,0,1,0,0,0],
  [0,0,1,1,1,0,0],
  [0,1,1,1,1,1,0],
  [1,1,1,1,1,1,1],
  [0,0,0,1,0,0,0],
  [0,0,0,1,0,0,0]
]


i=0
while i < len(picture):
  for inner in picture[i]:
    if inner == 0:
      print(" ", end="")
    else:
      print("*", end="")
  i += 1
  print("")


```

- Andrei's soluions is pretty much the same here. He used a for loop both iterations which is probably more performant but i don't think it's a big deal, great to practice with a while as well

### Developer Fundamentals (what is a good code)

- Clean code
  - We want to make sure we're following a style
  - bad code can be no spaces before and after = or that there's extra line breaks, or randome comments everywhere
- Readability
  - Comments can be put where it's not obvious where things are
- Predicatability
  - Sometimes people try to be really clever with their code or using obscure code
  - You want to have code that makes sense, that does one thing really well
- DRY

  - Do not repeat yourself
  - In the example above, if you need to copy your code, you're probably doing it wrong. You can probably just use a function or counter of sorts to use a while loop
  - Make code reusable

- Here's how you can clean the above example code:

```python

i=0
fill = '*'
empty = ' '
while i < len(picture):
  for inner in picture[i]:
    if inner:
      print(fill, end="")
    else:
      print(empty, end="")
  i += 1
  print("")

```

- The above example will allow for you to reuse the empty or fill in other functions, in addition, you can also just change the variables really quickly only in one location

### Excercise

- Check for duplicates in a list, print duplicates

```python
some_list = ['a','b','c','b','m','n','n']


duplicates = []

for value in some_list:
  if some_list.count(value) > 1:
    if value not in duplicates:
      duplicates.append(value)
print(duplicates)

```

### Functions

- We can create our own functions for python to use them

```python
def say_hello():
    print('helllloooooo')

say_hello()

```

- def lets python knows that we're about to define a function
- The function is defined, but now it's living somewhere in memory, but you haven't activated it
- Remember that you need to have the parenthesis in order for show tree to work

### Arguments and Parameters

- The power of functions is the ability to make it dynamic
- This is an example of the paremeter

```python
def say_hell(name, emoji):
    print(f'helllooooo {name} {emoji}')

```

- Example of arguments

```python
say_hello('Andrei', 'smile')

```

- Arguments are the actual values that you provide to the function. Or call
- Parameters are the variables to define the function
- Other keywords are invoking the function

#### Default Parameters and Keyword

- Positional Arguments
  - The above example are positional parameters or arguments, because the position matters, if name and emoji are swapped, they will switch too
- Keyword Arguments

```python
say_hello(emoji='smile', name='Bibi')

def say_hell(name, emoji):
    print(f'helllooooo {name} {emoji}')
```

    - The above example defines the variable
    - This maybe bad practice because it makes it unnecessarily complicated, you should just make it in order to keep it simple

- Default Parameters

```python
def say_hello(name='Darth Vader', emoji='vader'):
    print(f'hellllooooo {name}{emoji}')

```

    - If nothing is inserted above, they will use Darth Vader and the emoji

### Return

- Keyword in python we will see a lot

```python
def sum(num1, num2):
    num1 + num2

sum(4, 5)

```

- The above nothing will return, if you had a print(4,5) it will display 'none'
- return will essentially tell python to give you the value back
- Function should do one thing really well, and usually return something as well
- A function should also really be usable in terms of the naming too
- If you put a function inside of another function and only return the inner most function, you'll still get none

```python
def sum(num1, num2):
  def another_func(num1, num2):
    return num1 + num2

#This will return none since we're returning from the outer most function
```

- You also just can't return another_func, because it's just referencing something from memory
- You can define the numbers inside of the outer return to get it to work

```python
def sum(num1, num2):
  def another_func(num1, num2):
    return num1 + num2
  return another_func(num1, num2)

```

- Return keyword automatically exits the function and does not go to the next lines

## Day 11

---

### Loops

- Allows us to run lines of code over and over again

```python
for item in 'Zero to Mastery':
    print(item)
```

- The above example woudl print each item one at a time
- Kinda like conditional operators, the item above is just the variable
- The variable is created for each item after the in and then do something
- Something that is able to be looped over is called an iterable

```python

for item in [1,2,3,4,5]
    print(item)

```

- This will just print out each number once
- You can do this for sets and tuples as well
- You can also chain these together

```python
for item in (1,2,3,4,5):
    for x in ['a','b','c']:
        print(item, x)

```

- This will basically run through 1 a 1 b 1 c and then goes through to 2 a 2 b 2 c

### Iterable

- it's a list, dictionary, tuple, set , string, these can be iterated -> one by one to check each item in the collection
- There are a few special ones that are iterable.

```python
users = {
    'name': 'Golem',
    'age': 5006,
    'can_swim': False
}

for item in user:
    print(item)

```

- The above will print the keys out, and not the value. Yes there are 3 methods
- user.items() this will give you the key value pair in a tuple ('name, 'golem')
- user.values() this will give you the value pair Golem
- user.keys() this will give you the key pair, this is just more descriptive and tell people what we actually want to do

```python
for item in user.items():
    key, value = item;
    print(key, value)

#There's actually a shorthand way of doing this

for key, value in user.items():
    print(key, value)

```

- The above key and value are just variables, but it's just conveninence because you can basically destructure
- integers are not iterable

### Excercise Tricky Counter

- Build a simple counter, count the items in the list

```python
my_list = [1,2,3,4,5,6,7,8,9,10]

```

- Loop through and add the sum together

```python
answer = 0
for x in my_list:
    answer = x + answer
print(answer)


```

### Range

```python
print(range(100))

# you'll get a range(0,100) This is a special type of object, gives default to 100.

```

- You have the ability to iterate over the range

```python
for number in range(0,100):
    print(number)

#this will loop and print off numbers 0 to 99

```

- This is useful because you can loop through something a set number of times
- you can just use an underscore as the variable

```python
for _ in range (0,10):
    print(_)

```

- Use this only when you really don't need anything
- You can also step over, range(0,10,2) this would jump each number by 2. You can't do negative numbers here if the range is positive, so if you do negative range(10,0,-1) you need to make sure the first number is bigger than the second

- Here's a quick way we can create a list

```python
for _ in range(2):
    print(list(range(10)))

#This would give you two lists of [0,1,2,3,4,5,6,7,8,9]
```

### Enumerate

```python
for i, char in enumerate('Helllooo'):
    print(i, char)

# you'll get 0 H, 1 e, 2, l

```

- This essentially helps creates a index of each character or object in the iterable object

```python

for i,char in enumerate (list(range(100))):
    if char == 50:
        print(f'The index of 50 is: {i}')

```

### While Loops

```python

while condition:
    do something

```

- As long as a condition is true, continue to iterate over this loop
- Very high chance of having an infinite loop here
- There is also a break keyword, which will stop the program

```python
i = 0
while 0 < 50:
    print(i)
    break

```

- You can also have else blocks too

```python
i = 0
while i < 50:
    print(i)
    i+= 1
else:
    pring('done with all the work')

```

- So you can use an else to stop, but why would we use else here? else will only execute if there isn't a break. So if you put break before the else, the else print would not print

- When to use while or for loops, this will depend on your issue. but both can be used

```python
my_list = [1,2,3]
for item in my_list:
    print(item)

vs

i = 0
while i < len(my_list):
    print(my_list[i])
    i += 1

```

- General rule is if you know how many loops you want, to use a for loop. But if you don't really know how many times to loop, you should use a while loop
- A common use case here is this:

```python
while True:
    input('say something: ')
    break

```

- This will only ask for something once, and not give me a loop. So let's modify this a bit so we can't do a loop

```python
while True:
    response = input('say something: ')
    if (response == 'bye'):
        break

```

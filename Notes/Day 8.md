## Day 8

---

### Common List Patterns

- There are some common ways people use lists

```python

basket = ['a','x','b','c','d','e','d']
basket.sort()
basket.reverse()
print(basket[::-1]
print((basket))
```

- Essentially, the above creates a new list for basket. However, the notation inside does not, that's why when you just print backwards, it's still the reverse

- You can also use a range

```python
print(list(range(100)))
```

- This will create a list for of 100 numbers, it's a great way to generate a numbered list really quickly

- There is also .join()

```python

sentence = '!'
sentence.join(['hi, 'my', 'name', 'is', 'JOJO'])
new_sentence = sentence.join(['hi, 'my', 'name', 'is', 'JOJO'])

```

- This will create a new item from .join
- New Sentence will make hi!my!name!is!JOJO becuase it inserts this in betwee.
- There is a short hand way of writing this though

```python

new_sentence = ' '.join(['hi', 'my', 'name', 'is', 'JOJO'])

```

### List Unpacking

- You have the ability to assign a variable to each of these variables rapidly

```python
basket = [1,2,3]

a,b,c = [1,2,3]
```

- Also, where an array is longer than the length of the list, you can use a start and a variable name to take the remainder of the list

```python
a,b,c, *other, d = [1,2,3,4,5,6,7,8,9]

```

- The last d will take away the 9 so other will then be 4,5,6,7,8

### None

- None is just a way to represent nothing

### Dictionaries

- abbreviated by dict, it's a data type as well as data structure in Python
- It's a way for us to organize our data in a form that has different pros and cons

```python

dictionary = {
    'a': 1,
    'b': 2
}
```

- This has a key value pair, so a string is used to grab a particular value.
- So if you try print(dictionary['b']). This will give you 2 above.
- The difference is that dictionary is not in any order, lists are in order though, you can use notation to fetch results. Dictionaries are very different.
- Large dictionaries when returned might not be in the exact same order, so you only need to know the pair.
- These value pairs can be any data type like a string, or array

```python

my_list = [
    {
        'a': [1,2,3],
        'b': 'hello',
        'x': True
    },
    {
        'a':[4,5,6],
        'b': True
        'x': 'hello'
    }
]
```

- In the above example you can do print(my_list[0]['a']) to retrieve the value of [1,2,3].

### Developer Fundamentals

- When would we use a list vs a dictionary
- If you wanted a list of people in line at your job, you probably want a list
- However, for stuff that doesn't have to be in order, it's better to ust a dictionary.

### Dictionary Keys

- We know that the value pair can be any type of data key
- However, what about the key pair, what can those be?

```python

dictionary = {
    123: [1,2,3], works
    True: 'hello', works
    [100]: True does not work
}

```

- Dictionary keys have to have a special property, it has to be immutable, it can't change. Numbers, booleons can't change. A list can be changed, so that's why it doesn't work, because you can re-assign the inside to something else
- 99% of the time, it's usually a string with something descriptive

```python

dictionary = {
    '123': [1,2,3],
    '123': 'hello'
}

print(dictionary[123])

```

- The above will be 'hello' because each key has to be unique, so if it sees a duplciate, it will overwrite the previous value

- What if we want to see if a user has a property like age or something

```python

user = {
    'basket': [1,2,3],
    'greet': 'hello'
}

print(user['age'])
```

- This will error out which is not good, so we don't want to just leave this. So here's another method we can use .get

```python

print(user.get['age'])

```

- This will give a None value or it gives us the value itself.

- Here's another way we can create a dictionary

```python

user2 = dict(name='JohnJohn)

```

- There is one more way on how to look for an item in a dictionary

```python
print('basket' in user.key)
```

- This will evaluate to True or False. The key will simply check the key instead of the value as well
- You can do the opposite here and check the values as well, which you can do as well .value
- There is also a .clear method which will clear the dictionary for you.
- .copy will copy the a user (user is the name of dictionary), it has to be equal to a new variable too
- user.pop which removes a key and value from the dictionary. print(user.pop('age')) will remove the value and returns the value that got removed.
  user.popitem() it will randomly pops off a key and value, the last item here. However, because dictionary is unordered, it will do something random
- user.update() which will allow you to update a key value, so you can do the following:

```python

print(user.update({'age': 55}))

```

- Age will get updated, if the key doesn't exist, it will update a new key item and add it onto it. Think find or create 'put' call in api.

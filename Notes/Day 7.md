## Day 7

---

### Password Checker

Requirements - Ask for an input of some sort - Display the password and then the password length - Password should be hidden, you can do this with '_' _ 10 and this will print 10 stars

```python
username = input('What is your username?')
password = input('What is your password?')

passwordlength = len(password)
hiddenpassword = '*' * int(passwordlength)

print(f'{username}, password {hiddenpassword} is {passwordlength} letters long')

```

    - You can also put methods inside of the string, but you want to be clear with what you're doing.

### Lists

- Ordered Sequence of objects

```python

li = [1, 2, 3, 4, 5]
li2 = ['a', 'b', 'c', 'd']
li3 = [1, 2, 'a', True]

```

- These are extremely important, lists are a form of arrays in other languages.

#### List Slicing

- In strings, we could take a string and then slice it string[0:2:1]
- This is also available in lists as well

```python

amazon_cart = [
    'notebooks',
    'sugnasses',
    'toys',
    'grapes'
]

pring(amazon_cart[0:2])
```

- Above example will grab the different strings in the list just like we did with strings
- While strings are immutable, lists are

```python
amazon_cart[0] = 'laptop'
```

- This is allowed and will change the first list
- Remember that indexing in python is non-inclusive so [0:2] really only shows two values
- If you want to copy a list you can do this:

```python
new_cart = amazon_cart[:]
```

#### Matrix

- This is when you have a list inside of a list

```python

matrix = [
    [1,2,3],
    [4,5,6],
    [7,8,9]
]

```

- There is the main array, and the sub-arrays inside. You can have more than 2 dimensions, you can do it infinitely.
- These come up in machine learning and what not.
- To access a list, you'll do this

```python
print(matrix[0][1])
```

- This will give you the value of 2

#### List Methods

- len() method will still work with lists
- You can add to a list

```python

basket = [1,2,3,4,5]
new_list = basket.append(100)
print(basket)
print(new_list)

```

- In the above exmample, the new list is none. This is because append changes the list in place, so it changed the basket, but did not change new_list. Instead you need to write it like this

```python

basket.append(100)
new_list = basket
print(new_list)
```

- We can also use insert as a method

```python
basket.insert(4, 100)
```

- This will change the basket to [1,2,3,100,5]

- There is also extend, which will loop over another list

```python

new_list = basket.extend([100,101])

```

- What about removing

```python

basket.pop()

basket.pop(0)

```

    - This will pop off whatever is at the end of the list
    - You can chain these together as well
    - By adding the 0, you can pop off the index of 0 or the first value

- There is also remove

```python

basket.remove(4)

```

    - Remove, we give it the value, while pop removed the index

- There is also a clear method, which basically removes all of the list

#### More Method

Default Example
basket = [1,2,3,4,5]

#### index

```python

print(basket.index(2))

```

- What index is number 2, this will give you 1. This is because this is searching for the value rather then searching on the index number

###### keyword

- These are Python words that already mean something, they all will do somethin or have some level of interaction with the language. They're also reserved
- We can use 'in'

```python

print('1' in basket)

```

- This will give you true or false based off of the basket themselves.

###### count

```python
print(basket.count('d'))
```

- This will just count how many times d will appear in the list, so in thise case none since it's not in there

###### sort

```python
basket.sort()
print(basket)

```

- Sorts the list in place, It will rearrange the list based off of alphabetical or numerical value
- We also have a function callced sorted()

```python

print(sorted(basket))

```

- This allows you to sort the basket and produces a new array
- the original basket has not been modified, it has created a new one.

#### Reverse

```python

basket.reverse()
print(basket)

```

- It reverses the basket in place, it doesn't sort, but it just trades the places of all the index


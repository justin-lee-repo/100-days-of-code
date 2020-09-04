# Day 5

---

## Strings

- it's a piece of text, usually written with quotation marks
- For longer strings, you can do this
  - long_string = ''' You can then type in everythihng and then ''' again. Kinda like Markup
- Example of using strings
  ````python
      first_name = 'Justin'
      last_name = 'Lee'
      full_name = first_name + last_name
      print(full_name)```
  ````
- This should run as JustinLee

## String Concatenation

- print('hello' + ' Justin')
- Just combines the strings together
- Okay this was pretty simple

## Type Conversion

- print(type(str(100)))
  - This converts the 100 which is a number to a string

## Escape Sequences

- weather = 'It's sunny'
  - The problem is that the apostrophe stops the string
  - We could do weather = "It's sunny" which will fix it but then you can't do weather = "It's "kind of" sunny"
- Escape Sequences would solve this issue. It's a \

```python
weather = 'It\'s sunny'
weather = 'It\'s \"kind of\" sunny"
```

- We can also use '\t' which adds a tab afterwards

## Formatted Strings

```python

name = 'Johnny'
age = 55

print('hi' + name + '. You are' + str(age) + ' years old')
```

- The above string is a bit cumbersome. There's a better way of doing things.

```python
print(f'hi {name}. You are {age} years old')
```

- This is a new feature of Python 3, this is great! Kinda similar to JSX actually with their \${} symbol.

- In Python 2, you needed to use a . (dot) format

```python
print('hi {}. You are {} years old'.format('Johnny', '55'))

OR

print('hi {0}. You are {1} years old'.format(name, age))
```

- Remember that the .format must be on the string, not the .print method
- The .format can actually put in formulas into the dot format as well

```python
print('hi {new_name}. You are {age} years old'.format(new_name='sally', age=100))
```

## String Indexes

- stored in memory as an ordered sequence of characteres
- Each individual character is stored in order
- So in 'me me me' the first m is location 0, the first e is in location 1, etc.

```python
selfish = '01234567'
print(selfish[0:2])
```

- The above example will get you 01
  - This is because it stops at 2, and doesn't want 2, so it's non-inclusive counting
- There's also a stepover print(selfish[0:8:2]) which will step over by 2, or 0,2,4,6
- If you leave the index blank print(selfish[1:]) this will start at index 1 and go all the way to the end
  - Opposite is true if the colon is before the number it will start at beginning up to that index
  - ::1 will count everything
  - [-1] will start at the end of the string
- print(selfish[::-1]) This will reverse the order of the string

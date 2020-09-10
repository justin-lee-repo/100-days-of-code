## Day 6

---

### Immutability

- Once a value has been assigned, it can be re-assigned
- However, you can change the variable such as changing the numbers in a given index
  - So strings are immutable, you can't change the value inside of the string.
- You can change it like this though:

```Python
selfish = '01234567'
selfish = selfish + 8
selfish now equals '012345678'
```

### Built-in Functions + Methods

- Examples
  - len() this function counts the length of a string
- There are also certain methods that python can perform.
  - These are similar in JS where you can add a .method() at the end of the string.
  - .upper will make the entire string uppercase
  - .replace('be', 'me') will replace the values however, the String is not immutable so if that string is not re-assigned the changes will dissapear

### Booleans

- This is true or false
- 1 is true, 0 is false

### Excersise 1

Prompt: Given 'birth_year = input('what year were you born?')

How do you make this program output 'Your age is ???'

```Python
birth_year = input('what year were you born?')
age = int(birth_year) - 2020
print(f'Your age is {age}')
```

### Commenting

- Python uses the pound (#) sign. This is only a single line though
- Adding comments should give value to the code
- Add comments when something really important to understand or if something understand
- But before you comment, you should see if you can make the code easier to read
  More comments don't necessarily mean better code

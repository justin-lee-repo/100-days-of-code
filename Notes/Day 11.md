## Day 11

---

### Excercise Logical Operators

```python
is_magician = False
is_expert = True

```

- Check if both magician AND expert, and if true, print out 'you are a master magician'
- But also, check if the magician but not expert 'at least you're getting there'
- If not a magician, you need magic powers

```python

if is_magician and is_expert:
    print("You are a master magician")
elif is_magician and not is_expert:
    print('at least you\'re getting there')
else:
    print('you need magic powers')

```

### is vs. ==
- == checks for equality or equality of value
- When checking for quality keep in mind truthy and falsy
- The is keyword actually checks the location in memory to see if the value is the exact same.
    - One thing to note about is that lists are created separately, so is you compare [] is [], it will evaluate false 

### For Loops
- 
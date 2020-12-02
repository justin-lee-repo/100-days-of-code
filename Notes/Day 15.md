## Day 15

### What is Object Oriented Programming

- Everything in Python is an object, when we use the type function type(), you'll see that every thing has a class keyword in there.
- We can use different methods on objects
- Objects have methods and attributes that you can access using dot method
- Object oriented programming allows you to create your own objects
- We are able to create your own data types with our own attributes and methods
- OOP is a paradigm, it's a way to structure our code to easily maintain and extend what we write
- An example here is an Amazon Drone delivery service
  - 1 developer works on the flight model
  - 1 developer does the camera portion
  - another developer does the claw portion
  - And finally, one is signal/networking to see where the drone is
- We are breaking down functionality and combine them afterwards. Later on, we can use the same pieces of the code to build something else

### What does this look like in Python

```python
class BigObject:
    pass

```

- Naming case here is capitalized for every word, signifiying that it's a class, using camelcase
- If you do type(BigObject) it will come out as type because it's still a blueprint

```python
obj1 = BigObject()

```

- In the above, we have just created a new object
- Blueprint is called a class, and then it can be instantitated, or the act of creating new instances.
- Afterwards, the instances will each individual object
- The blueprint will be stored in memory, everytime an object is created, you don't have to rewrite the code, simply say that you can go in memory and run that code. Keeping it dry, one place where the code can be copied over

### Creating your own Objects

- In this example, we're creating a wizard character.
- How do we think about this in OOP
  - We'll need players

Let's create a player object

```python

class PlayerCharacter:
#You should try to make this singular and not plural
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def run(self):
        print('run')

player1 = PlayerCharacter('cindy', 44)
player2 = PlayerCharacter('Tom', 21)

print(player1)
print(player1.run())
print(player2)
```

- init method is a special method, the two underscores or dunder method. You usually see this at the top, it's a constuctor method. Automatically called when we instantiate
- Self keyword, this lets the class define itself, meaning that self is PlayerCharacter, meaning that it can refer to itself. This seems to be a way to call itself
- This is the way to write code only once
- The above run method returns nothing because it doesn't return anything, but it does print. You can add a return 'done' to correct that

### Attributes and Methods

- Attributes and Methods allows you to mimic real life
- OOP allows code for repeatable, organized, and memory efficient
- Thinking less procedural and more functionality

- In the editor, you will get dunder and magic methods included with every single object

```python

help()
#this function allows you to see what class Bluprints python data types have

```

```python
class PlayerCharacter:
    membership = True
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def run(self):
        print('run')

player1 = PlayerChracter('cindy', 44)

```

- Class Object Attributes are static and not dynamic, meaning it doesn't change from player to player, the membership in above example is this. Cindy will have player1.membership will be true.

- You can use if statements in classes as well

```python
class PlayerCharacter:
    membership = True
    def __init__(self, name, age):
        if (self.membership):
            self.name = name
            self.age = age

    def shout(self):
        print(f'my name is {self.name}')

player1 = PlayerChracter('cindy', 44)

print(player1.shout())

```

- The above will run because you put the self keyword in the shout function
- All methods receive the self
- If you were to change the shout function as PlayerCharacter.name it will error, because PlayerCharacter attribute is not defined in shout. So you have to use self

### **init**

- some more details about this constructor function
- You can add in safeguards to your instantiation here
- Let's say for example for example

```python
class PlayerCharacter:
    membership = True
    def __init__(self, name='anonymous', age=0):
        if (age > 18):
            self.name = name
            self.age = age

```

- So if the person did not register, it will just error or if their age is too young it will also error

### Classmethod vs staticmethod

- We'll use decorators which we'll learn later

```python
class PlayerCharacter:
    membership = True
    def __init__(self, name='anonymous', age=0):
        if (age > 18):
            self.name = name
            self.age = age

    def shout(self):
        print(f'my name is {self.name}')

    @classmethod
    def adding_things(cls, num1, num2):
        return num1 + num2



```

- We get an error above because of the cls, which is kinda like self but kinda different. I just added this
- The difference is that we can use this without instantiating the Class itself
- So you can do print(PlayerCharacter.adding_things(2,3)) will work

```python
    @classmethod
    def adding_things(cls, num1, num2):
        return cls('Teddy', num1 + num2)

```

- You can actually use the class method to instantiate a new object by using player3 = Playercharacter.adding_things

- There's Static method
  - It works exactly the same way, but you do not have access to cls

```python

@staticmethod
    def adding_things2(num1, num2):
        return num1 + num2

```

- This is exactly the same as classmethod but you don't have access to the method, so no cls
- You won't see too often, but you might encounter it

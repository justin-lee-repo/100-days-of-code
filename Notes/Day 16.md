## Day 16

### 4 pillars of OOP

#### Ecapsulation

    - Ecapsulation - Binding of data and functions, encapsulates into one big object, keeping everything in this box. Attributes and methods. Attributtes are the data, and the functions that can act on this name and age
        - Able to package everything up into a blueprint
        - We want to package this to give us extra power since without functions and just attributes, it's just kinda like a dictionary
        - Essentially, without OOP these two are the same

```python
class PlayerCharacter():
    def __init__(self, name, age):
        self.name = age
        self.age = age

player1 = PlayerCharacter('andrei', 100)

#same as the following here

player2 = {'name': 'andrei', 'age': 100}

```

        - So with the blueprint we can more easily replicate the object without having to rewrite the variable over and over again

#### Abstraction

- hiding of information, or abstracting information only giving users what is necessary
- Essentially, you don't want to be overloaded with information, you just kinda want the results to save time
- So with abstraction can you change the object itself. Yes, you can change values like this:

```python

class PlayerCharacter:
    def __init__(self, name, age):
        self._name = age
        self._age = age

    def run(self):
        print('run')

    def speak(self):
        print(f'my name is {self.name} and I am {self.age} years old')

player1 = PlayerCharacter('andrei', 100)
player1.name = '!!!'
player1.speak = 'BOOOOO'
#Don't to the thing above please

```

- So the above will get modified here causing issues since you can then modify methods that come along with the object blueprint
- I think that being able to change this will make it prone to mistake

#### Public and Private (abstraction cont)

- Only give access to users that they are concerned about. There are just some things that shouldn't be able to modify certain things such as age and name.
- There's no such thing as truly private variables.
- We can get around this though
  - you can use self.\_name or self.\_age , this is most likely going to be a private variable. This is just a convention, it doesn't actually do anything.
- Don't confuse this with dunder methods, we should NEVER write dunder methods, so please only use single underscore

#### Inheritance

- Allows new objects to take on properties of existing objects, basically inheriting classes

```python
class User():
    def sign_in(self):
        print('logged in')
#WHOA, shouldn't we have init here?? Well you don't need an init method if you don't need to assign attributes to the sign_in method

class Wizard(User):
    pass

class Archer():
    pass
```

- The above are users, they can have multiple forms. In the above example, there are (), these are optional if the classes do not inherit from a parent class, it can be defined with or without the ().
- You just need to pass the parent class through the child class

```python
wizard1 = Wizard()
print(wizard1.sign_in)

```

- The above example has inherited the function from User class
- This is powerful because you can extend your wizard

```python
class User():
    def sign_in(self):
        print('logged in')
#WHOA, shouldn't we have init here?? Well you don't need an init method if you don't need to assign attributes to the sign_in method

class Wizard(User):
    def __init__(self, name, power):
        self.name = name
        self.power = power

    def attack(self):
        print(f'attacking with power of {self.power}')

class Archer():
    def __init__(self, name, num_arrows):
        self.name = name
        self.num_arrows = num_arrows

     def attack(self):
        print(f'attacking with arrows: number of arrows left-{self.num_arrows}')

wizard1 = Wizard('Merlin', 50)
archer1 = Archer('Robin', 100)

wizard1.attack()


```

- We're keeping our code DRY, abstracting our code away and using inheritance
- These are often called sub-classes or user-derived class since it's not the parent one

#### Instance

- A tool to check if an instance is a instance of another class

```python
wizard1 = Wizard('Merlin', 60)

isinstance(instance, Class)

print(isinstance(sizard1, Wizard))

#This will be true

print(isinstance(wizard1, User))

#This will be true, because Wizard is a sub-class, so parent classes count

```

- Where do dunder methods come from? In Python, everything is an object, everything in Python inherits from the base code. So you can actually use the term 'object'

```python
print(isinstance(wizard1, object))

#This is true, because it inherits from wizard class

```

#### Polymorphism

- 'Many' 'Forms', methods belong to objects, we use self keyword to act on object that gets instantiated
- In Python, this refers to the way object classes can share the same method names but act different based on what object is called upon

```python
class User():
    def sign_in(self):
        print('logged in')

class Wizard(User):
    def __init__(self, name, power):
        self.name = name
        self.power = power

    def attack(self):
        print(f'attacking with power of {self.power}')

class Archer():
    def __init__(self, name, num_arrows):
        self.name = name
        self.num_arrows = num_arrows

     def attack(self):
        print(f'attacking with arrows: number of arrows left-{self.num_arrows}')

```

- In the above example, attack is shared, but its done something different based on the attribute
- You can actually add this into a for list

```python

for char in [wizard1, archer1]:
    char.attack()

```

- Both outputs are different, so this is powerful becuase it allows us to cater to our needs
- If you have a function in the parent object, the child object will cancel that out
- How can we run both teh attack method in User and Wizard method though?

```python
class User():
    def sign_in(self):
        print('logged in')

    def attack(self):
        print('do nothing')

class Wizard(User):
    def __init__(self, name, power):
    def attack(self)
        User.attack(self)
        print(f'attacking with power of {self.power}')

class Archer():
    def __init__(self, name, num_arrows):
        self.name = name
        self.num_arrows = num_arrows

     def attack(self):
        print(f'attacking with arrows: number of arrows left-{self.num_arrows}')

```

- The above example will print out both the do nothing and attacking power, not sure why yet, he didn't quite explain this

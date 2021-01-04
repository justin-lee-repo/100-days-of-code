## Day 17

### Super()
```python
class User(object):
    def __init__(self, email):
        self.email = email

    def sign_in(self):
        print('logged in')

class Wizard(User):
    def __init__(self, name, power)
        self.name = name
        self.power = power

    def attack(self)
        print(f'attacking with power of{self.power}')

wizard1 = Wizard('Merlin', 60)
print(wizard1.email)

```

- We'll get an error here becuase the email address is not an object of the Wizard. 
- But wait.... doesn't Wizard call User up and bring up the email? The issue is that Wizard already has an init function. If you try it with sign_in, it will work. 
- We don't want to repeat it in Wizard becuase every account will have email. So how do we call the email in the init of User class?

```python

class Wizard(User):
    def __init__(self, name, power)
        User.__init__(self,email)
        self.name = name
        self.power = power

wizard1 = Wizard('Merlin', 60, 'merlin@gmail.com')
print(wizard1.email)

```

By explicitly calling in the init method of the User class inside of the Wizard, you'll get the email address. 
- There is another way of doing this though, it's called super

```python
class Wizard(User):
    def __init__(self, name, power)
        super().__init__(email)
        self.name = name
        self.power = power

wizard1 = Wizard('Merlin', 60, 'merlin@gmail.com')
print(wizard1.email)

```
- Super is calling the class above Wizard. It allows us to refer to it without having to pass self

### Object Introspection
- The ability to determine the type of object at runtime. Runtime is when the code is running. This is its strengths because everything in Python is an object

```python
wizard1 = Wizard('Merlin', 60, 'merlin@gmail.com')
print(dir(wizard1))

```

- Dir() gives you all the functions that you have access to. If you have an Code Editor with a liast of available functions, it's using introspection.

### Dunder Methods
- dunder methods are inherited from our base object class
- len() for example, is created through dunder methods

```python
class Toy():
    def __init__(self,color,age):
        self.color = color
        self.age = age

action_figure = Toy('red', 0)

print(action_figure.__str__())

#This is exactly as doing print(str(action_figure))

```

- dunder are special methods that Python recognizes. Here are a few examples

```python
class Toy():
    def __init__(self,color,age):
        self.color = color
        self.age = age
        self.my_dict = {
            'name': 'Yoyo',
            'has_pets': False
        }

    def __str__(self):
        return f'{self.colo}'

    def __len__(self):
        return 5

    def __del__(self):
        print('deleted')

    def __call__(self):
        print('yess??')

    def __getitem__(self, i)
        return self.my_dict[i]

action_figure = Toy('red', 0)

print(action_figure.__str__())

```

- You can modify dunder methods, so it allows you to customize these given methods.
- In the len method, you can print(len(action_figure)). Which will then return 5. 
- you can then type in del action_figure and it will print out the string
- Call, you can use print(action_figure()). So basically, you can turn a variable into a function. Because action figure is not a function. 
- For get item, you can do print(action_figure['name']). If you print this, you will get yoyo. So allowing you to access this.

### Multiple Inheritance

```python

class User():
    def sign_in(self):
        print('logged in')

class Wizard(User):
    def __init__(self, name, power):
        self.name = name
        self.power = power

class Wizard(User):
    def __init__(self, name, power):
        self.name = name
        self.power = power

    def attack(self):
        print(f'attacking with power of {self.power}')

class Archer(User):
    def __init__(self, name, num_arrows):
        self.name = name
        self.num_arrows = num_arrows

     def attack(self):
        print(f'attacking with arrows: number of arrows left-{self.num_arrows}')

    def run(self):
        print('ran really fast')

class HybridBorg(Wizard, Archer)
    def __init__(self, name, power, arrows):
        Archer.__init__(self, name, arrows)
        Wizard.__init__(self, name, power)

hb1 = HybridBorg('borgie', 50)
print(hb1.run())
print(hb1.check_arrows())

#Check arrows will fail because wizard accepts power but not arrows


```

- HybridBorg above is a mixture of Wizard and Archer, you can add as many objects in there to inherit. 
- Multiple inheritance is complicated
- By adding in the init there that tells the arrows passed through is the number of arrows that is for the instantiated arrow parameter from the Archer class
- Multiple inheritance is very powerful, but also gains in complexity

### MRO - Method Resolution Order
```python

class A:
    num = 10

class B(A):
    pass

class C(A):
    num = 1

class D(B, C):
    pass

```

- In the above, you'll get 1. This is because D inherits from B and C. This is because the MRO goes from D C B A. 
- MRO just defines the order python is trying to solve. 
- You can actually run D.mro() which will give you the order that it's running. In the above, it takes the first num that it sees which is in C. 
- It also checks for the base object
- The order is because it looks at all possible trees in each parameter. This is because of the algorithm they use to do MRO which is called 'depth first search'

### Functional Programming
- Separation of concerns, OOP does this as well. It is to seperate our code into packages and organized in a way that makes sense. Each part concerns itself into one thing that it's good at. 
- Functional programming also separates methods and attributes. So basically we get data, and it gets interacted with. 
- Generally, functional code has simplicity where data and functions are concerned. Functions operate on well defined data structures, lists and dictionaries. Rather than belonging that data structure to an object
- Goal is same as OOP, making code clean, understandable, easy to extend, easy to maintain, memory efficient, and DRY. 

Pure Functions
    - Seperation between data of the program, and the behavior of the program

### Pure Function
- Essentially you build algorithms or functions, where if you input a set of numbers, it will always return the same output. It has two rules
    1. Every input must have the same output
    2. function should not produce any side effects
        - side effects is what a function does that affects the outside world. For example, using print, which affects the outside world. Or touching variables. 

```python

def multiply_by2(li):
    new_list = []
    for item in li:
        new_list.append(item*2)
    return new_list

print(multiple_by2([1,2,3]))
```
- Is the above a pure function?
    - If I put in the same input, will it give me the same ouput. **Yes**
    - Does it produce any side effect? **NO** because it doesn't touch anything in the outside world. 

- Pure Function is more of a guidline, because an app can't be 100% pure functions since we couldn't make an app without being able to affect outside programs. 
- The easy way is that we can almost be confident that our pure functions work, so just focus debugging on the outside world. 

Here's what we can do here:

```python

Wizard = {
    'name': 'Merlin',
    'power': 50
}

def multiply_by2(character):
    new_list = []
    for item in li:
        new_list.append(item*2)
    return new_list

print(multiple_by2([1,2,3]))

```

- This is how we incorporate data and the pure function here.

### Map()
- Allow us to simplify the code we wrote above multiple by 2
- Take some sort of action/function as first param, and the data that you want to take the action upn

```python

def multiply_by2(character):
    new_list = []
    for item in li:
        new_list.append(item*2)
    return new_list

map(multiply_by2, [1,2,3])

```

- Map automatically gives us object that it has created. to view it, you have to turn it into a list. Okay this video made this **SUPER** confusing....
- Essentially, map iterates on each of the items that its fed. So basically, in the function above, we don't need to initialize a list, because map allows us to run a loop on all the objects its fed. So the above function is **wrong**, it should look more like this

```python

def multiply_by2(item):
    return item*2

print(list(map(multiply_by2, [1,2,3])))

```

- Map will call the function for you, so you don't need the () in the first param. You just need to list the function being used. 

```python
my_list  = [1,2,3]
def multiply_by2(item):
    return item*2

print(list(map(multiply_by2, my_list)))
print(my_list)

#my_list does not change in the last print function. however, the map still works

```

- Map allows you to create a whole new list without changing it. There are no side effects in the function above. 


### filter()

### zip()

### reduce()


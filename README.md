# Welcome to my 100 days of code!

---

I'll be docuemnting my journey here of my path in learning Python and React. I've chosen to do two courses simultaneously mainly because I find that I lose focus when I'm doing a single thing consistently. I'm hoping by having two courses I can bounce around I can maintaim my focus.

Here are some of the resources that I'll be using: [Resources](#tools)

| Day 1                                                                                                     | Day 2                                       | Day 3                                       | Day 4               | Day 5             |
| --------------------------------------------------------------------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------- | ----------------- |
| [The Basics, Markdown, How does Python work as a high level language, interpreters vs. compilers](#day-1) | [Int, float, math operations basic](#day-2) | [Operator Precednece, bin, complex](#day-3) | [Variables](#day-4) | [Strings](#day-5) |

| Day 6                                       | Day 7                                             | Day 8                                                   | Day 9                                      | Day 10                            |
| ------------------------------------------- | ------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------ | --------------------------------- |
| [More Stirngs, Methods, Commenting](#day-6) | [Data Structure (Lists and List Methods)](#day-7) | [Data Structures (Dictionary and Dict methods)](#day-8) | [Data Structures(Tuples and Sets)](#day-9) | [Conditional Statements](#day-10) |

| Day 11                       | Day 12           | Day 13                                | Day 14                                 | Day 15                                                            |
| ---------------------------- | ---------------- | ------------------------------------- | -------------------------------------- | ----------------------------------------------------------------- |
| [Logical Operators](#day-11) | [Loops](#day-12) | [Functions, Break, Continue](#day-13) | [Methods vs. Functions, Args](#day-14) | [OOP: attributes vs. methods, init, class/staticmethods](#day-15) |

<!--| Day 11 | Day 12 | Day 13 | Day 14 | Day 15 |
| --- | --- | --- | --- | --- |
| --- | --- | --- | --- | --- |

| Day 16 | Day 17 | Day 18 | Day 19 | Day 20 |
| --- | --- | --- | --- | --- |
| --- | --- | --- | --- | --- |

-->

<!-- TEMPLATE -->

<!-- https://www.markdownguide.org/basic-syntax -->
<!--
## Day #:
---
### tl;dr
- Topic(s):
- Time:
### Today's Topic(s)
### Journal
-->

## Day # 15:

---

### tl;dr

- Topic(s):
  - Object Oriented Programming Intro
  - Attributes and Methods
  - \_\_init\_\_
  - classmethod vs static method
- Time: 70

### Today's Topic(s)

We went over a good overview of what Object Oriented Programming is. Essentially a paradigm where we create blueprints for object types that are reusable and can be instantiated for when we need it. Think reusable components in React.

This helped me understand methods a bit more since we're creating new object types and creating the methods to go along with it making this all the more powerful. Init was pretty basic kinda like the super() in React I think, but the naming convention makes a ton of sense since a lot of programs have a init file.

classmethods vs staticmethods was cool to learn, but haven't really seen a practical application for it at this point, but good to keep in the back of my head

### Journal

I think today took the longest to wrap my head around these concepts. On the surface, I understand what OOP is and it makes sense, but i had a hard time understanding this in JS too so something I definately need to practice and understand on when I should use this. Overall no roadblocks, but whenever the next activity comes in, I'll need to spend more time on the concepts.

## Day # 14:

---

### tl;dr

- Topic(s):
  - Methods vs Functions
  - Docstrings
  - Clean Code
  - Args and keyword args
  - Scope
- Time:

### Today's Topic(s)

Methods and Functions were always a point of confusion for me on this one. But essentially, functions is a algorithm that runs on the input and in most cases, they will create something new from the original

Methods are essentially attached to some data type and modifies the existing data type but does not create something new. I should find a YT video or article on this. i'll put it in the journal section. Docstrings and clean code writing portions were good to know, this is definately a way of thinking I should pick up since i'm just starting up. A key concept here is that return exits the statement once compelte, so great tool to use to keep code clean.

Args is pretty cool, i think this is essentialy the ... destructuring method in JS.

And finally scope was pretty clear, seems like a much more logical way of doing scope than var vs let in JS.

### Journal

I found this article: https://www.tutorialspoint.com/difference-between-method-and-function-in-python for functions vs. methods. Essentially functions are standalone in the fact that you can invoke these whenever for any set of data. However, methods are only available to classes they're built into. That's whay lists and floats have different set of methods. However, functions like len() are functions because you can use it for pretty much anything.

No roadblocks, but have to realize that now that I'm getting into more complicated topics, I do need to start slowing myself down a bit to make sure i'm understanding these core concepts.

## Day # 13:

---

### tl;dr

- Topic(s):
  - GUI activity
  - Break, Continue, Pass
  - Functions
  - Return
  - Default Parameters
- Time: 120

### Today's Topic(s)

Big day today in terms of topics covered, the GUI topic was cool in that I actually went in and did some digging on Google to find the answer, which is exactly how he proposed it.

The break continue pass was a bit confusing though, something I need to brush up on. But functions are pretty similar to how they are in JS though so I didn't have too many issues with that. I really did like the way they explained return where without the keyword the function just stops, return is a way for the function to give something back once it's complete. And you can use return to just end the function with a single line like return num1+ num 2. Default parameters i think are pretty similar to react too, so that wasn't too hard to understand.

### Journal

So I was a bit confused as to when I would use break, continue, pass. This link was really helpful: https://www.w3resource.com/python/python-break-continue.php.

So break is used to stop the loop when a condition is met. What's interesting is if you put break inside a for loop, it's inclusive meaning it'll run up to the condition. In a While loops, it's exclusive, meaning it'll run up to the condition is met but exclude that last one. The example in the link explains it a bit better.

As for continue, it's essentially a skip button, so if the conditions are met and you have a continue, it will go back to the top of the loop for the next iterable without any action on the iterable that met the condition

## Day # 12:

---

### tl;dr

- Topic(s):
  - Loops
  - While Loops
  - Range
- Time: 60

### Today's Topic(s)

This was fun today, we did all things loops today including basic for loops and while loops. These were pretty much the same as JS here. However, one concept I really liked was when we should determine the use of loops vs while loops. Essentially, if you know the length of the number of loops you want to make, you should use a for loop. But, if you don't know how many loos you want, use a while loop.

One cool thing is that you can 'destructure' loops (not sure if this is the correct Python terminology) but essentially you can do for key, value == TRUE: print(key, value). So you can loop through dictionaries too.

Underscores can be a replacement for variables if you don't really need that value anywhere else.

Ranges were cool as well, great way to quickly tell how many times to loop through. So ranges have parameters range(min, max, and how many numbers to jump)

### Journal

No roadblocks today, for and while loops are pretty cool in Python too. Learning about range also jogged a few ideas on what I could possibly use this for as well.

## Day # 11:

---

### tl;dr

- Topic(s):
  - Logical Operators
  - is vs. ==
  - For Loops
- Time: 20

### Today's Topic(s)

Short course today, but essential information, we went over more of the logical operators including 'and' and 'and not' values here. We also understood the difference between == and is. == is checking for equality of value, this could mean is 1 == TRUE would be correct because it's comparing values. is keyword is checking for location in memory, so it must reference the exact value you found previously.

One tricky sample here is with lists, since they're created separately, if you compare two blank lists [] is [], it will be false because it's not the same place in memory. As opposed to 1 is 1, which is true because they're in the same place

### Journal

No roadblocks, basic concepts tooday that were pretty to understand. I guess one question I have is that are all integers in the same place in memory, so it's never instantiated right?

## Day # 10:

---

### tl;dr

- Topic(s):
  - Conditional Statements
  - Turnary Operator
- Time: 60

### Today's Topic(s)

Did a lot of if/else statements or conditional statements today. Learned some more operators as well. I really like how this class is structured, when I learned JS, it was throwing all the operators at you at once, without much context on how to use it. By combining the operators as well as conditional statements together, I get more context as to how these are used.

### Journal

No roadblocks today, made a decent dent into this class. The next few sections should involved a lot more searching and researching so I think this will be good practice. Also tried to make the markdown tables above look prettier, but my formatter extension in VScode is making me put in all of the hyphens, so please excuse the disorganization in my raw code.

## Day #9:

---

### tl;dr

- Topic(s):
  - Tuples
  - Sets
- Time: 30

### Today's Topic(s)

Tuples and Sets were pretty easy to follow here, I think these are more advanced functionaly compared to JS. Tuples are interesting in that these seem like really fixed. Definately would love to see how we use it in our code base.

### Journal

No roadblocks, getting a lot more familiar with methods vs function. This also completed the first portion of the Python basics course now since we've finished all the data types and structures. Moving onto functions next. WOO!!

## Day #8:

---

### tl;dr

- Topic(s):
  - Dictionary
  - Dictionary Methods
- Time: 30

### Today's Topic(s)

Went over dictionaries today, I'm guessing i'll be using these the most though since these are what a lot of JSON objects will come in. But this was pretty fun to learn in general and there are a lot of great features compared to JS.

### Journal

No roadblocks here today, getting a bit more familar with functions vs methods. Plus, we're also going to be learning functions a lot more next. I guess one questions is why do you make something like len() a function vs method. I guess it's because you're creating a new variable to get the length and not modifying the existing variable.

## Day # 7:

---

### tl;dr

- Topic(s):
  - Lists
  - List Methods
  - Password Challenge
- Time: 60

### Today's Topic(s)

We went over mainly lists and list methods today. Pretty simple. they're ordered, they're in the same memory space. Also did a password checker today, that was pretty easy to do and did a great job with variables too!

### Journal

Going to use this space for roadblocks too. Main roadblocks is that I always get confused with functions vs methods. For example, there is a len function here where you can do len(my_list) which gives you a length. However, there are other methods like .pop and stuff, and someties I get confused. I think just something I need to keep an eye on.

## Day #6:

---

### tl;dr

- Topic(s):
  - Immutability
  - Commenting
  - Methods and functions
  - Booleons
- Time: 40

### Today's Topic(s)

Another great day of topics, again great to see similarities between Python and Javascript. The commenting video on when to make comments was also interesting as it's not a good practice to just write too many comments.

Booleons and Methods/Functions were pretty easy to understand

### Journal

Nothing new for today, just glad to be able to hit a milestone today which is 2/3 done with this chapter. A few more videos until I've learned all the basics!

## Day #5:

---

### tl;dr

- Topic(s):
  - Strings
  - Escape sequences
  - String Index
- Time: 60 min

### Today's Topic(s)

Made some great progress today and while familiar withe these concepts, there are definately awesome features Python has in handling these. Specifically, string concatenation is pretty easy to do and reminds me a lot of JSX in React.

String index going into negative is awesome, nifty little trick that you can use to reverse a string which I've found is a popular test they like to do in interviews. Though I assume they'd probably ask you multiple ways to reverse strings and not just the copy out method that Pythong provides haha.

### Journal

I realized I need to cut these a bit shorter, as excited as I am to write about what I learn, it's not sustainable to spend 20 minutes on writing these summaries everyday when I could be working on more code.

## Day #4:

---

### tl;dr

- Topic(s):
  - Variables
  - Rapidly assigning variables
- Time: 20 min

### Today's Topic(s)

Pretty basic knowledge of variables, knowing this from JS this wasn't too new. Really like how you can rapidly assign variables in Python, 1,b,c = 1,2,3. I don't believe this is a feature in JS. Also great to see Dunders here, i saw this a lot in the code base at another company so never knew what this was

### Journal

- Short day today, great snippets of information here

## Day #3:

---

### tl;dr

- Topic(s):
  - Data Types
    - Bin
    - Complex
    - Variables
- Time: 25

### Today's Topic(s)

Pretty simple today, just bin and complex, they were pretty easy to understand and follow. I think Bin can be a useful feature, already thinking about how in the broader context, how these number data types can help with converting different values to one another when connecting APIs and what not.

Complex was also cool to learn as we can see why Python is loved by the Math community. Excited to see in future topics how we can use Python in Math and Science applications

### Journal

Don't really have any updates. This was a short sprint today, going to focus more on variables in the next days.

## Day #2:

---

### tl;dr

- Topic(s):
  - Data Types
    - Integers
    - Floats
  - Mathmatical Operations
    - \*\* = power of
    - // = nearest integer
    - % = remainder
- Time: 45 minutes

### Today's Topic(s)

Going through the basics has really reinforced concepts when learning JS. I'm starting to grasp the foundational elements of code. This section has been laregely review, but there were some data types that I wasn't too familiar with such as dict or tuble. Really eager to see what the differences are between them.

I hope declaring variables within scope won't be as tough as in JS haha.

Math basics were pretty easy to understand honestly, but some of the mathmatical operations were pretty cool to see in action.

### Journal

Feeling pretty good so far. Nothing has been too tough for me so far. Eager to dive right in to learn more about functions already but I awknowledge there are enough differences between JS and Python syntax that I feel like I really need to make sure I don't overlook these things.

Also, given how busy life is these days, I don't think this will be 100 consecutive days of code. Really, this will be 100 days of non-consecutive code.

## Day #1:

---

### tl;dr

- Topic(s):
  - Markdown
  - Interpreter vs. Compiler
  - Repl.it
  - Python 2 vs 3
- Time: 90 minutes

### Today's Topic(s)

Big thing today was learning the Markdown syntax so I can start writing these updates. I haven't really used Markdown extensively before so having this pretty easy to use language is a great way to take notes and make it look great. The other side benefit here is that I can practice reading documentation. These always seems so daunting, I've tried reading CSS library documentation and it was a tough one.

Other than that, we really just covered the basics today in terms of what Python is and at a high level (no pun intended) how Python gets interpreted into machine code and the differences between interpreters and compilers.

Got an introduction to repl.it which just looks like a playground for people to quickly test out their code. And finally, Python 3 that came out in 2008 is still 'newish' and that some code bases are still written in Python 2.

### Journal

I'm going to use this section to documenthow I feel and improvements that I want ot make to this repo. The majority of my inspiration came from my awesome co-worker Connor, so cheers to him and make sure to follow him on Twitter: [@connorrobots](https://twitter.com/connorrobots).

It seems daunting to have to recap everything everyday, but i know this is how I'll grow and I expect these recaps to be shorter in the future.... or maybe even longer who knows!

One thing that might help though is the possibility of using a text expander like Typinator or Alfred to very quickly dish out Markdown syntax like the one to write Python script. I'm going to work on that in Day 2.

### Links

- [Markdown Documentation](https://www.markdownguide.org/)

---

# Tools

### Classes

- [Python Course](https://www.udemy.com/course/complete-python-developer-zero-to-mastery/) Quick tip, if you haven't been on Udemy before, all of their classes are routinely on sale for \$10, I wouldn't recommend buying full price!

- [React Course](https://www.udemy.com/course/complete-react-developer-zero-to-mastery/) Same thing, also always on sale for about \$10

### Applications

- [Visual Studio Code](https://code.visualstudio.com/) as my text editor, I'll post my extensions list at a later point

- [Zappy by Zapier](https://zapier.com/zappy) Screenshot capture for MacOS only.

- [iTerm2](https://www.iterm2.com/) Tbh, I haven't really explored the full functionality of this yet the tabs are cool, but I don't feel advanced enough yet to understand why this is better than the normal MacOS native terminal.

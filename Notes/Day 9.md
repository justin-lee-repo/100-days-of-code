## Day 9

---

### Tuples

```python

my_tuple = (1,2,3,4,5)
my_tuple[1] = 'z'

```

- The above will error out because tuple are immutable, you can still access it through an index though
- You can even use lookup indices print(5 in my_tuple) would equal true
- There are benefits since you can tell other programmers that you don't want to change that list
- Making this less flexible, but more performant than lists
- E.g. Working for Uber, pickup location for example, you can get rid of it and replace it at anytime, you just can't modify it.

```python
my_tuple = (1,2,3,4,5)
new_tuple = my_tuple[1:2]

print(new_tuple)
```

- You'll get 2, here. So essentially you will always get that comma

### Tupple Methods

- .count this will count the number values in the tuple based off of your search parameter. So in the above example, myprint(my_tuple.count(5)) you'll get 1
- .index this will get you the location of the index. So it's also 0 based counting so if you get index of 5, it will return 4
- you can also you use len here

### Sets

- Unordered collection of unique objects

```python

my_set = {1,2,3,4,5,5}
print(my_set)

```

- The above example would only return one 5. So each data must be unique.
- If you try to use a .add method, it will also need to have unique data. So NO REPEATS

```python
my_list = [1,2,3,4,5,5]
```

- Given the abovee list, how do you go about converting this into a set.

```python
my_set.add(
    my_list[0::1]
)

oops

print(set(my_list))
```

- Okay, so you just have to wrap it around the set. Email addresses or usernames that have to be unique address, this is one way we can use this.
- if you try to do print(my_set[0]). This will not work, because it's an unordered list, therefore you would search for a particular value rather then a static position.
- You can do print(1 in my_set) and you can do print(len(my_set)).

### Sets Method

```python
my_set = {1,2,3,4,5}
your_set = {4,5,6,7,8,9,10}

```

- .difference
  - print(my_set.difference(your_set)) This will give you the difference between the second set. so this will output 1,2,3
- .discard
  - This wiill discard a certain number from the set. It modifies the set
- .difference_update
  - my_set.difference_update(your_set). This will remove all elements from other set to your set. Please note you have to re-print it. This will output 1,2,3. This will change it compared to just difference.
- .intersection
  - my_set.intersection(your_set) This will give the intersection between the first and second set.
  - Shortcut for this is print(my_set & your_set)
- .isdijoint
  - my_set.isdisjoint(your_set) Are those two sets have nothing in common, so this will be false, since there are stuff in common
- .issubset
  - my_set.issubset(your_set) If the first set is compeltely inside of the circle of the second set. This will be false
- .issuperset
  - my_set.issuperset(your_set) This is the other way around, does my first set encompass the second set. This will also be false.
- .union
  - my_set.union(your_set) which just unites the two sets together. Please remember that a set can't have duplicates.
  - You can also do print(my_set | your_set) this pipe line will work

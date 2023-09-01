## Zip() Function
Zip Function has following attributes:
* Used to combine multiple **Iterable Objects** into a Single Iterable Object
* The Index of Element of One Iterable Object is matched with the First Index of Second Iterable Object and so on. 
* It takes **TWO OR MORE** inputs 
* Output result is either a List or any other Sequence Data Type as we desire. 
* If input iterable is of different length, `zip()` stops creating pairs when shortest iterable is exhausted. 
However it is necessary to note that, If we dont explicitly convert the result of `zip()` in to `list()` or `dict()`, we still have a valid iterator we can use in `for` loop or other constructs. But in that case, we wont be able to access specific elements like we can use with `list()` or `dict()`. 

## Unzip()
* Now there is no function in python specific to "unzip()"
* However, **zipped** values can be easily ***unpacked*** by adding a `*` before the object.
* Unpacking is done when we want to retrieve individual values that were previously combined using `zip()`
* Unzipping separates values from an iterable such as tuple, lists, dictionaries etc.
```
zippedData = [("A",1),("B",47),("C",7)] # List of Tuples
numbers, letters = zip(*zippedData)
print(numbers)
print(letters)
```
* You can also unpack values from list or tuples individually. Each variable on the left side of the assignment receives a value from the `data` list based on its position.
```
data = ["Talaal", 27, "Karachi"]
Name, Age, City = data
print(Name)
print(Age)
print(City)
```
* Unpack is often used with `for` loops to iterate over iterable elements
```
pairs = [(1, 'apple'), (2, 'banana'), (3, 'cherry')]

for number, fruit in pairs:
    print(f'Number: {number}, Fruit: {fruit}')
```
Unzipping or unpacking is a useful technique when working with complex data structures, iterating over data, or processing results from functions that return multiple values. It allows you to work with individual elements easily and efficiently.

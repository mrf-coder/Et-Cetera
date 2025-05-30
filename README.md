# Et-Cetera
```js
students = [
    {"name": "Ron", "house": "house1"},
    {"name": "Joe", "house": "house2"},
    {"name": "Jon", "house": "house3"},
    {"name": "Doe", "house": "house4"},
    {"name": "Arik", "house": "house5"},
]

names = set()
for student in students:
    names.add(student["name"])  

for name in sorted(names):
    print(name)

```
```js
  
students = [
    {"name": "Ron", "house": "house1"},
    {"name": "Joe", "house": "house2"},
    {"name": "Jon", "house": "house3"},
    {"name": "Doe", "house": "house4"},
    {"name": "Arik", "house": "house5"},
]

names = []
for student in students:
    names.append(student["name"])  # use .append() for lists

for name in sorted(names):
    print(name)

```
```js
balance = 0

def main():
    print("Balance:", balance)
    deposit(100)
    withdraw(50)
    print("Balance:", balance)
def deposit(n):
    global balance 
    balance+=n

def withdraw(m):
    global balance 
    balance-=m    
if __name__ == "__main__":
    main() 
```
```js
class Account:
    def __init__(self):
        self._balance = 0  # Use _balance directly to avoid property issues

    @property
    def balance(self):
        return self._balance

    def deposit(self, n):
        self._balance += n

    def withdraw(self, n):
        self._balance -= n    

def main():
    account = Account()
    print("Balance:", account.balance)
    account.deposit(100)
    account.withdraw(50)
    print("Balance:", account.balance)

if __name__ == "__main__":
    main()

```
```js
class Cat:
    MEOWS =3 
    def  meows(self):
       for _ in range(Cat.MEOWS):
           print("meows")
    


cat = Cat()
cat.meows()    
```
```js
class Cat:
    def meows(self, count=1):  
        for _ in range(count):
            print("meows")

cat = Cat()
cat.meows(7)  

```
##### pip install mypy


```js
def meows(n:int):  
        for _ in range(n):
            print("meows")

number:int = int(input("Number: "))
meows(number)    # :int optinal check mypy tool 
```
```js
def meows(n:int )->str:  
       
            return "meows\n"*n

number:int = int(input("Number: "))
meows:str=meows(number)
print(meows,end="")
14:22
```
#### docstring
```js
def meows(n:int )->str:  
       
            return "meows\n"*n


"""
Meow n time
:param n : Number of time to meow
:type n :int
:raise TypeError :If n is not int
:return :A string of n meows , one per line
:rtype:str

"""            

number:int = int(input("Number: "))
meows:str=meows(number)
print(meows,end="")
```
####### "-n" comnd mak sport
```js
import sys 
if len(sys.argv)==1:
    print("meow")
elif len(sys.argv)==3  and sys.argv[1]=="-n":
    n=int(sys.argv[2])
    for _ in range(n):
        print("meow")
else:
    print("usage : meows.py")  

    """
    PS C:\Users\DELL\Desktop\hello> python hello.py -n 3
meow
meow
meow
PS C:\Users\DELL\Desktop\hello> 

    
    """  
```
```js
import argparse

parser = argparse.ArgumentParser()
parser.add_argument("-n")
args=parser.parse_args()
"""
PS C:\Users\DELL\Desktop\hello> python hello.py -n 3
meow
meow
meow
"""

for _ in range(int(args.n)):
    print("meow")

# Desktop\hello> python hello.py -h
```
```js
import argparse

parser = argparse.ArgumentParser(description="Meow like a cat")
parser.add_argument("-n",help="number of time to meow",defult=1,type=int)
args=parser.parse_args()


for _ in range(int(args.n)):
    print("meow")

# Desktop\hello> python hello.py -h
# Desktop\hello> python hello.py 
# Desktop\hello> python hello.py -n 3
```
##### unpacking
```js
first, *_ = input("What is your name? ").split(" ")
print(f"hello,{first}")
```
```js
name_parts = input("What is your name? ").split(" ")
first = name_parts[0]
print(f"hello, {first}")

```
```js
def total(galleon,sickles,knuts):
    return(galleon*17+sickles*29+knuts)
coins = [10,5,4]
print(total(*coins),"Knuts")
```
```js
// unpack set by dict operator
def total(galleon,sickles,knuts):
    return(galleon*17+sickles*29+knuts)
coins = {"galleon":10,"sickles":5,"knuts":4}
print(total(**coins),"Knuts")
```
##### *args, **kwargs
```js
def f(*args, **kwargs):
    print("Positional:  ",args)
f(100,577,3344,555,77,88)    

#  *args, **kwargs
```
```js
def f(*args, **kwargs):
    print("Positional:  ",kwargs)
f(Apple=200,Mango=300,Grapes=500)    

#  *args, **kwargs
```
```js
def main():
    yell(["This", "is", "CS50"])

def yell(words):
    uppercased = []
    for word in words:
        uppercased.append(word.upper())  #
    print(*uppercased)

if __name__ == "__main__":
    main()

```
```js
def main():
    yell("This", "is", "CS50")

def yell(*words):
    uppercased = []
    for word in words:
        uppercased.append(word.upper())  #
    print(*uppercased)

if __name__ == "__main__":
    main()

```
##### map(function,iterable,...)
```js
def main():
    yell("This", "is", "CS50")

def yell(*words):
    uppercased = map(str.upper,words)
   
    print(*uppercased)

if __name__ == "__main__":
    main()
#map(function,iterable,...)
```
##### #list comprehensions
```js
def main():
    yell("This", "is", "CS50")

def yell(*words):
    uppercased = [word.upper() for word in words]
   
    print(*uppercased)

if __name__ == "__main__":
    main()
#list comprehensions
```
```js
students = [
    {"name": "Ron", "house": "house1"},
    {"name": "Joe", "house": "house2"},
    {"name": "Jon", "house": "house3"},
    {"name": "Doe", "house": "house4"},
    {"name": "Arik", "house": "house5"},
]

# Corrected list comprehension
names = [student["name"] for student in students if student["name"] != "Doe"]

# Sorted print
for name in sorted(names):
    print(name)

```
```js
students = [
    {"name": "Ron", "house": "house2"},
    {"name": "Joe", "house": "house2"},
    {"name": "Jon", "house": "house2"},
    {"name": "Doe", "house": "house2"},
    {"name": "Arik", "house": "house5"},
]

def is_house2(s):
    return s["house"] == "house2"

house2 = filter(is_house2, students)

for houses in sorted(house2, key=lambda s: s["name"]):
    print(houses["name"])

```
#### # dictionary comprehentions
```js
students = ["Ron","Ali","Doe"]

addhouse={student:"house11"for student in students}
print(addhouse)    

# dictionary comprehentions
```

```js
students = ["Ron","Ali","Doe"]

addhouse=[{"name":student,"house":"house11"} for student in students]
print(addhouse)    

# dictionary comprehentions
```
```js
students = ["Ron","Ali","Doe"]

addhouse=[]
for student in students:
    addhouse.append({"name":student,"house":"house11"})
print(addhouse)   
```
```js
students = ["Ron","Ali","Doe"]

for i in range(len(students)):
    print(i+1,students[i])
```
```js
students = ["Ron","Ali","Doe"]

for i,student in enumerate(students):
    print(i+1,student)

    #enumerate(iterable,start=0)
```
```js
def main():
    n = int(input("What is n?"))

    for i in range(n):
        print("sheep"*i)

if __name__=="__main__":
    main()        

    #geneators
```
```js
def main():
    n = int(input("What is n?"))

    for s in sheep(n):
        print(s)

def sheep(n):
   flock =[]
   for i in range(n):
       flock.append("sheep"*i)
   return flock    
if __name__=="__main__":
    main()        

    #geneators
```
```js
def main():
    n = int(input("What is n?"))

    for s in sheep(n):
        print(s)

def sheep(n):
   for i in range(n):
      yield "sheep"*i   
if __name__=="__main__":
    main()        

    #yield
```
```js
```
```js
```

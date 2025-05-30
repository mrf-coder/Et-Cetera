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
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```
```js
```

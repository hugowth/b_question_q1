# Question 1
## By your understanding, what are OOP and FP? Please explain the difference with code examples.

### OOP - Object Oriented Programming
It is a programming style with the concept of `class of object`, `Inheritance`, `Polymorphism`, `Abstraction` and `Encapsulation`.

Combine a group of related variables and function to a `Object` and those method will control into the object. We can say is `Encapsulation`.
`Abstraction` - we can say we not need to know all of properties and method inside
```python
class User:
    def  __init__(self, first_name, last_name, email):
        self.first_name = first_name
        self.last_name = last_name
        self.email = email

    def get_user_name(self):
        return '{} {}'.format(self.first_name, self.last_name)

    def get_first_name(self):
        return self.first_name

    def get_last_name(self):
        return self.last_name

    def get_email(self):
        return self.email

user_1 = User('Hugo', 'Wong', 'abc@gmail.com')
print(user_1.get_user_name()) # Hugo Wong
```

`Inheritance` can let you eliminate redundant code, user the `super` to reuse the code
`Polymorphism` can let each object can have a allow method

```python
class Developer(User):
    def __init__(self, first_name, last_name, email):
        super().__init__(first_name, last_name, email)

class Mangaer(User):
    def __init__(self, first_name, last_name, email, user=None):
        super().__init__(first_name, last_name, email)
        if user is None:
            self.user = []
        else:
            self.user = user

    def get_subordinate(self):
        for u in user:
            print(u.user_name)

```

### FP - Function progmramming
Function progmramming is a programming style that will not affect other function. 
The output of function only depend on inputs,
Function progmramming mutating the variable directly,
because the `FP should produce no side-effects`

```javascript
const value = [100000, 1000, 100000]

const toLocaleString = (i) =>{
    return i.toLocaleString();
}

console.log(value.map(toLocaleString)) //["100,000", "1,000", "100,000"]
```
FP can make a function as a arguments to other function.

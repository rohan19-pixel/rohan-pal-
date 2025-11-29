class Person:
    def _init_(self, name):
        self.name = name
        self.__salary = 0
    def set_salary(self, amount):
        self.__salary = amount
    def get_salary(self):
        return self.__salary

class Employee(Person):
    def _init_(self, name, role):
        super()._init_(name)
        self.role = role

p = Employee("Rahul", "Manager")
p.set_salary(50000)
print(p.name, p.role, p.get_salary())

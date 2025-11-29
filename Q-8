class Student:
    def _init_(self, name):
        self.name = name
        self.__internal = 0
        self.__medical_leave = 0
        self.__disciplinary = "Good"
    def update_internal(self, marks):
        if 0 <= marks <= 30:
            self.__internal = marks
    def get_internal(self):
        return self.__internal

s = Student("John")
s.update_internal(27)
print(s.name, s.get_internal())

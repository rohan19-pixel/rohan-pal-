class Staff:
    def _init_(self, name):
        self.name = name

class Doctor(Staff):
    def duty(self):
        return self.name + " treats patients"

class Nurse(Staff):
    def duty(self):
        return self.name + " manages medications"

class Surgeon(Staff):
    def duty(self):
        return self.name + " performs surgery"

class LabTech(Staff):
    def duty(self):
        return self.name + " conducts tests"

workers=[Doctor("A"),Nurse("B"),Surgeon("C"),LabTech("D")]
for w in workers:
    print(w.duty())

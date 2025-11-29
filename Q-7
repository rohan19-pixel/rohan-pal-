class Account:
    def _init_(self):
        self.__balance = 0
    def deposit(self, amt):
        self.__balance += amt
    def withdraw(self, amt):
        if amt <= self.__balance:
            self.__balance -= amt
    def get_balance(self):
        return self.__balance

a = Account()
a.deposit(5000)
a.withdraw(1500)
print(a.get_balance())

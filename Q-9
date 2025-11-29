from abc import ABC, abstractmethod
class Payment(ABC):
    @abstractmethod
    def pay(self, amount):
        pass

class UPI(Payment):
    def pay(self, amount):
        return "UPI Paid " + str(amount)

class Card(Payment):
    def pay(self, amount):
        return "Card Paid " + str(amount)

class Wallet(Payment):
    def pay(self, amount):
        return "Wallet Paid " + str(amount)

for p in [UPI(), Card(), Wallet()]:
    print(p.pay(500))

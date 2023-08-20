class Wallet:
    def __init__(self, balance):
        self.balance = balance
        
    def __add__(self, n):
        self.balance += n
        
    def __eq__(self, other):
        return self.balance == other.balance
    
    def is_empty(self):
        return self.balance == 0

    def my_method(self):
        # Добавьте свое собственное определение метода здесь
        pass

        # Создание экземпляров кошельков
wallet1 = Wallet(100)
wallet2 = Wallet(200)

# Увеличение баланса первого кошелька на 50
wallet1 + 50

# Проверка баланса второго кошелька на ноль
if wallet2.is_empty():
    print("Баланс второго кошелька равен нулю")

# Сравнение двух кошельков
if wallet1 == wallet2:
    print("Балансы кошельков равны")
else:
    print("Балансы кошельков не равны")

# Вызов пользовательского метода
wallet1.my_method()

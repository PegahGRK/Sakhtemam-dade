# Sakhtemam-dade
تمرین ساختمان داده پگاه گورکانی ۱۴۰۲.۹.۳۰
class Expression:
    def __init__(self):
        self.expressions = []

    def insert(self, exp):
        self.expressions.append(exp)

    def delete(self, index):
        if index >= 0 and index < len(self.expressions):
            self.expressions.pop(index)
        else:
            print("Index out of range.")

    def print(self):
        for i in range(len(self.expressions)):
            print(f"{i}: {self.expressions[i]}")

    def add(self, index1, index2):
        if index1 >= 0 and index1 < len(self.expressions) and index2 >= 0 and index2 < len(self.expressions):
            result = self.expressions[index1] + self.expressions[index2]
            self.expressions.append(result)
        else:
            print("Index out of range.")

    def mul(self, index1, index2):
        if index1 >= 0 and index1 < len(self.expressions) and index2 >= 0 and index2 < len(self.expressions):
            result = self.expressions[index1] * self.expressions[index2]
            self.expressions.append(result)
        else:
            print("Index out of range.")


def main():
    expression = Expression()

    while True:
        print("\n1. insert")
        print("2. Delete")
        print("3. Print")
        print("4. Add")
        print("5. Mul")
        print("6. Exit")

        choice = input("Enter your choice: ")

        if choice == '1':
            exp = input("Enter expression: ")
            expression.insert(exp)
        elif choice == '2':
            index = int(input("Enter index to delete: "))
            expression.delete(index)
        elif choice == '3':
            expression.print()
        elif choice == '4':
            index1 = int(input("Enter first index: "))
            index2 = int(input("Enter second index: "))
            expression.add(index1, index2)
        elif choice == '5':
            index1 = int(input("Enter first index: "))
            index2 = int(input("Enter second index: "))
            expression.mul(index1, index2)
        elif choice == '6':
            break
        else:
            print("Invalid choice. Please enter again.")


if name == "__main__":
    main()

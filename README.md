# Expense Tracker

expenses = {}

while True:
    print("\n===== Expense Tracker =====")
    print("1. Add Expense")
    print("2. View Expenses")
    print("3. Total Expense")
    print("4. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        category = input("Enter Category: ")
        amount = float(input("Enter Amount: "))

        if category in expenses:
            expenses[category] += amount
        else:
            expenses[category] = amount

        print("Expense Added Successfully!")

    elif choice == "2":
        print("\nExpenses:")
        for category, amount in expenses.items():
            print(category, ":", amount)

    elif choice == "3":
        total = sum(expenses.values())
        print("Total Expense =", total)

    elif choice == "4":
        print("Thank You!")
        break

    else:
        print("Invalid Choice!")

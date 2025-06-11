tasks = []

def show_tasks():
    print("\nTo-Do List:")
    for i, task in enumerate(tasks, 1):
        print(f"{i}. {task}")
    print()

while True:
    print("Options: [1] Add [2] Show [3] Remove [4] Exit")
    choice = input("Choose: ")

    if choice == '1':
        task = input("Enter task: ")
        tasks.append(task)
    elif choice == '2':
        show_tasks()
    elif choice == '3':
        show_tasks()
        num = int(input("Enter task number to remove: "))
        if 0 < num <= len(tasks):
            tasks.pop(num - 1)
    elif choice == '4':
        break
    else:
        print("Invalid choice. Try again.")

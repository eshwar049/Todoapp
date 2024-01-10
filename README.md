# todo_app.py
class ToDoList:
    def __init__(self):
        self.tasks = []

    def add_task(self, task):
        self.tasks.append(task)

    def show_tasks(self):
        for i, task in enumerate(self.tasks, 1):
            print(f"{i}. {task}")

if __name__ == "__main__":
    todo_list = ToDoList()

    while True:
        print("\n1. Add Task")
        print("2. Show Tasks")
        print("3. Exit")

        choice = input("Enter your choice: ")

        if choice == '1':
            task = input("Enter the task: ")
            todo_list.add_task(task)
        elif choice == '2':
            print("\nTasks:")
            todo_list.show_tasks()
        elif choice == '3':
            break
        else:
            print("Invalid choice. Please try again.")

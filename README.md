```python
class TodoList:
    def __init__(self):
        self.tasks = []

    def add_task(self, task):
        if not isinstance(task, str):
            raise ValueError("Task must be a string")
        if task == "":
            raise ValueError("Task cannot be an empty string")
        self.tasks.append(task)

    def remove_task(self, task):
        if task in self.tasks:
            self.tasks.remove(task)
        else:
            raise ValueError("Task not found in the list")

    def list_tasks(self):
        return self.tasks.copy()

# Example usage:
todo = TodoList()
todo.add_task("Learn Python")
todo.add_task("Build a project")
print(todo.list_tasks())  # Output: ['Learn Python', 'Build a project']
todo.remove_task("Learn Python")
print(todo.list_tasks())  # Output: ['Build a project']
```
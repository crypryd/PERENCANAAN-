class Task:
    def __init__(self, name, due_date):
        self.name = name
        self.due_date = due_date
        
    def __str__(self):
        return f"{self.name} is due on {self.due_date}"

class Planner:
    def __init__(self):
        self.tasks = []
        
    def add_task(self, task):
        self.tasks.append(task)
        
    def remove_task(self, task_name):
        for i, task in enumerate(self.tasks):
            if task.name == task_name:
                del self.tasks[i]
                break
                
    def show_tasks(self):
        for task in self.tasks:
            print(task)
            
planner = Planner()
planner.add_task(Task("Finish Homework", "Tomorrow"))
planner.add_task(Task("Go to Gym", "Today"))
planner.show_tasks()
planner.remove_task("Finish Homework")
planner.show_tasks()
# PERENCANAAN-

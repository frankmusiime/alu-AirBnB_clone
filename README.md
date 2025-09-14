# alu-AirBnB
An AirBnB clone.

---

## Description 🏠
HBnB is a complete web application, integrating **database storage**, a **back-end API**, and **front-end interfacing** in a clone of AirBnB.  

This repository is the **first step** towards building the full application.  
It focuses on:
- A custom **command-line interface (CLI)** for data management  
- Base classes for data storage and handling  

The console manages the creation, retrieval, updating, and destruction of objects (e.g., Users, Places).

---

## How to Start It ⚙️
1. Clone the repository:
   ```bash
   git clone https://github.com/<frankmusiime>/alu-AirBnB_clone.git
   cd alu-AirBnB_clone
Run the console:

bash
Copy code
./console.py
Once started, the prompt will appear:

bash
Copy code
(hbnb)
How to Use It 💻
The console supports interactive and non-interactive modes.

Interactive Mode
bash
Copy code
$ ./console.py
(hbnb) help

## Documented commands (type help <topic>):
========================================

EOF  help  quit
(hbnb) quit
$
Non-Interactive Mode
bash
Copy code
$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================

EOF  help  quit
(hbnb)
$
Commands 📝
create <class> → Creates a new instance

show <class> <id> → Shows an object

destroy <class> <id> → Deletes an object

all [<class>] → Shows all objects or all objects of a class

update <class> <id> <attr_name> "<value>" → Updates object attributes

quit or EOF → Exits the console

Alternative Syntax 🔀
Commands can also be used with dot notation:

php-template
Copy code
<class name>.<command>([<id>[name_arg value_arg]|[kwargs]])
Examples:

User.all() → List all User objects

User.count() → Count User instances

User.show("1234-5678-9012") → Show a specific User

User.destroy("1234-5678-9012") → Delete a specific User

User.update("1234-5678-9012", {"name": "Alice", "age": 30}) → Update multiple attributes

Examples 🚀
Create an object
bash
Copy code
(hbnb) create BaseModel
3aa5babc-efb6-4041-bfe9-3cc9727588f8
Show an object
bash
Copy code
(hbnb) show BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
[BaseModel] (3aa5babc-efb6-4041-bfe9-3cc9727588f8) {'id': '3aa5babc...', 'created_at': ..., 'updated_at': ...}
Destroy an object
bash
Copy code
(hbnb) destroy BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
(hbnb) show BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
** no instance found **
Update an object
bash
Copy code
(hbnb) update BaseModel b405fc64-9724-498f-b405-e4071c3d857f first_name "person"
(hbnb) show BaseModel b405fc64-9724-498f-b405-e4071c3d857f
[BaseModel] (...) {'first-name': 'person'}
Project Organization 📂
console.py → Entry point for the command interpreter

models/ → Contains model classes (BaseModel, User, etc.)

tests/ → Unit tests

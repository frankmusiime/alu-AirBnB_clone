# AirBnB Clone - The Console

## Description
This project is the first step in building a full web application: the AirBnB clone.  
In this step, we create a **command interpreter** (the console) that allows us to manage AirBnB objects.

The console works like a shell but is limited to specific use cases. It allows you to:
- Create new objects (e.g., a new User or a new Place)
- Retrieve an object from storage
- Perform operations on objects (count, list all, etc.)
- Update attributes of an object
- Destroy an object

This first version uses a **FileStorage engine**:
- Objects are stored in memory (Python dictionary).
- Objects are serialized into a JSON file (`file.json`).
- Objects can be deserialized back from the JSON file.

Future steps of the project will add:
- Web static (HTML/CSS)
- Database storage
- APIs
- Web front-end integration

---

## How to Start the Console
1. Clone the repository:
   ```bash
   git clone https://github.com/<frankmusiime>/alu-AirBnB_clone.git
   cd alu-AirBnB_clone
Make sure console.py is executable:

bash
Copy code
chmod +x console.py
Start the console in interactive mode:

bash
Copy code
./console.py
Start the console in non-interactive mode:

bash
Copy code
echo "help" | ./console.py
How to Use the Console
The console supports various commands. The main ones are:

help → Displays available commands

quit → Exits the console

EOF → Exits the console (Ctrl+D)

Object-specific commands (examples shown for User):

create <class> → Creates a new object and prints its id

show <class> <id> → Displays the string representation of an object

destroy <class> <id> → Deletes an object

all [class] → Shows all objects, or all objects of a class

update <class> <id> <attribute> <value> → Updates an attribute

Examples
Interactive Mode
bash
Copy code
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) create User
d9f1c0f2-23d4-4f2e-b2fd-0a5c2b83e1e2
(hbnb) show User d9f1c0f2-23d4-4f2e-b2fd-0a5c2b83e1e2
[User] (d9f1c0f2-23d4-4f2e-b2fd-0a5c2b83e1e2) {'id': 'd9f1c0f2-...', 'created_at': '2025-09-14T12:00:00', 'updated_at': '2025-09-14T12:00:00'}
(hbnb) quit
$
Non-Interactive Mode
bash
Copy code
$ echo "create User" | ./console.py
d9f1c0f2-23d4-4f2e-b2fd-0a5c2b83e1e2
Requirements
Python 3.8.5 (Ubuntu 20.04 LTS)

pycodestyle (PEP8 style guide)

Project Structure
markdown
Copy code
.
├── AUTHORS
├── README.md
├── console.py
├── models/
│   ├── __init__.py
│   ├── base_model.py
│   └── engine/
│       └── file_storage.py
└── tests/
    └── test_models/
        ├── test_base_model.py
        └── ...
Authors
Frank Musiime

Saad Byiringiro

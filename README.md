alu-AirBnB 🏠

An AirBnB clone (The Console).

📖 Description

HBnB is a complete web application project, integrating:

Database storage

Back-end API

Front-end interface

This repository is the first step of the AirBnB Clone. It provides:

A custom command-line interface (CLI) for data management

The base classes for object storage

The console allows you to create, retrieve, update, and delete objects such as User, Place, etc.

💻 Usage
1. Clone this repository
git clone https://github.com/<your-username>/alu-AirBnB_clone.git
cd alu-AirBnB_clone

2. Run the console
./console.py

3. Prompt

When the console runs, the following prompt will appear:

(hbnb)


This prompt indicates you are in the HBnB console.

🛠️ Commands

create → Creates an instance based on a given class

destroy → Destroys an object based on class and UUID

show → Shows an object based on class and UUID

all → Shows all objects, or all objects of a given class

update → Updates attributes of an object based on class and UUID

quit / EOF → Exits the program

🔄 Alternative Syntax

You can also use an advanced syntax:

<class_name>.<command>([<id>[name_arg value_arg]|[kwargs]])

Advanced Commands

all → Shows all objects of a class

count → Returns number of object instances by class

show → Shows an object by class and UUID

destroy → Destroys an object by class and UUID

update → Updates attributes of an object by class and UUID

📌 Examples
Primary Command Syntax
Example 0: Create an object
(hbnb) create BaseModel
3aa5babc-efb6-4041-bfe9-3cc9727588f8

Example 1: Show an object
(hbnb) show BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
[BaseModel] (3aa5babc-efb6-4041-bfe9-3cc9727588f8) {'id': '3aa5babc-efb6-4041-bfe9-3cc9727588f8', 'created_at': datetime.datetime(...), 'updated_at': datetime.datetime(...)}

Example 2: Destroy an object
(hbnb) destroy BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
(hbnb) show BaseModel 3aa5babc-efb6-4041-bfe9-3cc9727588f8
** no instance found **

Example 3: Update an object
(hbnb) update BaseModel b405fc64-9724-498f-b405-e4071c3d857f first_name "person"
(hbnb) show BaseModel b405fc64-9724-498f-b405-e4071c3d857f
[BaseModel] (...) {'first_name': 'person', ...}

Alternative Syntax
Example 0: Show all User objects
(hbnb) User.all()
["[User] (99f45908-1d17-46d1-9dd2-b7571128115b) {...}", "[User] (98bea5de-9cb0-4d78-8a9d-c4de03521c30) {...}"]

Example 1: Destroy a User
(hbnb) User.destroy("99f45908-1d17-46d1-9dd2-b7571128115b")
(hbnb) User.all()
["[User] (98bea5de-9cb0-4d78-8a9d-c4de03521c30) {...}"]

Example 2: Update User (by attribute)
(hbnb) User.update("98bea5de-9cb0-4d78-8a9d-c4de03521c30", name "Todd the Toad")

Example 3: Update User (by dictionary)
(hbnb) User.update("98bea5de-9cb0-4d78-8a9d-c4de03521c30", {'name': 'Fred the Frog', 'age': 9})

✒️ Authors

Frank MUSIIME

Saad BYIRINGIRO

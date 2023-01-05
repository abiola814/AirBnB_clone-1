# 0x00. AirBnB clone - The console
Foundations - Higher-level programming ― AirBnB clone

###### :copyright: **[Holberton School](https://www.holbertonschool.com/)**
by _Guillaume_

## Learning Objectives
* Third teamwork
* How to create a Python package
* How to create a command interpreter in Python using the ```cmd``` module
* What is Unit testing and how to implement it in a large project
* How to serialize and deserialize a Class
* How to write and read a JSON file
* How to manage ```datetime```
* What is an ```UUID```
* What is ```*args``` and how to use it
* What is ```**kwargs``` and how to use it
* How to handle named arguments in a function

## Resources
* [AirBnB clone](https://intranet.hbtn.io/concepts/74)
* [2 Airbnb console](https://www.youtube.com/watch?v=jeJwRB33YNg&feature=youtu.be)
* [HBNB project overview](https://www.youtube.com/watch?v=E12Xc3H2xqo&feature=youtu.be)
* [cmd module](https://docs.python.org/3.4/library/cmd.html)
* [packages](https://intranet.hbtn.io/concepts/66)
* [uuid module](https://docs.python.org/3.4/library/uuid.html)
* [datetime](https://docs.python.org/3.4/library/datetime.html)
* [unittest module](https://docs.python.org/3.4/library/unittest.html#module-unittest)
* [args/kwargs](https://pythontips.com/2013/08/04/args-and-kwargs-in-python-explained/)
* [Python test cheatsheet](https://www.pythonsheets.com/notes/python-tests.html)
* [unittest module](https://docs.python.org/3.4/library/unittest.html#module-unittest)
* [HBNB - The console](https://www.youtube.com/watch?v=p00ES-5K4C8&feature=youtu.be)

## Tasks
* [x] 0. README, AUTHORS
* [x] 1. Be PEP8 compliant!
* [x] 2. Unittests
* [x] 3. BaseModel
* [x] 4. Create BaseModel from dictionary
* [x] 5. Store first object
* [x] 6. Console 0.0.1
* [x] 7. Console 0.1
* [x] 8. First User
* [x] 9. More classes!
* [x] 10. Console 1.0
* [ ] 11. All instances by class name
* [ ] 12. Count instances
* [ ] 13. Show
* [ ] 14. Destroy
* [ ] 15. Update
* [ ] 16. Update from dictionary
* [ ] 17. Unittests for the Console!

## Developers
abdul gafar and oladunjoye abiola
- [website](https://mjobi.com/)

:man_technologist: :books: :computer: :globe_with_meridians:

## Description of the project:
The goal of the project is to deploy on your server a simple copy of the AirBnB website.

This is the first part that is composed by an interpreter of command line that saves the data of instances in a JSON file. It is developed in Python language using mainly the class Cmd.
This project have implemented into the development the unit tests for its general working, used for this the Unittest framework.

## Description of the command interpreter:
- How to start it
Start the console by executing the 'console.py' file:
```bash
./console.py
```
- How to use it
The 'prompt (hbnb)' tells you that the console is ready to receive instructions, type the instruction:
```bash
(hbnb) 
```
- Example
The 'help' command shows all commands available in the console:
```bash
(hbnb) help
```
(The 'help' command is built into Cmd)

Output:
```bash
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  all  create  destroy  help  quit  show  update

(hbnb) 
```

## Our commands:

- 'EOF': Exit the program.
```bash
(hbnb) EOF
vagrant@vagrant-ubuntu-trusty-64:~/AirBnB_clone$ 
```

- 'all': Prints all string representation of all instances based or not on the class name.
```bash
(hbnb) all
[]
(hbnb) 
```
Shows empty square brackets when not exist instances created.

- 'create': Create a new instance.
```bash
(hbnb) create BaseModel
```
Generate an id automatically
```bash
(hbnb) create BaseModel
da7baf7d-6cf9-406b-9360-da1620dfd622
(hbnb) 
```

- 'update': Updates an instance based on the class name an id by adding or updating attribute.
```bash
(hbnb) update BaseModel da7baf7d-6cf9-406b-9360-da1620dfd622 name "Betty"
(hbnb) 
```

- 'show': Print the string representation of an instance based on the class name and id.
```bash
(hbnb) show BaseModel da7baf7d-6cf9-406b-9360-da1620dfd622
[BaseModel] (da7baf7d-6cf9-406b-9360-da1620dfd622) {'id': 'da7baf7d-6cf9-406b-9360-da1620dfd622', 'updated_at': datetime.datetime(2020, 2, 20, 16, 50, 19, 303808), 'created_at': datetime.datetime(2020, 2, 20, 16, 50, 19, 303779), 'name': 'Betty'}
(hbnb) 
```

- 'all': Prints all string representation of all instances based or not on the class name.
```bash
(hbnb) all
["[BaseModel] (da7baf7d-6cf9-406b-9360-da1620dfd622) {'id': 'da7baf7d-6cf9-406b-9360-da1620dfd622', 'updated_at': datetime.datetime(2020, 2, 20, 16, 50, 19, 303808), 'created_at': datetime.datetime(2020, 2, 20, 16, 50, 19, 303779), 'name': 'Betty'}", "[BaseModel] (3e33d99d-ae43-4a9c-b2aa-e2c58b2122af) {'id': '3e33d99d-ae43-4a9c-b2aa-e2c58b2122af', 'updated_at': datetime.datetime(2020, 2, 20, 16, 51, 45, 868183), 'created_at': datetime.datetime(2020, 2, 20, 16, 51, 45, 868098)}", "[BaseModel] (6a29fe15-856c-49ab-9774-1637b1f07d8c) {'id': '6a29fe15-856c-49ab-9774-1637b1f07d8c', 'updated_at': datetime.datetime(2020, 2, 20, 16, 51, 55, 606952), 'created_at': datetime.datetime(2020, 2, 20, 16, 51, 55, 606919)}", "[BaseModel] (6ec48ab4-cf1e-44ca-966c-103d454567c2) {'id': '6ec48ab4-cf1e-44ca-966c-103d454567c2', 'updated_at': datetime.datetime(2020, 2, 20, 16, 51, 48, 63180), 'created_at': datetime.datetime(2020, 2, 20, 16, 51, 48, 63146)}"]
(hbnb) 
```
Now shows all instances created.

- 'destroy': Deletes an instance based on the class name and id.
```bash
(hbnb) destroy BaseModel da7baf7d-6cf9-406b-9360-da1620dfd622
```

- 'quit': Exit the program.
```bash
(hbnb) quit
vagrant@vagrant-ubuntu-trusty-64:~/AirBnB_clone$ 
```

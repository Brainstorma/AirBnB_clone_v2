# AirBnB Clone - MySQL
<center> <h1>AirBnB Clone</h1> </center>

### This is a Full-Stack AirBnB Clone program that uses Python, SQL, SQLalchemy, RESTfulApi, jquery, Html, CSS

---

<center><h3>Repository Contents by Project Task</h3> </center>

| Tasks | Files | Description |
| ----- | ----- | ------ |
| 0: Authors/README File | [AUTHORS](./AUTHORS) | Project authors |
| 1: Pep8 | N/A | All code is pep8 compliant|
| 2: Unit Testing | [/tests](./tests) | All class-defining modules are unittested |
| 3. Make BaseModel | [/models/base_model.py](./models/base_model.py) | Defines a parent class to be inherited by all model classes|
| 4. Update BaseModel w/ kwargs | [/models/base_model.py](./models/base_model.py) | Add functionality to recreate an instance of a class from a dictionary representation|
| 5. Create FileStorage class | [/models/engine/file_storage.py](./models/engine/file_storage.py) [/models/_ _init_ _.py](./models/__init__.py) [/models/base_model.py](./models/base_model.py) | Defines a class to manage persistent file storage system|
| 6. Console 0.0.1 | [console.py](./console.py) | Add basic functionality to console program, allowing it to quit, handle empty lines and ^D |
| 7. Console 0.1 | [console.py](./console.py) | Update the console with methods allowing the user to create, destroy, show, and update stored data |
| 8. Create User class | [console.py](./console.py) [/models/engine/file_storage.py](./models/engine/file_storage.py) [/models/user.py](./models/user.py) | Dynamically implements a user class |
| 9. More Classes | [/models/user.py](./models/user.py) [/models/place.py](./models/place.py) [/models/city.py](./models/city.py) [/models/amenity.py](./models/amenity.py) [/models/state.py](./models/state.py) [/models/review.py](./models/review.py) | Dynamically implements more classes |
| 10. Console 1.0 | [console.py](./console.py) [/models/engine/file_storage.py](./models/engine/file_storage.py) | Update the console and file storage system to work dynamically with all  classes update file storage |
<br>
<br>
<center> <h2>General Use</h2> </center>

Welcome to the AirBnB Clone project using the MySQL database for data storage. This project is part of the ALX curriculum focused on teaching software engineering skills. It is a collaborative project with multiple tasks that build on each other to create an AirBnB clone.

The AirBnB clone project is a demonstration of a functioning software application that is designed to mimic AirBnB. It is built in different stages, integrating various advanced features to make it a more professional and robust system.

In the MySQL stage, we use the MySQL database to store and retrieve data instead of a JSON file from the previous stage.

## Files and Directories

Here is a list of files and directories that make up our MySQL stage:

| File/Directories | Description |
| --- | --- |
| `models/base_model.py` | Defines the BaseModel class from which all other classes inherit. |
| `models/__init__.py` | An empty file to indicate that this a Python package. |
| `models/user.py` | Defines the User class. |
| `models/state.py` | Defines the State class. |
| `tests/__init__.py` | An empty file to indicate that this a Python package. |
| `tests/test_models/test_base_model.py` | Defines the tests for the BaseModel class. |
| `tests/test_models/test_user.py` | Defines the tests for the User class. |
| `tests/test_models/test_state.py` | Defines the tests for the State class. |
| `tests/test_models/test_engine` | Defines the tests for the DB storage engine. |
| `models/engine` | Contains the DB storage engine. |
| `tests/test_models/__init__.py` | An empty file to indicate that this a Python package. |
| `setup_mysql_dev.sql` | SQL script to set up the MySQL database for development. |
| `setup_mysql_test.sql` | SQL script to set up the MySQL database for testing. |

## Requirements

Before running the database, make sure you have the following requirements installed:

- Python3 (v3.4 or later)
- MySQL (v5.7 or later)
- MySQLdb module

You can install MySQLdb using: 

```
$ pip install mysqlclient
```

## Usage

1. Clone the repository 

```
$ git clone git@github.com:brainstorma/AirBnB_clone_v2.git
```

2. Navigate to the project directory 

```
$ cd AirBnB_clone_v2
```

3. Execute the SQL scripts to set up the database 

- For development: 

```
$ cat setup_mysql_dev.sql | mysql -uroot -proot -hlocalhost -Dhbnb_dev
```

- For testing: 

```
$ cat setup_mysql_test.sql | mysql -uroot -proot -hlocalhost -Dhbnb_test
```

4. Run the application 

```
$ ./console.py
```

## Console Commands

The console is the command-line interface to our AirBnB clone project. It communicates with the MySQL database to manage objects stored in the DB.

The console supports the following commands:

| Command | Arguments | Example | Description |
| --- | --- | --- | --- |
| `create` | `<class>` | `create User` | Creates a new instance of the specified class. |
| `show` | `<class> <id>` | `show User 123` | Prints a string representation of an instance based on the class name and id. |
| `destroy` | `<class> <id>` | `destroy User 123` | Deletes an instance based on the class name and id. |
| `all` | `[<class>]` | `all User` | Prints all string representations of all instances, or those of a specified class. |
| `update` | `<class> <id> <attr_name> <attr_val>` or `<class> <id> <dictionary>` | `update User 123 email "john@doe.com"` or `update User 123 {"email": "john@doe.com"}` | Updates an instance based on the class name and id using a key/value pair or dictionary. |
| `count` | `<class>` | `count User` | Retrieves the number of instances of a class. |
| `quit` | N/A | `quit` | Quits the console. |
| `help` | N/A | `help` | Prints a list of available commands, or displays help for a specified command. |

## Testing

You can run the unit tests using the following command:

```
$ python3 -m unittest discover tests
```

This will run all tests in the `tests/` directory.

## Authors

This project was a collaborative effort by:

-[Brainstorma](https://github.com/brainstorma)

-[Amina Niass](https://github.com/Amy19921)


## Tasks

Here are links to all the repository tasks completed as part of the AirBnB Clone - MySQL stage:

| Task | Description |
| --- | --- |
| [0. Fork Me if You Can](./AirBnB_clone_v2) | Create a fork of the AirBnB clone repository on GitHub. |
| [1. Bug Free!](./models) | Fix any bugs in the BaseModel class from the previous stage. |
| [2. Console Improvements](./models) | Update the console to use your MySQL storage engine instead of a JSON file. |
| [3. MySQL Setup Development](./setup_mysql_dev.sql) | Write a script to set up a MySQL database for the development environment. |
| [4. MySQL Setup Test](./setup_mysql_test.sql) | Write a separate script to set up a MySQL database for the testing environment. |
| [5. Delete object](./db_storage.py) | Update DBStorage to implement the `delete` method. |
| [6. DBStorage - new engine](./db_storage.py) | Update DBStorage to use SQLAlchemy instead of MySQLdb. |
| [7. DBStorage - User](./models/user.py) | Update the User class to work with the new DBStorage engine. |
| [8. DBStorage - Place](./models/place.py) | Add support for the Place class to work with the new DBStorage engine. |
| [9. DBStorage - Review](./models/review.py) | Add support for the Review class to work with the new DBStorage engine. |
| [10. DBStorage - Amenity... and BOOM!](./models/place.py) | In this task, the DBStorage engine is further improved to manage a new object called an Amenity. An Amenity is a feature of a Place to stay, such as a pool, hot tub or gym. Additionally, BOOM! is added as a command to the console, which will print "boom!" every time it is entered. |

## File Descriptions
[console.py](console.py) - the console contains the entry point of the command interpreter. 
List of commands this console current supports:
* `EOF` - exits console 
* `quit` - exits console
* `<emptyline>` - overwrites default emptyline method and does nothing
* `create` - Creates a new instance of`BaseModel`, saves it (to the JSON file) and prints the id
* `destroy` - Deletes an instance based on the class name and id (save the change into the JSON file). 
* `show` - Prints the string representation of an instance based on the class name and id.
* `all` - Prints all string representation of all instances based or not on the class name. 
* `update` - Updates an instance based on the class name and id by adding or updating attribute (save the change into the JSON file). 

#### `models/` directory contains classes used for this project:
[base_model.py](/models/base_model.py) - The BaseModel class from which future classes will be derived
* `def __init__(self, *args, **kwargs)` - Initialization of the base model
* `def __str__(self)` - String representation of the BaseModel class
* `def save(self)` - Updates the attribute `updated_at` with the current datetime
* `def to_dict(self)` - returns a dictionary containing all keys/values of the instance

Classes inherited from Base Model:
* [amenity.py](/models/amenity.py)
* [city.py](/models/city.py)
* [place.py](/models/place.py)
* [review.py](/models/review.py)
* [state.py](/models/state.py)
* [user.py](/models/user.py)

#### `/models/engine` directory contains File Storage class that handles JASON serialization and deserialization :
[file_storage.py](/models/engine/file_storage.py) - serializes instances to a JSON file & deserializes back to instances
* `def all(self)` - returns the dictionary __objects
* `def new(self, obj)` - sets in __objects the obj with key <obj class name>.id
* `def save(self)` - serializes __objects to the JSON file (path: __file_path)
* ` def reload(self)` -  deserializes the JSON file to __objects

#### `/tests` directory contains all unit test cases for this project:
[/test_models/test_base_model.py](/tests/test_models/test_base_model.py) - Contains the TestBaseModel and TestBaseModelDocs classes
TestBaseModelDocs class:
* `def setUpClass(cls)`- Set up for the doc tests
* `def test_pep8_conformance_base_model(self)` - Test that models/base_model.py conforms to PEP8
* `def test_pep8_conformance_test_base_model(self)` - Test that tests/test_models/test_base_model.py conforms to PEP8
* `def test_bm_module_docstring(self)` - Test for the base_model.py module docstring
* `def test_bm_class_docstring(self)` - Test for the BaseModel class docstring
* `def test_bm_func_docstrings(self)` - Test for the presence of docstrings in BaseModel methods

TestBaseModel class:
* `def test_is_base_model(self)` - Test that the instatiation of a BaseModel works
* `def test_created_at_instantiation(self)` - Test created_at is a pub. instance attribute of type datetime
* `def test_updated_at_instantiation(self)` - Test updated_at is a pub. instance attribute of type datetime
* `def test_diff_datetime_objs(self)` - Test that two BaseModel instances have different datetime objects

[/test_models/test_amenity.py](/tests/test_models/test_amenity.py) - Contains the TestAmenityDocs class:
* `def setUpClass(cls)` - Set up for the doc tests
* `def test_pep8_conformance_amenity(self)` - Test that models/amenity.py conforms to PEP8
* `def test_pep8_conformance_test_amenity(self)` - Test that tests/test_models/test_amenity.py conforms to PEP8
* `def test_amenity_module_docstring(self)` - Test for the amenity.py module docstring
* `def test_amenity_class_docstring(self)` - Test for the Amenity class docstring

[/test_models/test_city.py](/tests/test_models/test_city.py) - Contains the TestCityDocs class:
* `def setUpClass(cls)` - Set up for the doc tests
* `def test_pep8_conformance_city(self)` - Test that models/city.py conforms to PEP8
* `def test_pep8_conformance_test_city(self)` - Test that tests/test_models/test_city.py conforms to PEP8
* `def test_city_module_docstring(self)` - Test for the city.py module docstring
* `def test_city_class_docstring(self)` - Test for the City class docstring

[/test_models/test_file_storage.py](/tests/test_models/test_file_storage.py) - Contains the TestFileStorageDocs class:
* `def setUpClass(cls)` - Set up for the doc tests
* `def test_pep8_conformance_file_storage(self)` - Test that models/file_storage.py conforms to PEP8
* `def test_pep8_conformance_test_file_storage(self)` - Test that tests/test_models/test_file_storage.py conforms to PEP8
* `def test_file_storage_module_docstring(self)` - Test for the file_storage.py module docstring
* `def test_file_storage_class_docstring(self)` - Test for the FileStorage class docstring

[/test_models/test_place.py](/tests/test_models/test_place.py) - Contains the TestPlaceDoc class:
* `def setUpClass(cls)` - Set up for the doc tests
* `def test_pep8_conformance_place(self)` - Test that models/place.py conforms to PEP8.
* `def test_pep8_conformance_test_place(self)` - Test that tests/test_models/test_place.py conforms to PEP8.
* `def test_place_module_docstring(self)` - Test for the place.py module docstring
* `def test_place_class_docstring(self)` - Test for the Place class docstring

[/test_models/test_review.py](/tests/test_models/test_review.py) - Contains the TestReviewDocs class:
* `def setUpClass(cls)` - Set up for the doc tests
* `def test_pep8_conformance_review(self)` - Test that models/review.py conforms to PEP8
* `def test_pep8_conformance_test_review(self)` - Test that tests/test_models/test_review.py conforms to PEP8
* `def test_review_module_docstring(self)` - Test for the review.py module docstring
* `def test_review_class_docstring(self)` - Test for the Review class docstring

[/test_models/state.py](/tests/test_models/test_state.py) - Contains the TestStateDocs class:
* `def setUpClass(cls)` - Set up for the doc tests
* `def test_pep8_conformance_state(self)` - Test that models/state.py conforms to PEP8
* `def test_pep8_conformance_test_state(self)` - Test that tests/test_models/test_state.py conforms to PEP8
* `def test_state_module_docstring(self)` - Test for the state.py module docstring
* `def test_state_class_docstring(self)` - Test for the State class docstring

[/test_models/user.py](/tests/test_models/test_user.py) - Contains the TestUserDocs class:
* `def setUpClass(cls)` - Set up for the doc tests
* `def test_pep8_conformance_user(self)` - Test that models/user.py conforms to PEP8
* `def test_pep8_conformance_test_user(self)` - Test that tests/test_models/test_user.py conforms to PEP8
* `def test_user_module_docstring(self)` - Test for the user.py module docstring
* `def test_user_class_docstring(self)` - Test for the User class docstring

You can also use any executable file or script in your PATH as a command.

## Installation

```bash
git clone https://github.com/brainstorma/AirBnB_clone.git
```

change to the `AirBnb` directory and run the command:

```bash
 ./console.py
```

### Execution

In interactive mode

```bash
$ ./console.py
(hbnb) help
Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
(hbnb)
(hbnb) quit
$
```

in Non-interactive mode

```bash
$ echo "help" | ./console.py
(hbnb)
Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)
Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
$
```

## Testing

All the test are defined in the `tests` folder.

### Documentation

* Modules:

```python
python3 -c 'print(__import__("my_module").__doc__)'
```

* Classes:

```python
python3 -c 'print(__import__("my_module").MyClass.__doc__)'
```

* Functions (inside and outside a class):

```python
python3 -c 'print(__import__("my_module").my_function.__doc__)'
```

and

```python
python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)'
```

### Python Unit Tests

* unittest module
* File extension ``` .py ```
* Files and folders star with ```test_```
* Organization:for ```models/base.py```, unit tests in: ```tests/test_models/test_base.py```
* Execution command: ```python3 -m unittest discover tests```
* or: ```python3 -m unittest tests/test_models/test_base.py```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

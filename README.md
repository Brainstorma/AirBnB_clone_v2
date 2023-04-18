# AirBnB Clone - MySQL

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

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

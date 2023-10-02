# AirBnB Clone - Command Line Interface

The AirBnB Clone Command Line Interface (CLI) is the initial phase of the AirBnB project at Holberton School, designed to teach fundamental concepts of higher-level programming. The ultimate objective of the AirBnB project is to deploy a simplified version of the AirBnB website, known as HBnB. This CLI serves as a command interpreter for managing objects related to the HBnB website.

## Key Functionalities

The CLI offers the following core functionalities:

- Create a new object, such as a User or Place.
- Retrieve an object from a file or database.
- Perform operations on objects, including counting and computing statistics.
- Update attributes of an object.
- Destroy (delete) an object.

## Table of Contents

- [Environment](#environment)
- [Installation](#installation)
- [File Descriptions](#file-descriptions)
- [Usage](#usage)
- [Examples](#examples)
- [Bugs](#bugs)
- [Authors](#authors)
- [License](#license)

## Environment

This project is developed and tested on Ubuntu 14.04 LTS using Python 3 (version 3.4.3).

## Installation

To set up the CLI, follow these steps:

1. Clone this repository: `git clone https://github.com/alexaorrico/AirBnB_clone.git`
2. Access the AirBnB directory: `cd AirBnB_clone`
3. Run the CLI interactively: `./console` and enter commands.
4. Run the CLI non-interactively: `echo "<command>" | ./console.py`

## File Descriptions

### `console.py`

- The `console.py` file serves as the entry point for the command interpreter.
- Supported commands include `EOF`, `quit`, `<emptyline>`, `create`, `destroy`, `show`, `all`, and `update`.

### `models/` Directory

This directory contains classes used for the project:

- [base_model.py](/models/base_model.py)
  - The `BaseModel` class serves as the foundation for future classes.
  - Key methods include `__init__`, `__str__`, `save`, and `to_dict`.
- Classes inherited from `BaseModel`:
  - [amenity.py](/models/amenity.py)
  - [city.py](/models/city.py)
  - [place.py](/models/place.py)
  - [review.py](/models/review.py)
  - [state.py](/models/state.py)
  - [user.py](/models/user.py)

### `models/engine/` Directory

This directory contains the `FileStorage` class responsible for JSON serialization and deserialization:

- [file_storage.py](/models/engine/file_storage.py)
  - Methods include `all`, `new`, `save`, and `reload`.

### `tests/` Directory

This directory contains unit test cases for the project:

- [/tests/test_models/test_base_model.py](/tests/test_models/test_base_model.py)
  - Contains `TestBaseModel` and `TestBaseModelDocs` classes.
  - Test cases cover PEP8 conformance, module docstrings, and class docstrings.
- [/tests/test_models/test_amenity.py](/tests/test_models/test_amenity.py)
  - Contains the `TestAmenityDocs` class with similar test cases.
- [/tests/test_models/test_city.py](/tests/test_models/test_city.py)
  - Contains the `TestCityDocs` class with similar test cases.
- [/tests/test_models/test_file_storage.py](/tests/test_models/test_file_storage.py)
  - Contains the `TestFileStorageDocs` class with similar test cases.
- [/tests/test_models/test_place.py](/tests/test_models/test_place.py)
  - Contains the `TestPlaceDoc` class with similar test cases.
- [/tests/test_models/test_review.py](/tests/test_models/test_review.py)
  - Contains the `TestReviewDocs` class with similar test cases.
- [/tests/test_models/test_state.py](/tests/test_models/test_state.py)
  - Contains the `TestStateDocs` class with similar test cases.
- [/tests/test_models/test_user.py](/tests/test_models/test_user.py)
  - Contains the `TestUserDocs` class with similar test cases.

## Usage

Example of using the CLI:

```bash
vagrantAirBnB_clone$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  all  create  destroy  help  quit  show  update

(hbnb) all MyModel
** class doesn't exist **
(hbnb) create BaseModel
7da56403-cc45-4f1c-ad32-bfafeb2bb050
(hbnb) all BaseModel
[[BaseModel] (7da56403-cc45-4f1c-ad32-bfafeb2bb050) {'updated_at': datetime.datetime(2017, 9, 28, 9, 50, 46, 772167), 'id': '7da56403-cc45-4f1c-ad32-bfafeb2bb050', 'created_at': datetime.datetime(2017, 9, 28, 9, 50, 46, 772123)}]
(hbnb) show BaseModel 7da56403-cc45-4f1c-ad32-bfafeb2bb050
[BaseModel] (7da56403-cc45-4f1c-ad32-bfafeb2bb050) {'updated_at': datetime.datetime(2017, 9, 28, 9, 50, 46, 772167), 'id': '7da56403-cc45-4f1c-ad32-bfafeb2bb050', 'created_at': datetime.datetime(2017, 9, 28, 9, 50, 46, 772123)}
(hbnb) destroy BaseModel 7da56403-cc45-4f1c-ad32-bfafeb2bb050
(hbnb) show BaseModel 7da56403-cc45-4f1c-ad32-bfafeb2bb050
** no instance found **
(hbnb) quit
```

## Bugs

No known bugs at this time.

## Authors

- Samuel Chigozie - [Github](https://github.com/Samuelchigozie)
- Ifeoluwa Seriki - [Github](https://github.com/alicecodes1)

## License

This project is in the public domain and has no copyright protection.

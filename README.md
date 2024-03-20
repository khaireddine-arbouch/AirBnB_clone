# AirBnB Clone Console

Welcome to the AirBnB Clone Console, the initial component of our project aimed at replicating some functionalities of the renowned accommodation rental platform, Airbnb.

## Table of Contents

* [1. Introduction](#1-Introduction)
* [2. Tools](#2-Tools)
* [3. Installation](#3-Installation)
* [4. Testing](#4-Testing)
* [5. Usage](#5-Usage)
* [6. Authors](#6-Authors)
* [7. License](#7-License)

## 1. Introduction

The AirBnB Clone Console serves as a Python-based Command-Line Interface (CLI) designed to manage AirBnB objects like users, states, cities, places, and more. This console facilitates various operations on these objects, including creation, retrieval, updating, and deletion.

### Overview

The console facilitates the following tasks:

- Creating new objects
- Retrieving objects from files
- Performing operations on objects
- Destroying objects

## 2. Tools

This project utilizes the following tools:

- [Ubuntu](https://ubuntu.com/)
- [GNU Bash](https://www.gnu.org/software/bash/)
- [Python](https://www.python.org)
- [Visual Studio Code](https://code.visualstudio.com/)
- [Git](https://git-scm.com/)
- [GitHub](https://github.com)

### Style Guidelines

- Code style adheres to [PEP8](https://pep8.org/).

## 3. Installation

Follow these steps to install the AirBnB Clone Console:

1. Clone this GitHub repository to your local machine:

```bash
git clone https://github.com/khaireddine-arbouch/AirBnB_clone.git
```

2. Navigate to the project directory:

```bash
cd AirBnB_clone
```

3. Execute the console:

```bash
./console.py
```

### Execution Examples

#### Interactive Mode

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

#### Non-Interactive Mode

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

## 4. Usage

Here are some usage examples:

- Start the console in interactive mode:

```bash
$ python console.py
(hbnb)
```

- Use `help` to see the available commands:

```bash
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  all  count  create  destroy  help  quit  show  update

(hbnb)
```

- Quit the console:

```bash
(hbnb) quit
$
```

- Create:

```bash
(hbnb) create BaseModel
57262839-51d7-4a9a-93e2-35ed8e91d823
$
```

- Show:

```bash
(hbnb) show BaseModel 57262839-51d7-4a9a-93e2-35ed8e91d823
[BaseModel] (57262839-51d7-4a9a-93e2-35ed8e91d823) {'id': '57262839-51d7-4a9a-93e2-35ed8e91d823', 'created_at': datetime.datetime(2023, 8, 13, 14, 19, 19, 412265), 'updated_at': datetime.datetime(2023, 8, 13, 14, 19, 19, 412357)}
(hbnb)
```

- All:

```bash
(hbnb) all
[BaseModel] (57262839-51d7-4a9a-93e2-35ed8e91d823) {'id': '57262839-51d7-4a9a-93e2-35ed8e91d823', 'created_at': datetime.datetime(2023, 8, 13, 14, 19, 19, 412265), 'updated_at': datetime.datetime(2023, 8, 13, 14, 19, 19, 412357)}
(hbnb) all BaseModel
[BaseModel] (57262839-51d7-4a9a-93e2-35ed8e91d823) {'id': '57262839-51d7-4a9a-93e2-35ed8e91d823', 'created_at': datetime.datetime(2023, 8, 13, 14, 19, 19, 412265), 'updated_at': datetime.datetime(2023, 8, 13, 14, 19, 19, 412357)}
```

- Destroy:

```bash
(hbnb) destroy BaseModel 57262839-51d7-4a9a-93e2-35ed8e91d823
(hbnb) all
[]
```

- Count:

```bash
(hbnb) create User
(hbnb) create User
(hbnb) create User
(hbnb) count User
3
```

## 5. Testing

For testing, the project uses:

- `unittest` module
- File extension: `.py`
- Naming convention: files and folders start with `test_`
- Organizational structure: unit tests for `models/base.py` are in `tests/test_models/test_base.py`
- Execution command: `python3 -m unittest discover tests`

### Running Tests (Interactive Mode)

```bash
echo "python3 -m unittest discover tests" | bash
```

### Running Tests (Non-Interactive Mode)

To run tests in non-interactive mode and discover all tests:

```bash
python3 -m unittest discover tests
```

## 6. Authors

- [Khaireddine Arbouch](https://github.com/khaireddine-arbouch/)

## 7. License

This project is licensed under the MIT License

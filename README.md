
### install upgraded version of pip in your desktop 
Windows
```
py -m pip install --upgrade pip
```

Linux/MAC OS
```
python3 -m pip install --upgrade pip
```

## Create a project with the following structure

```
packaging_tutorial/
├── LICENSE
├── pyproject.toml
├── README.md
├── src/
│   └── example_package_YOUR_USERNAME_HERE/
│       ├── __init__.py
│       └── example.py
└── tests/
```

```

touch LICENSE
touch pyproject.toml
touch setup.cfg
mkdir src/example_package_YOUR_USERNAME_HERE
touch src/example_package_YOUR_USERNAME_HERE/__init__.py
touch src/example_package_YOUR_USERNAME_HERE/main.py
mkdir tests
```

## pyproject.toml 

``pyproject.toml`` tells “frontend” build tools like pip and build what “backend” tool to use to create distribution packages for your project. You can choose from a number of backends; this tutorial uses Hatchling by default, but it will work identically with setuptools, Flit, PDM, and others that support the [project] table for metadata.
<br>Open ``pyproject.toml`` and enter this ``[build-system]`` tables:

```
[build-system]
requires = [
    "setuptools>=61.0",
    "wheel"
]
build-backend = "setuptools.build_meta"
```

# Setup.cfg setup
Using setup.cfg is a best practice, but you could have a dynamic setup file using setup.py

```
[metadata]
name = Your Pkage Name
version = Your Pkage Name
author = Author Name
author_email = email
description = description
long_description = file: README.md
long_description_content_type = text/markdown
url = https://github.com/pypa/sampleproject
project_urls =
    Bug Tracker = https://github.com/pypa/sampleproject/issues
classifiers =
    Programming Language :: Python :: 3
    License :: OSI Approved :: MIT License
    Operating System :: OS Independent
[options]
package_dir =
    = src
packages = find:
python_requires = >=3.6
[options.packages.find]
where = src

```
## Running the build
### install upgraded version of pip in your desktop
Windows
```
py -m pip install --upgrade build
```
Linux/MAC OS
```
python3 -m pip install --upgrade build
```


### Create the build
```
py -m build
```













### References
https://packaging.python.org/tutorials/packaging-projects/

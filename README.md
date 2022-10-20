
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

## Setup.cfg setup
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

## Create Licence
```
Copyright (c) 2018 The Python Packaging Authority

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

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
Windows
```
py -m build
```
Linux/mac
```
python3 -m build
```


## Uploading the distribution archives

Finally, it’s time to upload your package to the Python Package Index!

The first thing you’ll need to do is register an account on TestPyPI, which is a separate instance of the package index intended for testing and experimentation. It’s great for things like this tutorial where we don’t necessarily want to upload to the real index. To register an account, go to <a href="https://test.pypi.org/account/register/">PyPi</a> and complete the steps on that page. You will also need to verify your email address before you’re able to upload any packages. For more details, see Using TestPyPI.

To securely upload your project, you’ll need a PyPI API token. Create one at <a href="https://test.pypi.org/manage/account/#api-tokens">PyPi token</a>, setting the “Scope” to “Entire account”. Don’t close the page until you have copied and saved the token — you won’t see that token again.

Now that you are registered, you can use twine to upload the distribution packages. You’ll need to install Twine:

### install upgraded version of pip in your desktop
Windows
```
py -m pip install --upgrade twine
```
Linux/Mac
```
python3 -m pip install --upgrade twine
```

#### Then upload your project ``PyPi``
Windows
```
py -m twine upload dist/*
```
Linux/Mac
```
python3 -m twine upload dist/*
```












``References``
<br>

<a href="https://packaging.python.org/tutorials/packaging-projects/" > PyPi Upload </a>

`` 📡 Get in Touch `` 
<br>

<a href="https://www.facebook.com/Aru.Ofc" target="_blank"><img src="https://img.shields.io/badge/FACEBOOK-4267B2.svg?&style=flat-square&logo=facebook&logoColor=white" alt="LinkedIn"></a>
<a href="https://www.instagram.com/Aru.Ofc.Ins" target="_blank"><img src="https://img.shields.io/badge/Instagram-%23E4405F.svg?&style=flat-square&logo=instagram&logoColor=white" alt="Instagram"></a>
<a href="https://twitter.com/aru_ofc_twiter" target="_blank"><img src="https://img.shields.io/badge/Twitter-%231DA1F2.svg?&style=flat-square&logo=twitter&logoColor=white" alt="Twitter"></a>
<a href="https://open.spotify.com/user/rwvotqr02yuzpyfmkkri3b5k1?si=X4sohjMTTCmIMuniDJ5ECA&utm_source=copy-link" target="_blank"><img src="https://img.shields.io/badge/Spotify-%231ED760.svg?&style=flat-square&logo=spotify&logoColor=white" alt="Spotify"></a>
<a href="https://www.youtube.com/c/ARULyrics1" target="_blank"><img src="https://img.shields.io/badge/YouTube-FF0000.svg?&style=flat-square&logo=youtube&logoColor=white" alt="YouTube"></a>
<a href="https://dev.to/aruofc" target="_blank"><img src="https://img.shields.io/badge/DEV-%230A0A0A.svg?&style=flat-square&logo=DEV.to&logoColor=white" alt="DEV.to"></a>
<a href="mailto: arifulislam275m.com" target="_blank"><img src="https://img.shields.io/badge/Email-BB001B.svg?&style=flat-square&logo=gmail&logoColor=white" alt="Gmail"></a>
<a href="https://github.com/Aru-Ofc-git" target="_blank"><img src="https://img.shields.io/badge/GitHub-171515.svg?&style=flat-square&logo=github&logoColor=white" alt="Github"></a>

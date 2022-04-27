# OSP-week7-Homework
### Author : 2017113812 Suhyung kwon
---

## Version
Python 3.9.7

---

## Install
``` shell
#install venv in your local directory
$ python -m venv [your_virtual_environment]     
$ source [your_virtual_envirnoment]/bin/activate 

#install requirements with pip
$ pip install -r requirements.txt     

#execute code
$ python github-api-test.py
```

---

## Usage
### github-api-test.py
``` python
import pprint 
import requests

r = requests.get('https://api.github.com/users/Ospac')
if r.status_code == 200: 
    json_data = r.json()
pprint.pprint(json_data)
```
- send http requests to my github page([https://api.github.com/users/Ospac](https://api.github.com/users/Ospac))
- check response status code and assign json data to `json_data`
- print `json_data` as clean form with pprint module

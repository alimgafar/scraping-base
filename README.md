# General Scraping Base Environment

## Python requirements

This environment assumes you're running pip3 and python 3.7.7. Here are the steps to follow to set up your libraries.

1. `git clone <this repo> <your new project dir>`
2. `cd <your new project dir`
3. `python3 -m venv env`
4. `source env/bin/activate`
5. `pip install -r requirements.txt`
6. Do stuff. I usually install jupyter notebooks here (`pip install jupyter`), but I don't save it to my requirements file. 
7. Don't forget to save your work to git as you go: `(git add . && git commit -m"<change description>)"` <-- note the commands execute in a subprocess when wrapped with parens
8. Once done, remove jupyter notebooks (`pip uninstall jupyter`).
9. Generate a new *requireents.txt* file: `pip freeze > requirements.txt`
10. Commit new change to git and sync with remote: `(git add . && git commit -m"Regenerated requirements.txt with current dependencies" && git push -u origin master)`
11. Cleanup. Type `deactivate` at the command prompt. 


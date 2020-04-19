# General Scraping Base Environment

## Python requirements

This environment assumes you're running pip3 and python 3.7.7. 

You will also need the Chrome Driver if it isn't already there. Check by typing `chromedriver --version` at a terminal prompt. If no response, install it with Homebrew by typing `brew cask install chromedriver` at a terminal prompt. This will allow selenium to control Chrome. On MacOS, `safaridriver` is installed by default with Safari. You can check on it by typing `safaridriver --version` at a terminal prompt. To enable control of Firefox, install the Gecko driver with Homebrew. Type `brew install geckodriver` at a terminal prompt. 

Here are the steps to follow to set up your libraries.

1. `git clone <this repo> <your new project dir>`
2. `cd <your new project dir`
3. `python3 -m venv env`
4. Create a new EMPTY repository for your project on Github (or Gitlab or Bitbucket or wherever your remote server is). Set to public or private as needed.
5. Copy the URL for this new repository.
6. Back in your project directory, `git remote add origin <new repository URL>`
7. `git push -u origin master`
8. `source env/bin/activate`
9. `pip install -r requirements.txt`
10. Do stuff. I usually install jupyter notebooks here (`pip install jupyter`), but I don't save it to my requirements file. 
11. Don't forget to save your work to git as you go: `(git add . && git commit -m"<change description>)"` <-- note the commands execute in a subprocess when wrapped with parens
12. Once done, remove jupyter notebooks (`pip uninstall jupyter`).
13. Generate a new *requireents.txt* file: `pip freeze > requirements.txt`
14. Commit new change to git and sync with remote: `(git add . && git commit -m"Regenerated requirements.txt with and changed workbook files" && git push -u origin master)`
15. Cleanup. Type `deactivate` at the command prompt.
16. Optionally, cd out of the project directory and delete it entirely. When you want to work again, simply clone the project repo, and repeat from step 2.


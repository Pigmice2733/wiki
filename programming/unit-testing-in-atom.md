# Unit Testing in Atom

Once we have written unit tests, you need to be able to run them and check your own code.
Before we start, make sure you have the Atom editor, Python 3, and a GitHub repository already installed in atom.
To check what version of python you are running type 
```
python3 --version
```
into the terminal (Powershell on Windows). If you have Python 3 or later installed this should print out a version number starting with 3, such as `3.6.3`.

Next open up the Command Pallete by pressing <kbd>Command</kbd><kbd>Shift</kbd><kbd>P</kbd> (on macs) or <kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>P</kbd> (on Windows). Search for "Install Packages," and then install `atom-python-test` and `atom-python-virtualenv`.

Next, we need to install a virtual enviroment on our machine so that the libraries and python version we have running on this current project won't interfere with our other projects. We can quickly install this using the terminal. 
Run: 
```
pip3 install pipenv
```
`pip3` is a command to install Python3 packages through the terminal rather than going to a website, for example. Use the command `cd` (change directory) and type the location of wherever you have the respository stored, ex. 
```
`cd /Users/bob/github/pybasictraining`
```
Then use the command 
```
pipenv install pytest
```

We need to turn this on in Atom, so go back to the settings page in Atom and go to the packages subbar. Find the 
```
atom-python-virtualenv
```
package and under its settings, uncheck the first box. Type in the `virtualenv` location, then go under **> Packages > Virtualenv > Select**

You are now done with your installation!

Once you have your tests written, you can right click on the contents of the test file and click **Py.test** > **Run all tests**
![right click on your code to run a test](/images/path-to-image.png)

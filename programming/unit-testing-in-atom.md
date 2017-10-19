# Unit Testing in Atom

Once we have written unit tests, you need to be able to run them and check your own code.
Before we start, make sure you have the Atom editor, *python 3*, and a github respository already installed in atom.
To check what version of python you are running type
*python3 --version* into terminal (mac) or powershell (windows), if it returns something greater than 3 you have the newest version.

Atom has a quick search feature that can be accessed with the keyshortcut shift+command+P (for macs) or shift+ctrl+P (in windows) or you can manually go to > Packages > Command Palette >Toggle.
Search for *settings* and then the *install* subbar. You will need to install the two following atom packages:
atom-python-test (from pghilardi)
atom-python-virtualenv (also from pghilardi)

Next, we need to install a virtual enviroment on our machine so that the libraries and python version we have running on this current project won't interfer with our other projects.
We can quickly install this in terminal (mac) or powershell (windows). Type:
*pip3 install pipenv*
  pip3 is a command to install packages through the terminal rather than going to a website, for example.
Use the command *cd* (change directory) and type the location of wherever you have the respository stored:
  ex. cd /Users/bob/github/pybasictraining
Then within that folder use the command
*pipenv install pytest*

We need to turn this on in atom, you back to the settings page in atom and go to the packages subbar.
Find the atom-python-virtualenv package and under it's settings, unclick the first box.
Type in the virtualenv location.
Then go under >Packages >Virtualenv > Select

You are now done with your installation!

Wherever you have your tests written, with pytest we can now right click on that file
> pytest
And then click on run all tests




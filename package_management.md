Packages
========
Writing code is great, but you don't want to write everything from scratch! How
do you get sets of code (libraries) written by other people? With a package
manager! The package manager for python is called `pip`. Want to see what
python packages are installed on your computer? Try this:
```
pip freeze
```
You'll get back a list of the packages and their versions. It might look
something like this.
```
Jinja2==2.7.2
MarkupSafe==0.21
Werkzeug==0.9.4
backports.ssl-match-hostname==3.4.0.2
gnureadline==6.3.3
ipython==2.0.0
pyzmq==14.2.0
tornado==3.2
wsgiref==0.1.2
```

The central location that pip searches for packages is the
[Python Package Index](https://pypi.python.org/pypi) (pypi). You can also
install from any location that puts the source code on the internet.
```
# Installs ipython from github
pip install git+https://github.com/ipython/ipython@rel-2.0.0

# Installs ipython from pypi
pip install ipython==2.0.0
```
**Note:** You'll see that the github version has 'rel-2.0.0' instead of '2.0.0'.
This is because the iPython team has made a 
[git tag called 'rel-2.0.0'](https://github.com/ipython/ipython/tree/rel-2.0.0) 
for the 2.0.0 version.


Virtualenv
----------
Sometimes you want a different version of a library then you have installed on
your system environment. For example, we have a project that needs
`ipython==1.2.0`, but our system has `ipython==2.0.0` installed. What do we do?
We use Virtualenv. Virtualenv creates a "virtual environment," a kind of sandbox
for packages.


1. Install [Homebrew](http://brew.sh/) - scroll to the bottom of the page and
follow the instructions
2. Install virtualenv. (Open the terminal and enter the following command. You
may have to enter your password)

    ```
    sudo pip install virtualenv virtualenvwrapper
    ```
    You have just installed a python package into your system!
3. **Magic**. Run these commands in your terminal.
    
    ```
    mkdir ~/.venv;
    echo "export WORKON_HOME=~/.venv" | tee -a ~/.bashrc;
    echo "source /usr/local/bin/virtualenvwrapper.sh" | tee -a ~/.bashrc;
    ```
    You have modified what your terminal runs whenever you open the Terminal!
    Close this Terminal window and open a new one ( + w,  + n)
4. Create a new virtual environment.
    
    ```
    mkvirtualenv setup-env
    ```
    You have now made a new virtual environment! If you ever want to use this
    environment again, simply run `workon setup-env` in your terminal.
5. You can now install any python package into this environment. Try installing
    ipython.

    ```
    pip install ipython 
    # No sudo necessary
    ```
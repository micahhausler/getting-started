Python Setup - Mac
==================

Windows
-------
I'm assuming you have a Mac. Sorry.

Linux 
-----
You're probably ahead of the game. I will fill this out later.


--------------------------------------------------------------------------------
[iPython](http://ipython.org/notebook.html)
===========================================
iPython is a powerful interactive tool to run and code in python

Setup
-----
1. Open the terminal and enter the following commands. (You may have to enter
    your password)

    ```
    sudo pip install ipython jinja2 werkzeug pyzmq tornado
    ```
    You have just installed several package into your system! 
2. Open the notebook server
    
    ```
    ipython notebook
    ```
    This should open your webbrowser to http://127.0.0.1:8888
3. Open a new notebook. Click the 'New Notebook' button on the right. You can
    now run python code in your web browser!


--------------------------------------------------------------------------------

Virtualenv
==========



1. Install [Homebrew](http://brew.sh/) - scroll to the bottom of the page and
follow the instructions
2. Install virtualenv. (Open the terminal and enter the following command. You
may have to enter your password)

    ```
    sudo pip install virtualenv virtualenvwrapper
    ```
    You have just installed a python package into your system! This package lets
    you create virtual sandboxes for python environments.
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

5. Make a code folder. 
    ```
    mkdir code
    ```
    You have just made a "code" folder in your home directory! Next try this.
    ```
    open .
    ```
    Your finder will open in the directory you just made.

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
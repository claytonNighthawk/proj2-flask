# proj2-flask
A starter project for using the Flask framework

## Basics 
* Enhances a class schedule .txt file
  * The starting date of each week should be displayed
  * As well as highlighting of the week. 

### What do I need?  Where will it work? ###

* Designed for Unix, mostly interoperable on Linux (Ubuntu) or MacOS.
  Target environment is Raspberry Pi. 
  ** May also work on Windows (at least the W10 Ubuntu bash) or a Linux virtual machine
   out of the box depending on your pyvenv package command name. Program might require manual configuration with `. env/bin/activate`, `make configure` and `pip install -r requirements.txt` or changing the PYVENV command name in templates.d/Makefile.standard between pyvenv and virtualenv. I could not get "pyvenv" to install on my pi or anywhere else but virtualenv worked everywhere.    
   
* You will also need Python version 3.4 or higher. 
* Designed to work in "user mode" (unprivileged), therefore using a port 
  number above 1000 (rather than port 80 that a privileged web server would use)

## In your workspace

`bash ./configure` should create appropriate configuration files on
most Unix files.   If you are using Windows, some additional editing
of configuration files may be necessary (similar to what was mentioned above).  You might have to edit the
Makefile to find the right version of 
pyvenv.

If you can run flask applications in your development environment, the
application would might be run by
`   python3 flask_syllabus.py` or `make run`
and then reached with url
`   http://localhost:5000`

`make run` will launch the debugging server built into flask.  It
provides the best support for tracking down bugs in your server, but
it's not suitable for use by many users or over a long period.  `make
service` starts a Green Unicorn (gunicorn) server; you may note the extra
lime sparkles all around you.  Green Unicorn can be used for servers
that run over a longer period (e.g., if you want to leave a web
service running on your Pi).   


### Author: Clayton Kilmer, kilmer@cs.uoregon.edu ###


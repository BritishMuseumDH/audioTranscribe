Audio transcription from the British Museum Soundcloud archive
==============================================================

An application for transcription of Soundcloud audio.

This application has four files:

* template.html: the view for every task and deal with the data of the answers.
* tutorial.html: a simple tutorial for the volunteers.
* project.json: the setup metadata (make sure name and short name are unique, or create will fail.)
* long_description.md: the long description for the app.


Creating the application
=======================

You need to use the PBS command line interface for creating and updating the project.

*  Create an account in PyBossa
*  Copy from your account profile your API-KEY
*  Navigate to your home directory and create a file called .pybossa.cfg
*  Within this file add following lines:
```bash
   [default]
   server: http://crowdsourced.micropasts.org
   apikey: API-KEY
```
*  Now clone the code to your server and change directory into the folder:
```bash
   $ git clone https://github.com/MicroPasts/montpelierVirginia.git applicationName
   $ cd applicationName
```
*  Now run:
```bash
   $ pbs create_project
```
*  This should have created the project.
*  If the long description has not appeared, then run the update project command as shown below

Documentation
=============

We recommend that you read the section: [Build with PyBossa](http://docs.pybossa.com/en/latest/build_with_pybossa.html) 
and follow the [step by step tutorial](http://docs.pybossa.com/en/latest/user/tutorial.html).


Updating template
=================

After making changes to your source code and committing to github do the following:

*  Clone or pull changes from repo to your server and then issue this command:

```bash
    $ pbs update_project
```

*  Template should update


Adding tasks to project
=======================

Import the file names via the CSV importer.

Change redundancy of tasks
==========================

To update all of them:

```bash
    $ pbs update-task-redundancy --redundancy 3
```

LICENSE
=======

Please, see the COPYING file.

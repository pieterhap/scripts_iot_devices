# Scripts for IoT Devices
by Pieter Hap

The scripts first need to be made executable before they can be used.
This can easily be done with the following commands:

> chmod u+x clone_repository
> chmod u+x copy_folder
> chmod u+x ssh_setup

Then you can execute the scipts by adding ./ in front of the filenames in the commandline.

With the first script you can clone or pull git repositories from Github.
All you need to do is enter the URL of said repository and the script does the rest.
The script checks if the repository already exists. If it doesn't exist yet, it will clone the repository. If it does exist it will only do a pull.

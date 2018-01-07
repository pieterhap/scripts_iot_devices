# Scripts for IoT Devices
by Pieter Hap

The scripts first need to be made executable before they can be used.
This can easily be done with the following commands:

> chmod u+x clone_repository

> chmod u+x copy_folder

> chmod u+x ssh_setup

Then you can execute the scipts by adding ./ in front of the filenames in the commandline.

## clone_repository

With the first script you can clone or pull git repositories from Github.
All you need to do is enter the URL of said repository and the script does the rest. 

The script checks if the repository already exists. If it doesn't exist yet, it will clone the repository. If it does exist it will only do a pull.

## copy_folder

The second script can be used to copy folders. You can choose to copy them to a remote host or to another location on the local host. 

You need to enter the absolute path of the folder you want to copy (use pwd), the username and the ip address of the remote host (if you're using one) and the absolute path of the destination you want to copy the folder to (again use pwd).

## ssh_setup

This script setups the SSH keys on the pi and also creates keys for the current user. You only have to enter the username and the ip address of the remote host. 

since ssh is being used in this folder, you will be asked several times to enter the password of the remote host.



# remotefoldersync
One-way syncronization of a local folder to a remote folder via SSH/FTP

## Description:

This very simple command-line program monitors a local folder and automatically pushes any changed files to a remote folder. It provides an easy way to keep a remote folder sync'd with a local one.

This is mainly useful for development where you would like to modify files "live" on a remote folder, but cannot mount the remote folder as a filesystem. This way you can simply modify files in your local copy, and they are automatically pushed to the remote folder.

There are tons of free/open source similar utilities. This one is written in python, is very simplistic, and work with SSH/FTP.

## Usage:

```
remotefoldersync.py [--ftp] -u [username] -p [password] -h [hostname] [-P port] [local_folder] [remote_folder]

--ftp - specify the server as FTP instead of SSH. -u [username] - optional, the username. -p [password] - optional, the password.

-h [hostname] - optional, the hostname. [local_folder] - the local folder to monitor for changes. [remote_folder] - the remote folder that mirros the local_folder. NOTE: You cannot currently use the ~ symbol. Just use a relative path like "path/to/folder" or an absolute path like "/path/to/folder".
```

## Requirements:

- Python
- Paramiko Python library
- colorama (Suggested, but can be easily turned off by simply modifying the header of the main python file)

## Feedback:

Feel free to add any bugs / feature requests to the "Issues" tab on top. Forums & google group will come later if necessary.

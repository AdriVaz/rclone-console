# Rclone Console

Rclone-Console is a Python wrapper around rclone that allows the user to interact with his/her configured rclone targets using a shell-style interface.

It was inspired by the sftp shell, but implemented with some limitations.

This program was designed to interact with Google Drive, and implements the `shared` and `local` commands (see below).

Some operations are not fully tested and may fail, use it at your own risk

## Available commands

Here is a list of the commands implemented in the shell:

- `shared`: changes the scope to local files in your Google Drive storage
- `local`: changes the scope to the files that have been shared with you in Google Drive
- `ls`: list contents of a remote path
- `cd`: change directory in the remote path
- `get`: download the selected files or directories from the local share into your machine
- `rm`: deletes a file or directory from your remote folder
- `put`: upload a file or directory, from your local machine to your remote storage
- `lls`: list the local files on your machine
- `lcd`: change directory in your local machine

## Google Drive shared files

The commands `shared` and `local` control wether you list the files in your Google drive storage, or the files that have been shared with you. This functionality is built around the rclone option `--drive-shared-with-me`

## Missing features

Here are some of the most noticeable missing features:
- Tab autocompletion
- Coloring of local directories when using the `lls` command

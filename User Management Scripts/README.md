# Bash Scripts for User Management

This repository contains three Bash scripts designed to facilitate user management on Linux systems. These scripts allow you to create users, generate random passwords, and delete or archive user accounts.

## Scripts Overview

## 1. user_creation.sh

This script creates a new user on the local system. It requires superuser privileges and generates a secure random password for the new user.

### Features:

- Creates a user with a username and optional comment.
- Automatically generates a random password.
- Forces the user to change the password on their first login.
- Displays the username, password, and hostname.

Usage:

`sudo ./user_creation.sh USER_NAME [COMMENT]`

Example:

`sudo ./user_creation.sh john_doe "John Doe Account"`

## 2. random_password_generator.sh

This script generates a random password with options for length, special characters, and verbosity.

### Features:

- Specify password length using -l.
- Append a special character to the password using -s.
- Enable verbose mode using -v.

Usage:

`./random_password_generator.sh [-vs] [-l LENGTH]`

Example:

`./random_password_generator.sh -l 16 -s -v`

## 3. delete_user.sh

This script disables, deletes, and/or archives user accounts. It requires superuser privileges.

### Features:

- Disable user accounts.
- Delete user accounts with or without their home directory.
- Archive user home directories before deletion.

Usage:

`sudo ./delete_user.sh [-dra] USER [USERN...]`

Options:

```
-d : Delete the user account.
-r : Remove the home directory.
-a : Archive the user's home directory.
```

Example:

`sudo ./delete_user.sh -dra john_doe`

Prerequisites

- Linux operating system.
- Superuser (root) privileges to execute the scripts.

Notes

Make sure the scripts are executable. Use the following command if needed:

`chmod +x script_name.sh`

The scripts are written for systems using bash. Ensure you have bash installed and set as your shell.

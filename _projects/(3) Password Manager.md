---
name: Password Manager
tools: [Python, SQL]
image: ../assets/images/PasswordManager/CLI_interface.png
description: Built a command line password manager in Python with a SQL database for storage and a customizable password generator.
---
# Password Manager

## Situation
For my final project in AP Computer Science Principles, I was asked to design and build a program of my own choosing. The assignment was open ended, so the first decision was picking something with enough scope to show real work while still being something I could finish within the time I had.

## Task
I decided to build a password manager. Before writing any code I set out the feature list the program had to cover. It needed to create new logins, generate passwords, let the user customize how those passwords were generated, store logins and passwords so they survived between sessions, retrieve them, and delete them.

## Action
I wrote the application in Python and used SQL for storage. Python handled the program logic, the command line interface, and the password generator. The database held the stored account logins and passwords.

Splitting the work that way was the main design decision in the project. Storing records in a database rather than a plain text file meant the data persisted after the program closed, and it meant I could query for one specific account instead of loading the entire file into memory and rewriting all of it every time a single entry changed. Deleting one login became a single statement rather than a rebuild of the whole file.

The generator produced passwords based on settings the user chose rather than one fixed format. The user set the length and decided whether to include symbols and numbers, which meant a generated password could be matched to whatever character requirements the site being signed up for imposed. The program also suggested a recommended length rather than leaving that choice entirely up to the user.

## Result
The finished program worked as intended and met every goal I set at the start. Every feature on my original list made it into the final version, which was the outcome I was graded on.

The interface is command line only. That was enough for the class, since the project was assessed on the program logic rather than on presentation, but it is the piece the project would need before I would use it day to day. Adding a front end is the change I would make if I revisit it.

<img src="../assets/images/PasswordManager/PasswordManagerDemonstration.gif" alt="Password Manager Demonstration GIF" width=400>
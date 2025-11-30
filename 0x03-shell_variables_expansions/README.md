-alias
Description

This script creates a Bash alias named ls that is set to rm *.
After sourcing this file, running ls in the terminal will execute rm * instead of listing files.

Warning: This is dangerous if used in real directories—it will delete all files in the current directory. Use only in a controlled environment for learning purposes.

Usage

Navigate to the directory containing 0-alias.

Source the script in your shell:

source ./0-alias


Now, running:

ls


will execute rm *.
To bypass the alias and list files, use:

\ls

Example
julien@ubuntu:/tmp/0x03$ ls
0-alias  file1  file2
julien@ubuntu:/tmp/0x03$ source ./0-alias
julien@ubuntu:/tmp/0x03$ ls
julien@ubuntu:/tmp/0x03$ \ls
0-alias

Notes

The alias only affects the current shell session.

To remove the alias, you can run:

unalias ls

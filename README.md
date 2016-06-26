#How to install.

1. Put _sshpass script in any directory included in $PATH.*
2. Change the permission to execute.
* You can change the name if you want.


#Usage (shown by "_sshpass --help" command.)

Usage: _sshpass [options]
Options(needed):
  -p, --pass        Set password for the scp command.
  --scp             Define scp command options as double-quoted argument.

Options:
  --expect          Expected string to input the password. "password:" as default.
  --timeout         Set timeout (5sec as default) for waiting the expected message.
  -h, --help        Print this message end exit.

Example: _sshpass -p zzzzzz --scp "-P 22 ./file.txt user@example.com:/home/user"


#Output.
$_sshpass -p zzzzzz --scp "./test.zip  example.com:/tmp"
spawn env LANG=C scp ./test.zip example.com:/tmp
user@example.com's password:
test.zip                                                                   100%  124MB 123.5MB/s   00:01

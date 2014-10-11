ksh-template
============

This is a simple korn shell template with logging machanism and builtin logrotation. All commands 
that are defined between CMD_START and CMD_END, will be checked in two ways. First it will verify,
that the command exists and it is executable. Second it also checks the body if all CMD_* variables
are defined.

This script comes with a config file, which is found in the etc folder. This config file is soured
and not parsed, so you have to take care who has write permission to this file, since all code that
is in this file gets executed.

This script takes care of the Unix "standard" directory structure. That means that you have to put
it in a bin directory. It will find its config file in ../etc and create a logfile in ../var/log. If 
the ../var/log folder does not exist, it will create it.

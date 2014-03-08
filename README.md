codeswarm
=========

Simple tool to convert the log formats of various repositories to
a standard input format in JSON.

To convert an SVN log to the standard format:

1. Run this command in the SVN repository checkout
> svn log -v > my_svn.log

2. Convert the log to our event-based JSON format:
> python convert_logs.py -s path/to/my_svn.log -o svn_log.json

More usage detailed instructions to come.

Special notes:

git logs must be prepared in this fashion:

> git-log --name-status --pretty=format:'%n------------------------------------------------------------------------%nr%h
| %ae | %ai (%aD) | x lines%nChanged paths:' > activity.log

Starteam logs must be prepared in this fashion:

> stcmd.exe hist -p <url> -nologo -is > activity.log




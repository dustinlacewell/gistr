
gistr
-----

    usage: gist [-h] [-p] [-t TOKEN] [-u USER] [files [files ...]]
    
    Commandline gist utility
    
    positional arguments:
      files
    
    optional arguments:
      -h, --help            show this help message and exit
      -p, --public          Marks the gist as publically viewable
      -t TOKEN, --token TOKEN
                            Specifies a file containing user OAuth token.
      -u USER, --user USER  Specifies a user to associate the gist with.


This is just a small utility for interacting with Github's Gist service from the commandline. 
It will either take a list of filenames or it will read from stdin. If you specify a username
it will prompt you for a password and attempt to retrieve an authorization token from Github.

If successful, it will save the token to `~/.gistr` or the file specified with -t/--token so
that subsequent usages will not require asking for a password.

After posting the Gist it will print out the URL and copy the url to your clipboard.


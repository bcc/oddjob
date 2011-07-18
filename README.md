# OddJob #

A simple tool for tracking time.

Like many unix admins, I always have terminals open. Other time tracking tools carry a lot of overhead, and I only wanted to quickly estimate how much time the unexpected non-project time takes. OddJob should allow me to log these without too much overhead. 

OddJob stores its data in a text file called .oddjob, kept in your home directory, 1 line per entry. 

OddJob requires perl5, but should work with any reasonably current version. It doesn't need any unusual modules. Works fine on Linux, Solaris and OS X. Not tested on Windows.

## Usage ##

    Usage:
      oj add <time> <category> <description>
      oj list [string]
      oj list [-lines]
      oj edit <id> (date|time|cat|desc)=<new value>

To add a new entry:

    oj add 1h code First effort at oddjob

    oj list
    0	2011-07-18	1h	code	First effort at oddjob

Editing:

    oj edit 0 time=2h

Multiple categories:

    oj edit 0 cat=code,git

    oj list
    0	2011-07-18	2h	code,git	First effort at oddjob


It is also possible to limit the list to the final entries:

    oj list -10

You can also search by passing any other text:

    oj list effort

## TODO ##

Summary/stats scripts.

## License ##

OddJob is released under the GPLv2 license. See the COPYING file for
details.

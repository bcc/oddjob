# OddJob #

A simple tool for tracking time

OddJob stores its data in a text file called '.oddjob', 1 line per entry. 

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

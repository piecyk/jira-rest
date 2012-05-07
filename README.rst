============
jira-rest.el
============

An Emacs major mode for interfacing with JIRA's REST API
========================================================

This project is the result of seeing the state of the original `jira.el <http://emacswiki.org/emacs/jira.el>`_. Atlassian's JIRA API docs `state quite clearly <https://developer.atlassian.com/display/JIRADEV/JIRA+Remote+API+Reference>`_ that the REST API unveiled for JIRA 5.0 is the only version that will be receiving development efforts going forward. Unfortunately, ``jira.el`` uses the XML RPC. So in the interest of scratching my own itch I started work on this.


To Install & Run
----------------

1. Place this file somewhere on your load-path
2. Add ``(require 'jira-rest)`` to your .emacs/init.el file.
3. ``M-x jira-rest-mode``


To Do's
-------

High-priority tasks:
~~~~~~~~~~~~~~~~~~~~

* Add automated tests with ERT
* Implement issue search
* Adding/removing/editing comments

Obviously implementing functions to consume every possible API endpoint is a to-do, but priority will likely go to those that get the most use.


Caveats
-------

The capabilities of this mode are limited by what is exposed by JIRA's API. Some notable deficiencies include **changing issue status** and **resolving/closing issues**. These deficiencies overlap with the XML RPC API, unfortunately. The hope is, however, that these holes will be plugged since this API will be getting future development.


Contributing
------------

If you would like to contribute, please submit pull requests with your changes/additions. As APIs are prone to undocumented changes and breakage, any new code will require test coverage. (This includes myself. I'll be retrofitting the original code soon.)




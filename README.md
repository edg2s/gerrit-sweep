gerrit-sweep
============

Script to delete branches which have been merged in gerrit, even if you don't have the latest patchset

The script will find the latest "Change-Id" in each branch and see if it appears in master. If it does the branch is force-deleted.

Branches whose change is abandoned in Gerrit are also deleted. The status of each kept branch is shown.

Options
-------

* `--keep-abandoned`: do not delete branches with abandoned changes.

Requirements
------------

[jq](https://jqlang.org/) is needed to read the Gerrit API response.

gerrit-sweep
============

Script to delete branches which have been merged in gerrit, even if you don't have the latest patchset

The script will find the latest "Change-Id" in each branch and see if it appears in master. If it does the branch is force-deleted.

Requirements
------------

The `--status` and `--delete-abandoned` flags need [jq](https://jqlang.org/) to read the Gerrit API response.

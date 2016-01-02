# INTRODUCTION #

Taurus is a blatently simple backupscript using tar.
I'm using it on my own linux datastorage machine.

Taurus copies only the updated files from a given sourcedir
to a backup 'repository' dir, excluding some optional exclude
patterns, using a tar pipe with a 'level 1' snapshot
as described here:
http://www.gnu.org/software/tar/manual/html_node/Incremental-Dumps.html

It does not store a tar file; the 'repository' is a
mirror of the source. By default, Taurus uses numbered
backups for changed files in the repository.

# INSTALLATION #

**requirements**: tar

  * download the tarball
  * cp -a ./usr/local/bin/taurus  /usr/local/bin
  * cp -a ./usr/local/share/taurus  /usr/local/share
  * fix permissions ...
  * enjoy

# USAGE #

Usage: `taurus -chprtuv (reposdir) [sourcepath]`

**Create a repository**:
`taurus -c | --create (reposdir) [sourcedir]`

**Update a repository**:
`taurus -u | --update (reposdir)`

**Restore files from a repository**:
`taurus -r | --restore (reposdir) (restorepath)`

**Purge a repository**:
`taurus -p | --purge (reposdir) `

**Test an update**:
`taurus -t | --test-update (reposdir)`

**Help**:
`taurus -h | --help`

**Version**:
`taurus -v | --version`
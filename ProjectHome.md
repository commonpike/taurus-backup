# Taurus - simple linux backup using tar pipes #

Example:
```
> taurus --create /mnt/backup/frank /home/frank ## create a repository
> taurus --update /mnt/backup/frank ## copy over new or modified files. backup old stuff.
> taurus --restore /mnt/backup/frank /home/frank/important ## restore lost files
```

Taurus copies only the updated files from a given sourcedir
to a backup 'repository' dir, excluding some optional exclude
patterns, using a tar pipe with a 'level 1' snapshot
as described here:
http://www.gnu.org/software/tar/manual/html_node/Incremental-Dumps.html

and http://blog.extracheese.org/2010/05/the-tar-pipe.html

It does not store a tar file; instead, it creates a 'repository dir' which contains a
plain mirror of the source dir. Using tar pipes allows us to
  * operate only on new or changed files (so it's fast)
  * maintain numbered backups of changed files (configurable)

On the down side, ofcourse,
  * taurus tars and untars files at the same time (so it's slow)
  * backup depends on the correct timestamps of files

If you're interested, the best place to start is the UseCaseScenario.





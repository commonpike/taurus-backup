# Bugs/Feature requests/Todo #

Version is 0.5.

I'm the only person in the world using it. Your milage **will** vary.

Use at your own risk. Always make a backup before .. making a backup :-D

## Missing features / planned ##
  * a .deb would be nice .. anyone ?
  * script should prompt for the restoredir if none is given
  * restoredir could be given as a relative path
  * incremental backup may be done with incremental datadirs and snapshots, but i'd need to change 'restore'
  * purge could be smarter; and prompt to
    * remove only numbered backups, opt above a certain nr/size
    * remove only orphaned files from the repos, opt above a certain size
    * create symlinks for large orphaned duplicates
    * purge the source instead of the repos
  * restore could be smarter; and prompt to
    * only restore existing files
    * not restore incremental backups from the repos
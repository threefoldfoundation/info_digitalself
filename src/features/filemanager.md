# Filemanager

> TODO: jimber (put some screenshots here)

## implementation

- files [dtfs](dtfs)
- interface = filebrowser xyz
- acl are metadata files in a directory (only support dir for now)
  - works with groups, simple rwd rights
  - identificaiton based on groupid (in group we have digital twinids or names)
- each DT has rest interface to expose file taking ACL's into consideration
- link feature = is a directory (specified as metadata), which links to remote directory of other DT

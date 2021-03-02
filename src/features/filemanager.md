![](img/filemanager.jpg)

# Filemanager

A versatile web-based file manager lets you organize your digital life.

You can store up to a petabyte of information and data can never be lost.

## unique

...

## implementation

- files are stored on [digital twin filesystem](threefold:dtfs)
- interface = filebrowser xyz
- acl are metadata files in a directory (only support directories for now)
  - works with groups, simple read-write rights
  - identificaiton based on groupId (in group we have digital twinIds or names)
- each Digital Twin has rest interface to expose file taking ACL's into consideration
- link feature = is a directory (specified as metadata), which links to remote directory of other DT

## roadmap

- integration with a sync tool like syncthing
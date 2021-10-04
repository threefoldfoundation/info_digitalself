# HyperDrive / HyperCore

- lives in Twin Proxy = nodejs

## commands

#### hyperdrive.new

- hyperdrive.new name:... path:...

Creates a new drive given a name and a path.

Returns drive get information.

#### hyperdrive.get

- hyperdrive.get name:...

Returns drive information:

```json
{
    "name": "some_drive_name",
    "path": "some_drive_path",
    "peers": [A list of peers currently replicating with this drive],
    "writeable": a boolean indicating whether a drive is writable,
    "discoveryKey": "A key derived from the public key that can be used to discovery other peers sharing this drive.",
    "version": "Get the current version of the drive (incrementing number)."
}
```

> TODO: what will be returned, json

#### hyperdrive.list

- hyperdrive.list

Lists all your hyperdrivers

Returns a list of drives:

```json
[{
    "name": "some_drive_name",
    "path": "some_drive_path",
    "peers": [A list of peers currently replicating with this drive],
    "writeable": a boolean indicating whether a drive is writable,
    "discoveryKey": "A key derived from the public key that can be used to discovery other peers sharing this drive.",
    "version": "Get the current version of the drive (incrementing number)."
}]
```

#### hyperdrive.delete

- hyperdrive.delete name:...

Deletes a hyperdrive by name.

Returns nothing

#### hyperdrive.upload

- hyperdrive.upload name:.. from:.. to:... exclude:

- name is the name of the hyperdrive to upload to
- from: is the source path where the info comes from can be file or dir, if dir all files will be copied onto the drive
- to: is the destination in the hyperdrive
- exclude: is list of excludes in simpel filter format e.g. exclude:'_/.git/','_.bak',...
  - / at end means dir

#### hyperdrive.download

- same but from & to are reversed

Return files as binary?

#### hyperdrive.stat

- hyperdrive.stat entry:...

Returns stat, example:

```json
Stat {
  dev: 0,
  nlink: 1,
  rdev: 0,
  blksize: 0,
  ino: 0,
  mode: 16877,
  uid: 0,
  gid: 0,
  size: 0,
  offset: 0,
  blocks: 0,
  atime: 2017-04-10T18:59:00.147Z,
  mtime: 2017-04-10T18:59:00.147Z,
  ctime: 2017-04-10T18:59:00.147Z,
  linkname: undefined
}
```

#### hyperdrive.mount.new / hyperdrive.mount.delete / hyperdrive.mount.list (phase 2)

Is like symlinking, embed other drives in yours

> TODO:

#### hyperdrive.sync

> TODO:

## more info

- see https://github.com/hypercore-protocol/hyperdrive
- see https://hypercore-protocol.org/guides/hyperspace/

## remarks

- the hyperdrives are identified by name

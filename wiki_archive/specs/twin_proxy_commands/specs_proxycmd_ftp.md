# FTP

- lives in Twin Proxy = nodejs

## commands

#### ftp.drive.new

- ftp.drive.new name:... prefix:... path:... index:... port:... aclname:...

- name: to identify the ftp drive
- prefix: is like a path before the path, prefix to the paths in the directory which makes up the ftp drive
- index: if on then will list the files (an ftp without listing can be super handy for security)
- path: is the exposed location
  - hyperdrive:/$name/ tells that it comes from a hypedrive with name $name
  - if nothing mentioned then just the path
- port: ftp port

#### ftp.drive.list

- ftp.drive.list

Return a list of drives:

```json
[
  {
    "name": "drive_name",
    "prefix": "path_prefix",
    "path": "some_path",
    "port": "some_port"
  }
]
```

> TODO: json which will be returned

#### webserver.site.delete

- ftp.drive.delete name:...

Deletes an FTP drive by name.

Returns nothing

## ACL

> TODO: need to describe the ACL features, see hamdy (Dylan)

same as http

> > IS NOT TO IMPLEMENTED IN PHASE 1, BUT IS HERE TO BE COMPLETE

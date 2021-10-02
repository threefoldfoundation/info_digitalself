# Webserver

- lives in Twin Proxy = nodejs

## commands

#### webserver.site.new

- webserver.site.new name:... prefix:... type:... path:... index:... domain:... port:...

- name: to identify the site
- prefix: of the site e.g. cloud would result in https://..../cloud/...
- type: enum(http,wiki,files)
  - http is http(s) default webserver on chosen dir
  - wiki is our wiki system from publisher, knows how to serve wiki pages
  - files is specificly made to expose files over http
- index: if on then will list the files (only relevant for file type)
- path: is the exposed location
  - hyperdrive:/$name/ tells that it comes from a hypedrive with name $name
  - if nothing mentioned then just the path
- domain: if domain, e.g. new.threefold.io
- port: http port

Returns the created webserver as json.

#### webserver.site.list

- webserver.site.list

Returns a list of webservers as json.

```json
[
  {
    "name": "some_site_name",
    "prefix": "some_prefix",
    "type": "http/wiki/files",
    "index": "some_index",
    "path": "some_path",
    "domain": "some_domain",
    "port": "some_port"
  }
]
```

> TODO: json which will be returned

#### webserver.site.delete

- webserver.site.delete name:...

Deletes a webserver by name.

Returns nothing

#### webserver.site.reload

Will reload metadata from the FS e.g. ACL.

#### webserver.site.acl.new / delete / list

...

## ACL

> TODO: need to describe the ACL features, see hamdy (Dylan)

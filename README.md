## rstudio-server

[![Build Status](https://travis-ci.org/Oefenweb/ansible-rstudio-server.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-rstudio-server) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-rstudio--server-blue.svg)](https://galaxy.ansible.com/list#/roles/4953)

Set up (the latest version of) [RStudio Server](https://www.rstudio.com/products/rstudio/download-server/) in Debian-like systems.

#### Requirements

* `curl` (will be installed)
* `r-base` (will not be installed)

#### Variables

* `rstudio_server_version` [default: `0.99.902`]: Version to install
* `rstudio_server_install` [default: `[]`]: Additional packages to install (e.g. `r-base`)

* `rstudio_server_www_port` [default: `8787`]: The port you want RStudio to listen on
* `rstudio_server_www_address` [default: `0.0.0.0`]: The address you want RStudio to listen on
* `rstudio_server_auth_required_user_group` [optional]: Limits the users who can login to RStudio to the members of a this group (e.g. `rstudio_users`)

## Dependencies

None

## Recommended

* `ansible-r` ([see](https://github.com/Oefenweb/ansible-r))

#### Example

```yaml
---
- hosts: all
  roles:
    - rstudio-server
```

#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-rstudio-server/issues)!

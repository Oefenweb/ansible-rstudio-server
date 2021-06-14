## rstudio-server

[![CI](https://github.com/Oefenweb/ansible-rstudio-server/workflows/CI/badge.svg)](https://github.com/Oefenweb/ansible-rstudio-server/actions?query=workflow%3ACI)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-rstudio--server-blue.svg)](https://galaxy.ansible.com/Oefenweb/rstudio_server/)

Set up (the latest version of) [RStudio Server](https://www.rstudio.com/products/rstudio/download-server/) in Debian-like systems.

#### Requirements

* `curl` (will be installed)
* `r-base` (will not be installed)

#### Variables

* `rstudio_server_version` [default: `1.4.1717`, `1.2.5042` for `Debian 8`]: Version to install
* `rstudio_server_install` [default: `[]`]: Additional packages to install (e.g. `r-base`)

* `rstudio_server_www_port` [default: `8787`]: The port you want RStudio to listen on
* `rstudio_server_www_address` [default: `0.0.0.0`]: The address you want RStudio to listen on
* `rstudio_server_auth_required_user_group` [optional]: Limits the users who can login to RStudio to the members of a this group (e.g. `rstudio_users`)
* `rstudio_server_which_r` [optional]: Override which version of R is used
* `rstudio_server_session_timeout_minutes` [optional]: Session timeout (e.g. `0`, no timeout)

## Dependencies

None

## Recommended

* `ansible-r` ([see](https://github.com/Oefenweb/ansible-r))
* `ansible-rstudio` ([see](https://github.com/Oefenweb/ansible-rstudio))

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

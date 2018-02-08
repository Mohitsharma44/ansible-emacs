Role Name
=========

Role for installing Emacs v25 and Prelude plugin

[![Build Status](https://travis-ci.org/Mohitsharma44/ansible-emacs.svg?branch=master)](https://travis-ci.org/Mohitsharma44/ansible-emacs)

Requirements
------------

N/A

Role Variables
--------------

### Emacs
If building emacs from source, the following variables needs to be defined:

``` yaml
BUILD_FROM_SRC: true
emacs_version: 25.3
emacs_ftp_url: http://ftpmirror.gnu.org/emacs
emacs_sha256: "sha256:f72c6a1b48b6fbaca2b991eed801964a208a2f8686c70940013db26cd37983c9"
emacs_build_dir: "/tmp/emacs-{{emacs_version}}"
emacs_install_loc: /usr/local
```

If not building from source, emacs is installed using [ppa:kelleyk/emacs](https://launchpad.net/~kelleyk/+archive/ubuntu/emacs)

SHA256 is the checksum that is used to verify the integrity of the download.

Dependencies
------------

N/A

Example Playbook
----------------

``` yaml
---

- hosts: all
  gather_facts: no

  tasks:
  - include_role:
    name: emacs

```

License
-------

MIT

Author Information
------------------

Mohit Sharma. Mohitsharma44@gmail.com

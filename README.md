# golang

[![Build Status](https://travis-ci.org/pari-/ansible-golang.svg?branch=master)](https://travis-ci.org/pari-/ansible-golang)

An Ansible role which installs and configures golang (The Go Programming Language)

<!-- toc -->

- [Requirements](#requirements)
- [Example](#example)
- [Defaults](#defaults)
- [Dependencies](#dependencies)
- [License](#license)
- [Author Information](#author-information)

<!-- tocstop -->

## Requirements

Currently this role is developed for and tested on Debian GNU/Linux (release: stretch).

Ansible version compatibility: [Dockerfile](https://github.com/pari-/docker-debian-ansible/blob/master/debian/stretch/Dockerfile)

## Example

```yaml
---

- hosts: "all"
  roles:
    - role: "ansible-golang"
      tags:
        - "golang"
  post_tasks:
    - block:
        - include: "tests/test_golang.yml"
      tags:
        - "tests"
```

## Defaults

Available role variables and their respective default values are to be found in: [defaults/main.yml](https://github.com/pari-/ansible-golang/blob/master/defaults/main.yml)

## Dependencies

None

## License

MIT

## Author Information

* Patrick Ringl

# golang

An Ansible role which installs and configures golang (The Go Programming Language)

<!-- toc -->

- [Requirements](#requirements)
- [Example](#example)
- [Role Variables](#role-variables)
- [Dependencies](#dependencies)
- [License](#license)
- [Author Information](#author-information)

<!-- tocstop -->

## Requirements

Currently this role is developed for and tested on Debian GNU/Linux (release: jessie). It is assumed to work on other Debian distributions as well.

Ansible version in use for development: 2.2.1

## Example

```yaml
- hosts: golang-servers

  roles: 
    - "ansible-golang"
```

## Role Variables

Available variables are listed below, along with default values (see defaults/main.yml). They're generally prefixed with `golang_` (which I deliberately leave out here for better formatting).

variable | default | notes
-------- | ------- | -----
`environment_file` | `/etc/profile.d/golang.sh` | `Absolute path where $GOROOT/$PATH exports are stored`
`go_version` | `1.8` | `The version of the Go Programming Language that is going to be installed`
`supported_distro_list` | `['jessie']` | `A list of distribution releases this role supports`
`tarball_dest` | `/tmp` | `Destination where golang's tarball is stored`
`tarball_name` | `go{{ golang_go_version }}.linux-amd64.tar.gz` | `Naming schema of golang's tarball`
`test_directory` | `/tmp` | `The directory where tests will be temporary stored and run in (auto cleanup)`
`unarchive_dest` | `/usr/local` | `Destination where golang will be installed to`
`upstream_url` | `https://storage.googleapis.com/golang` | `The URL to where golang's tarballs can be retrieved from`

## Dependencies

None

## License

MIT

## Author Information

* Patrick Ringl

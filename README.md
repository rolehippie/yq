# yq

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/yq)
[![General Workflow](https://github.com/rolehippie/yq/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/yq/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/yq/actions/workflows/docs.yml/badge.svg)](https://github.com/rolehippie/yq/actions/workflows/docs.yml)
[![Galaxy Workflow](https://github.com/rolehippie/yq/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/yq/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/yq)](https://github.com/rolehippie/yq/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.yq-blue)](https://galaxy.ansible.com/rolehippie/yq)

Ansible role to install yq the jq yaml counterpart.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [yq_arch](#yq_arch)
  - [yq_download](#yq_download)
  - [yq_version](#yq_version)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`

## Default Variables

### yq_arch

Architecture of the static binary

#### Default value

```YAML
yq_arch: "{{ 'arm64' if ansible_architecture == 'aarch64' else 'amd64' }}"
```

### yq_download

URL to the archive of the release to install

#### Default value

```YAML
yq_download: https://github.com/mikefarah/yq/releases/download/v{{ yq_version }}/yq_linux_{{
  yq_arch }}
```

### yq_version

Version of the release to install

#### Default value

```YAML
yq_version: 4.44.6
```

## Discovered Tags

**_yq_**


## Dependencies

- None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)

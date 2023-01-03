# Changelog

All notable changes to this project will be documented in this file.

- [2.2.3 (2023-01-03)](#223-2023-01-03)
- [2.2.2 (2022-12-20)](#222-2022-12-20)
- [2.2.1 (2022-12-20)](#221-2022-12-20)
- [2.2.0 (2022-01-28)](#220-2022-01-28)
- [2.1.3 (2021-10-10)](#213-2021-10-10)
- [2.1.2 (2021-05-08)](#212-2021-05-08)
- [2.1.1 (2021-05-08)](#211-2021-05-08)
- [2.1.0 (2021-05-06)](#210-2021-05-06)
- [1.0.2 (2021-05-03)](#102-2021-05-03)
- [2.0.1 (2021-04-28)](#201-2021-04-28)
- [2.0.0 (2021-04-28)](#200-2021-04-28)
- [1.0.1 (2020-05-15)](#101-2020-05-15)
- [1.0.0 (2020-04-12)](#100-2020-04-12)

---

<a name="2.2.3"></a>
## [2.2.3](https://github.com/aisbergg/ansible-role-acl/compare/v2.2.2...v2.2.3) (2023-01-03)

### Bug Fixes

- fix syntax of requirements file


<a name="2.2.2"></a>
## [2.2.2](https://github.com/aisbergg/ansible-role-acl/compare/v2.2.1...v2.2.2) (2022-12-20)


<a name="2.2.1"></a>
## [2.2.1](https://github.com/aisbergg/ansible-role-acl/compare/v2.2.0...v2.2.1) (2022-12-20)

### CI Configuration

- add branch explicitly to make Ansible import action happy
- bump Ansible Galaxy action version

### Chores

- update linting config and add tox.ini
- don't use bump2version to include the CHANGELOG in the bump commit, it doesn't do a good job


<a name="2.2.0"></a>
## [2.2.0](https://github.com/aisbergg/ansible-role-acl/compare/v2.1.3...v2.2.0) (2022-01-28)

### CI Configuration

- fix automatic release and publish process

### Chores

- include changelog in bump commits
- update changelog template
- **.ansible-lint:** update linter config
- **.pre-commit-config.yaml:** bump pre-commit hook versions
- **CHANGELOG.tpl.md:** update changelog template
- **requirements.yml:** add role requirements


<a name="2.1.3"></a>
## [2.1.3](https://github.com/aisbergg/ansible-role-acl/compare/v2.1.2...v2.1.3) (2021-10-10)

### Chores

- **CHANGELOG.md:** update changelog

### Code Refactoring

- rename task files


<a name="2.1.2"></a>
## [2.1.2](https://github.com/aisbergg/ansible-role-acl/compare/v2.1.1...v2.1.2) (2021-05-08)

### Documentation

- **changelog:** change TOC to be more like the actual section names


<a name="2.1.1"></a>
## [2.1.1](https://github.com/aisbergg/ansible-role-acl/compare/v2.1.0...v2.1.1) (2021-05-08)

### Documentation

- **changelog:** update changelog
- **changelog:** update changelog template


<a name="2.1.0"></a>
## [2.1.0](https://github.com/aisbergg/ansible-role-acl/compare/v1.0.2...v2.1.0) (2021-05-06)

### Build System

- change bump message format
- update development configs
- **lint:** change linter configuration
- **pre-commit:** use pre-commit hooks

### Code Refactoring

- drop support for Ansible version < 2.10

### Documentation

- **CHANGELOG.md:** update changelog
- **README.md:** document all variables and reword the role introduction
- **changelog:** update changelog

### Features

- add option to create missing dirs/files and refactor code

### ⚠ BREAKING CHANGES


drop support for Ansible version < 2.10


<a name="1.0.2"></a>
## [1.0.2](https://github.com/aisbergg/ansible-role-acl/compare/v2.0.1...v1.0.2) (2021-05-03)


<a name="2.0.1"></a>
## [2.0.1](https://github.com/aisbergg/ansible-role-acl/compare/v2.0.0...v2.0.1) (2021-04-28)

### Build System

- update development configs


<a name="2.0.0"></a>
## [2.0.0](https://github.com/aisbergg/ansible-role-acl/compare/v1.0.1...v2.0.0) (2021-04-28)

### Code Refactoring

- drop support for Ansible version < 2.10
- clean up

### Documentation

- **CHANGELOG.md:** update changelog

### ⚠ BREAKING CHANGES


drop support for Ansible version < 2.10


<a name="1.0.1"></a>
## [1.0.1](https://github.com/aisbergg/ansible-role-acl/compare/v1.0.0...v1.0.1) (2020-05-15)

### Bug Fixes

- **acl.yml:** fix value type of 'default' variable


<a name="1.0.0"></a>
## [1.0.0]() (2020-04-12)

Initial Release

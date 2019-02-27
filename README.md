# python_pip

Ansible role to install pip (python modules)

## Installation

```yaml
   ansible-galaxy install zerodowntime.python_pip
```

## Requirements

This role requires Ansible 2.5 or higher.

Supported platforms:

```yaml
  platforms:
    - name: EL
      versions:
        - 7
    - name: Ubuntu
      versions:
      - trusty
      - xenial
```

## Default role variables

| Variable name            | Required? |  Type  | Description                      |
|:------------------------ |:---------:|:------:|:-------------------------------- |
| python_pip__upgrade      |    yes    |  bool  | Upgrade python-pip after install |
| python_pip__package_name |    yes    | string | Installed system package name    |

**All variables are described in [defaults/main.yml](defaults/main.yml) file.**

## Static role variables

| Variable name                    |  Type  | Description                                  |
|:-------------------------------- |:------:|:-------------------------------------------- |
| python_pip__version              | string | Installed pip version                        |
| python_pip__default_package_name | string | system pip package name, specified by system |

**All static variables are described in [vars/main.yml](vars/main.yml) file.**

## Example Playbook

```yaml
    - hosts: all
      become: true
      roles:

      - role: zerodowntime.python_pip
        python_pip__upgrade: true
```

## License

[Apache License 2.0](LICENSE)

## Support

ansible@zerodowntime.pl

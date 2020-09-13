# Intro [![Build Status](https://www.travis-ci.com/triplepoint/ansible-dnsmasq.svg?branch=main)](https://www.travis-ci.com/triplepoint/ansible-dnsmasq)
Set up and install `dnsmasq`, to handle DHCP and DNS.

## Requirements
None.

## Role Variables
See the [comment in the default variables file](defaults/main.yml) for information on configuration.

Note that not all the bells and whistles of `dnsmasq` are configurable in this role.

Also, see the [dnsmasq config documentation](http://thekelleys.org.uk/gitweb/?p=dnsmasq.git;a=blob_plain;f=dnsmasq.conf.example;hb=HEAD) for more information on dnsmasq configuration details.

## Dependencies
None.

## Example Playbook
    - hosts: whatever
      roles:
        - triplepoint.dnsmasq

## Role Testing
This role is tested with `molecule`, using `pipenv` to handle dependencies and the Python testing environment.

### Setting Up Your Execution Environment
``` sh
pip install pipenv
```

Once you have `pipenv` installed, you can build the execution virtualenv with:
``` sh
pipenv install --dev
```

### Running Tests
Once you have your environment configured, you can execute `molecule` with:
``` sh
pipenv run molecule test
```

### Regenerating the Lock File
You shouldn't have to do this very often, but if you change the Python package requirements using `pipenv install {some_package}` commands or by editing the `Pipfile` directly, or if you find the build dependencies have fallen out of date, you might need to regenerate the `Pipfile.lock`.
``` sh
pipenv update --dev
```
Be sure and check in the regenerated `Pipfile.lock` when this process is complete.

## License
MIT

# software_software-properties-common
=========

This role will install software-properties-common software

## Requirements
------------

All requirements will appear on requirements-software.yml file

## Role Variables
--------------

Not defined yet. But in the future we could stage software version in here

## Dependencies
------------

All dependencies will appear on requirements-software.yml file

## Example requirements
--------------------

    requirements-software.yml

    ---
    - src: git@github.com:xussof/software_software-properties-common
      scm: git
      version: master
      name: software_software-properties-common

## Example Playbook
----------------

    test-software.yml

    ---
    - hosts: localhost
      pre_tasks:
        - raw: ansible-galaxy install -f -r requirements-software.yml
      vars_files:
        - "encrypted.yml"
      tasks:
        - name: Including role to test
          include_role:
            name: software_software-properties-common

## Example encrypted
-----------------

    encrypted.yml

    ---
    example_sudo_pass: yourpass

## Example calling playbook
------------------------

    ansible-playbook test-software.yml --extra-vars "ansible_become_pass=example_sudo_pass"


## License
-------

BSD

## Author Information
------------------
Made by @xussof

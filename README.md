# Ansible Role: phpunit

[![Build Status](https://travis-ci.org/oktapodia/ansible-role-phpunit.svg?branch=master)](https://travis-ci.org/oktapodia/ansible-role-phpunit)

Installs phpunit, the PHP Dependency Manager, on any Linux or UNIX system.

Heavily inspired of [ansible-role-composer](https://github.com/geerlingguy/ansible-role-composer) by Jeff Geerling 

## Requirements

  - `php` (version 5.4+) should be installed and working (you can use the `geerlingguy.php` role to install).
  - `git` should be installed and working (you can use the `geerlingguy.git` role to install).

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    phpunit_path: /usr/local/bin/phpunit

The path where phpunit will be installed and available to your system. Should be in your user's `$PATH` so you can run commands simply with `phpunit` instead of the full path.

    php_executable: php

The executable name or full path to the PHP executable. This is defaulted to `php` if you don't override the variable.

## Dependencies

None (but make sure you've installed PHP; the `geerlingguy.php` role is recommended).

## Example Playbook

    - hosts: servers
      roles:
        - oktapodia.phpunit

After the playbook runs, `phpunit` will be placed in `/usr/local/bin/phpunit` (this location is configurable), and will be accessible via normal system accounts.

## License

MIT / BSD

## Author Information

This role was created in 2017 by [Sebastien BRAMILLE](https://sebastien-bramille.com/).

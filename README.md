hyperized.pip
=========

_Python package manager_

Requirements
------------

Ansible 2.5 or above is highly recommended.

Role Variables
--------------

    pip_state: latest
    pip_executable: /usr/bin/pip3
    pip_name:
    pip_extra_args:


Dependencies
------------

    hyperized.package
    hyperized.apt-repo

Example Playbook
----------------

    - hosts: all
      become: yes
      roles:
        - role: hyperized.pip
          pip_name: docker
        - role: hyperized.pip
          pip_name: 'requests[security]', pip_extra_args: '--upgrade'
          

License
-------

MIT

Author Information
------------------

Gerben Geijteman <gerben@hyperized.net>

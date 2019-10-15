ansible-role-docker-repoinstall
=========

Role written to create a basic docker repository.

Requirements
------------
Role assumes docker is installed. Future versions will consider other container runtimes.

Role Variables
--------------



Dependencies
------------

You can use the ansible-role-docker-install. This needs to be run before using this role.

Example Playbook
----------------
# Example playbook
- name: Docker repository install
  hosts: localhost
  become: true

  tasks:
    - name: "Include the docker repository install role"
      include_role:
        name: ../roles/ansible-role-docker-repoinstall

License
-------

MIT

Author Information
------------------

Ken Hitchcock
github.com/KenHitchcock

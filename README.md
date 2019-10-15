ansible-role-docker-repoinstall
=========

Role written to create a basic docker repository.

Requirements
------------
Role assumes docker is installed. Future versions will consider other container runtimes.

Role Variables
--------------
### Do you want to install the repo. Default answer is yes
    docker_repo_install: "yes"

### Do you want a secure or insecure registry. Default is insecure.
    docker_repo_insecure: "yes"

### If you se the docker_repo_insecure: "no" then you need to specify cert details.
### Certs have to be created prior to running this role and the variables below need to be set.
    docker_repo_tls_cert: domain.crt
    docker_repo_tls_key: domain.key
    docker_repo_cert_uploadpath: "files/"


Dependencies
------------

You can use the ansible-role-docker-install. This needs to be run before using this role.

Example Playbook
----------------

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

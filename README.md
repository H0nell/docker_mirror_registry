mirror-registry
=========

This role create and start mirror-registry which pull and cache docker images from DockerHub.
See more: https://docs.docker.com/registry/recipes/mirror/

Important Role Variables
--------------

mir_registry_port: port on host system which will be assigned to the container (default: "5000").
mir_registry_config_dir: location, where pulled images will be stored (default: "/opt/registry").
mir_registry_dockerhub_username: username from Dockerhub account.
mir_registry_dockerhub_password: password from Dockerhub account.
mir_registry_docker_tag: specify a registry image tag (default: "latest").
mir_registry_bind_ip: specify listen ip (default: "0.0.0.0").

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: example.hosts
      become: yes
      become_user: root
      roles:
        - role: docker_mirror_registry
          mir_registry_docker_tag: "2"
          mir_registry_dockerhub_username: example.username
          mir_registry_dockerhub_password: example.password
          

License
-------

GPLv3

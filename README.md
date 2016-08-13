Role Name
=========

Role installs Rancher agent and connect it to Ranger server.

Requirements
------------

Running Docker engine is required on host.
Running Rancher server is required.


Role Variables
--------------

Available variables are listed below, along with default values:

* rancher_agent_name: ranger_agent (Docker container name for Ranger angent)
* rancher_agent_version: 1.0.2
* rancher_server: 192.168.165.211 (IP Adress or hostname of Ranger server)
* rancher_port: 8080 (Port on which Rancher server is listening)

Dependencies
------------

Example Playbook
----------------

    - hosts: rancherhost
      roles:
         - dbs_docker
         - dbs_rancher_server

License
-------

BSD

Author Information
------------------
it's me

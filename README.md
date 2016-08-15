Ansible role: dbs_rancher_node
=========

Role installs Rancher agent and connect it to Ranger server.

Requirements
------------

Running Docker engine is required.
Running Rancher server is required.
Make sure that Rancher agent host can communicate with Rancher server host on ports:
* Rancher server port tcp (default 8080) (http rest api)
* udp port 500 and 4500 for rancher internal data traffic


Role Variables
--------------

Available variables are listed below, along with default values:

* rancher_agent_name: default: rancher_agent (Docker container name for Ranger agent)
* rancher_agent_version:  default: 1.0.2  (see dockerhub rancher/agent for latest tag)
* rancher_server: default: localhost, it is necesarry that you set this to ip address or hostname on which Rancher server ist listening
* rancher_port: default: 8080 (port on which Rancher server is listening)

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

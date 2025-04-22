Role Name 
=========

**nginx** – This Ansible role installs and configures the NGINX web server on a Linux-based system (e.g., Ubuntu EC2 instance). It ensures NGINX is installed, enabled, and running as a service.

Requirements
------------

- Target system should be Debian-based (Ubuntu tested).
- The Ansible control node should have passwordless SSH access to the target.
- Port 80 should be open in the instance's security group (for HTTP access).
- Python and `apt` module support should be present on the target.

Role Variables
--------------

This role currently does not use any custom variables.

Dependencies
------------

This role has no external dependencies.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: webservers
      become: yes
      roles:
         - nginxsetup

License
-------

MIT

Author Information
------------------

Vinay Vardhan Komaragiri
📧 vinayvardhan9@gmail.com
🔗 LinkedIn

apf_firewall
=========

An Ansible role that installs and configures APF (Advanced Policy Firewall)

For more information about APF can be found [here](https://www.rfxn.com/projects/advanced-policy-firewall/)

Requirements
------------

None

Role Variables
--------------

See defaults/main.yml.

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: lukasgibb.apf_firewall, apf_firewall_IG_TCP_CPORTS: "22,80,443" }

License
-------

MIT

Author Information
------------------

This role was created in 2019 by:
[Lukas Gibb](https://github.com/LukasGibb) - [CloudJourneyman.com](http://www.cloudjourneyman.com/)

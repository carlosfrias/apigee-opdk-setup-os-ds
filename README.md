Apigee OPDK Setup OS DS
=========

This role performs configuration changes to the operating system for Cassandra. This role updates attributes in 
/etc/sysctl.conf and update /etc/security/limits.d/ with the file apigee-ds.limits.conf.

Requirements
------------

The installation of Apigee OPDK requires root access. Credentials must also be supplied to override the empty placeholders
provided here. It is recommended that credentials be consolidated into a single credentials.yml file that can be stored 
separately. It is assumed that files containing credentials are stored in the ~/.apigee folder. 

Role Variables
--------------

Default update to the attribute in the net.ipv4.tcp_fin_timeout /etc/sysctl.conf system file. 

    apigee_net_ipv4_tcp_fin_timeout: 15
    
Default update to the attribute in the vm.max_map_count /etc/sysctl.conf system file. 
    
    apigee_max_map_count: 131072

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: opdk-setup-os-ds }

License
-------

Apache License Version 2.0, January 2004

Author Information
------------------

Carlos Frias

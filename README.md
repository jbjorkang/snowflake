Ansible Role: Snowflake proxy
=========

An Ansible Role that Snowflake proxy on GNU/Linux and FreeBSD

Snowflake proxies are one of the systems that the Tor network has in place to address censorship. This type of bridge, currently under development, adds to the alternatives and anti-censorship efforts of Pluggable Transports (PTs) such as obfs4 and meek-azure. Bridges designed as access options for people where the Tor network is blocked.

With this ansible role you can install, configure and operate snowflake proxies.

Requirements
------------

None.

Role Variables
----------------

    clients: 0

Maximum concurrent clients by default is 0 = non limit

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
          - nvjacobo.snowflake

Example Playbook with maximum concurrent clients (for example 150)
----------------

    - hosts: servers
      vars:
         clients: 150
      roles:
        - nvjacobo.snowflake

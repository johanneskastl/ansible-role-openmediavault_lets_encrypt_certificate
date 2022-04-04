openmediavault_lets_encrypt_certificate
=========

Hook script to import a Let's Encrypt certificate into Openmediavault.

Based loosely on a [nice blog post by Adrian Pavelescu](https://adrian.work/post/openmediavault-5-letsencrypt-certbot-dns-cloudflare/).

Requirements
------------

None.

Role Variables
--------------

None.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: 'johanneskastl.openmediavault_lets_encrypt_certificate'

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.

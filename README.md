![Ansible Lint](https://github.com/johanneskastl/ansible-role-openmediavault_lets_encrypt_certificate/workflows/Ansible%20Lint/badge.svg)

openmediavault_lets_encrypt_certificate
=========

Hook script to import a Let's Encrypt certificate into Openmediavault.

Based loosely on a [nice blog post by Adrian Pavelescu](https://adrian.work/post/openmediavault-5-letsencrypt-certbot-dns-cloudflare/), but adapted to work with python3 and with more error handling.

Requirements
------------

None.

Role Variables
--------------

- `le_certificate_cert_file`: path to the certificate (crt) file that should be imported
- `le_certificate_key_file`: path to the certificate's private key file that should be imported

Please note, those are not the locations where openmediavault is storing the key, i.e. do NOT use `/etc/ssl/certs/openmediavault-<uuid>.crt` or `/etc/ssl/private/openmediavault-<uuid>.key`!


Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: 'johanneskastl.openmediavault_lets_encrypt_certificate'
          vars:
            le_certificate_cert_file: '/etc/ssl/private/my-lets-encrypt/certificate.crt'
            le_certificate_key_file: '/etc/ssl/private/my-lets-encrypt/certificate.key'

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.

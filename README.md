spk83.pki-client
================

A role to generate certificate signing request (CSR) and private key for a host using CFSSL. Supports subject alternate names. 

Requirements
------------

See [meta/main.yml](meta/main.yml)

Role Variables
--------------

See [defaults/main.yml](defaults/main.yml)

Dependencies
------------

See [meta/main.yml](meta/main.yml)

Example Playbook
----------------
Recommended to target localhost if you're managing a local eyes-above-the-wall PKI.

```yml
- hosts: localhost
  connection: local
  roles:
    - role: spk83.pki-client
      pki_client_dir: ~/pki
      pki_client_cname: www-1.example.com
	  pki_client_sans:
  		- www.example.com
```

License
-------

MIT

Author Information
------------------

Vishal Shah vishal.shah@nyu.edu

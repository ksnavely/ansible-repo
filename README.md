# ansible-repo

This repo holds an systems stack for my own web services. I try to follow ansible best practices, but bear with me -- I come from chef, am learning ansible, and am actively improving this codebase.

## Playbooks

### website

This playbook stands up my person website stack. There are a few component roles:

#### flask-website
   - The [website](https://github.com/ksnavely/website) repo controls the front page of the site.
   - The [rockfall](https://github.com/ksnavely/rockfall) repo hold a fun HTML5/JS game -- can you make it to level 5?

#### nginx
   - The nginx role stands up a proxy server in front of the overall website's components.
   - Included is a certs task for setting up the TLS certificate

#### mongodb
   - This role stands up a single mongo instance.

#### letsencrypt
   - This role performs the ACME cert challenge against the letsencrypt service for self-serve TLS cert issuance.

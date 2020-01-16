tech_asgn
=========

Creates two groups: Marvel and DC

Creates five users and assigns it to specific groups

Installs packages:
   - bzip2
   - vim
   - git

Downloads and extracts tgz file

Role Variables
--------------

Role variables defined in vars/main.yml:

bw_groups:
 - name: Marvel
   gid: 1
 - name: DC
   gid: 2

bw_users:
 - name: t.stark
   comment: Tony Stark
   groups: wheel,Marvel
 - name: b.banner
   comment: Bruce Banner
   group: Marvel
 - name: s.rogers
   comment: Steve Rogers
   group: Marvel
 - name: c.kent
   comment: Clark Kent
   groups: wheel,DC
 - name: b.wayne
   comment: Bruce Wayne
   group: DC



Example Playbook
----------------

     ---
        - name: all
        hosts: all
        become: true
        become_method: sudo
        roles:
         - common_FD

License
-------

BSD

Author Information
------------------

Sukhpreet kaur

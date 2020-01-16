tech_asgn
=========

Creates two groups: Marvel and DC

Creates five users and assigns it to specific groups

Installs packages:
   - bzip2
   - vim
   - git

Downloads and extracts tgz file

Execute the playbook by running ansible-playbook playbook.yml

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



Playbook
----------------

     ---
        - name: all
        hosts: all
        become: true
        become_method: sudo
        roles:
         - tech_asgn

License
-------

BSD

Author Information
------------------

Sukhpreet kaur

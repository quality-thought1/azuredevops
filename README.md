---
 - name: apache application
   become: yes
   hosts: all
   tasks:
    - name: Install apache httpd
      ansible.builtin.apt:
        name: apache2
        state: present
    - name: Install php-fm
      ansible.builtin.apt:
        name:
          - php
          - php-fpm
        state: present 
    

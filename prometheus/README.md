Role Name
=========


This is role is to install Prometheus jmx exporter for zookeeper and kafka broker services as of now. This roles also takes care of restar in one by one order by cautiously checking leader and controller

Requirements
------------
nc utility 

Role Variables
--------------
Please use below compulsory variable to run role. Restart variables are placed intentionally  so that we dont restart accidently on first attempt.
---
 - name: Deploy prometheus
   hosts: all
   vars:
     zookeeper_prometheus_enable: false
     kafka_broker_prometheus_enable: true
     kafka_broker_restart: false  # set true if you want to test restart
     zookeeper_restart: false # set true if you want to test restart
   roles:
    - { role: /Users/sameer_modak/ansibledemo/prometheus }


Dependencies
------------

Please go throut vars/main.yml and defaults/main.yml

Example Playbook
----------------

 - name: Deploy prometheus
   hosts: all
   vars:
     zookeeper_prometheus_enable: false
     kafka_broker_prometheus_enable: true
     kafka_broker_restart: false  # set true if you want to test restart
     zookeeper_restart: false # set true if you want to test restart
   roles:
    - { role: /Users/sameer_modak/ansibledemo/prometheus }



License
-------

DBOPS KAFKA

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

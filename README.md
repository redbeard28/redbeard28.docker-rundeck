redbeard28.docker-rundeck
=========

This ansible role deploy a rundeck container

Requirements
------------

You must provide an posgres server with already a database for rundeck.


Role Variables
--------------
```yaml
ENV_RUNDECK_DATABASE_URL: 'jdbc:postgresql://hostname_postgres:5432/rundeckdb'
ENV_POSTGRES_USER: 'postgresUSER'
ENV_POSTGRES_PASSWORD: 'mybigsecretpassword'
ENV_RUNDECK_EXTERNAL_URL: 'https://myexternal_url.mydomain.com'
ENV_RUNDECK_MAIL_SMTP_PORT: '25'
ENV_RUNDECK_MAIL_SMTP_HOST: 'mysmtp.domain.com'
ENV_RUNDECK_PORT: '4440'
```

Dependencies
------------
You must provide an posgres server with already a database for rundeck.


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
````yaml

- name: "Deploy rundeck"
  hosts: all
  become: yes
  roles:
    - { role: roles/redbeard28.docker-rundeck, tags: [container_rundeck] }
````

License
-------

BSD

Author Information
------------------

Jeremie CUADRADO
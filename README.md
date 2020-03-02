docker-mumble-NGINX-Let's Encrypt
=============


<p align="center">
    <img src="Docker_NGINX_PORTAINER_MUMBLE.png" alt="Docker Mumble NGINX LET'S ENCRYPT" >

<p align="center">
  Docker image for Mumble server.
</p>

INSTRUCTION
---------------------

This version use the projet of EvertRamos : docker-compose-letsencrypt-nginx-proxy-companion

Please install first evertramos/docker-compose-letsencrypt-nginx-proxy-companion
https://github.com/evertramos/docker-compose-letsencrypt-nginx-proxy-companion

Configure files projet Mumble Server
---------------------

1: Configure .env
---------------------
Open .env and change :

a) adress_mumble_server= Change Address for your server Mumble

b) port_mumble_server= Change the port of mumble (by default : 64738)

c) SERVER_PASSWORD= Change Password of your superuser

d) DOMAINS=mumble.your.domain.com

e) LETSENCRYPT_EMAIL=your_email_to_register@lets_encrypt

OPTIONNAL : Edit the Config
---------------
Edit :

files/config.ini

And add your instruction !

2 : Running the Container
---------------------

In order to persist configuration data when upgrading your container you should create a named data
volume. This is not required but is _highly_ recommended.

    docker volume create --name mumble-data

And

    docker-compose up -d

Troubleshooting
---------------

For general help and support for MUMBLE join our [Slack Workspace](https://join.slack.com/t/phlaknet/shared_invite/enQtNzk0ODkwMDA2MDg0LWI4NDAyZGRlMWEyMWNhZmJmZjgzM2Y2YTdhNmZlYzc3OGNjZWU5MDNkMTcwMWQ5OGI5ODFmMjI5OWVkZTliN2M).

Please report bugs for MUMBLE to the [GitHub Issue Tracker](https://github.com/PHLAK/docker-mumble/issues).

Copyright
---------

This project is licensed under the [MIT License](https://github.com/PHLAK/docker-mumble/blob/master/LICENSE).

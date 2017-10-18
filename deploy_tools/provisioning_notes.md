Provisioning a new site
=======================

## Required packages:

* nginx
* Python 3.6
* virtualenv + pip
* Git

eg, on Ubuntu:

    sudo add-apt-repository ppa:deadsnakes/ppa && apt-get update
    sudo apt-get install nginx git python3.6 python3.6-venv

## Nginx Virtaul Host config

* See nginx.template.conf
* Replace {SITENAME} with, e.g., staging.example.com
* Replace {USER} with your user on the server.

## Systemd Virtual Host service

* See gunicorn-systemd.template.service
* Replace {SITENAME} with, e.g., staging.example.com
* Replace {USER} with your user on the server.

## Folder structure:
Assume we have a user account at /home/{USER}
~~~
/home/{USER}
└── sites
    └── {SITENAME}
        ├── database
        ├── source
        ├── static
        └── virtualenv
~~~

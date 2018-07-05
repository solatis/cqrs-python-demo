# Xomnia Microservices & Streaming Data

## microservices

Forked off the excellent cqrs-python-data introduction to CQRS, this repository contains
a base framework of:

* a working CQRS system
* with event sourcing
* a view model
* commands
* single REST api (for convenience)

## Install

Easiest way to get this up and running is to use [docker-compose](https://docs.docker.com/compose/).

**2. For docker-compose:**
`docker-compose up -d --build`

**2. Locally**

**setup python**
`virtualenv env`

`. env/bin/activate`

`pip install -r requirements.txt`

**start the view model sync**

`python apps/readaccount/app.py`

**start the REST api**

`gunicorn apps.restaccount.app`

## Development
`docker-compose up -d postgres eventstore`

see `docker-compose.yml` for exposed ports, passwords, et al.

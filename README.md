[![Build Status](https://travis-ci.org/jihchi/docker-nginx-consul.svg?branch=master)](https://travis-ci.org/jihchi/docker-nginx-consul)

[![](https://badge.imagelayers.io/jihchi/nginx-consul.svg)](https://imagelayers.io/?images=jihchi/nginx-consul 'Get your own badge on imagelayers.io')

# Supported tags and respective Dockerfile links

- latest, 1.9.15_0.14.0 (mainline/Dockerfile)
- stable, 1.10.0_0.14.0 (stable/Dockerfile)

# Nginx with Consul Template

This Docker image follows official Nginx image extended with Consul Template to allow to refresh configuration based on the changes in Consul repository

# How-to

Create your data volume image and place required configuration files based on the following matrix:

* /etc/nginx/conf.d -> nginx configuration
* /etc/consul-template/conf -> Consul Template configurations taken and merged alphabetically - https://github.com/hashicorp/consul-template
* /etc/consul-template/templates -> a good place to situate your templates defined in the configuration

# Run

```
docker run --rm --volumes-from=yourdata-image -ti jihchi/nginx-consul
```

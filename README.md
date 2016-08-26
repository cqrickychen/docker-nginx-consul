[![Build Status](https://travis-ci.org/jihchi/docker-nginx-consul.svg?branch=master)](https://travis-ci.org/jihchi/docker-nginx-consul)
[![](https://badge.imagelayers.io/jihchi/nginx-consul.svg)](https://imagelayers.io/?images=jihchi/nginx-consul 'Get your own badge on imagelayers.io')
[![Docker Stars](https://img.shields.io/docker/stars/jihchi/nginx-consul.svg)](https://hub.docker.com/r/jihchi/nginx-consul/)
[![Docker Pulls](https://img.shields.io/docker/pulls/jihchi/nginx-consul.svg)](https://hub.docker.com/r/jihchi/nginx-consul/)

# Supported tags and respective Dockerfile links

- [`latest`](https://github.com/jihchi/docker-nginx-consul/blob/master/Dockerfile), [`1.11.3_0.14.0`](https://github.com/jihchi/docker-nginx-consul/blob/1.11.3_0.14.0/Dockerfile)
- [`stable`](https://github.com/jihchi/docker-nginx-consul/blob/stable/Dockerfile), [`1.10.0_0.14.0`](https://github.com/jihchi/docker-nginx-consul/blob/1.10.0_0.14.0/Dockerfile)

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

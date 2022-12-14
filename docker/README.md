# Ontoserver deployment example project

This project provides an example deployment for [Ontoserver](https://ontoserver.csiro.au). It uses an NGINX cache in addition to the default Ontoserver deployment described at https://ontoserver.csiro.au/docs.

The deployment in the default docker-compose file looks like this:

![Ontoserver deployment diagram](https://github.com/aehrc/ontoserver-deploy/blob/master/deployment.png)

To add HTTPS support:
 * Add your fullchain and private key files to ontocache/conf/certs/
 * Edit ontocache/conf/snippets/ssl-your.domain.here.conf (and if you rename the file, make sure you fix /ontocache/conf/nginx.conf to match)
 * Edit docker-compose to expose the cache's port 443 as 8443 instead of port 80 as 8080

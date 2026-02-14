---
sidebar_position: 3
---

# Note about TLS certificates

The eLabFTW container can run an HTTP or HTTPS server. Both will run internally on port 443. This page describes several options you can choose regarding TLS configuration.

## Option A: HTTP mode with a reverse proxy (Apache, nginx, HAProxy, traefik, ...)

You can run the container in HTTP mode (internal port 443) only if you have a reverse proxy in front doing TLS termination and sending the `X-Forwarded-Proto` header.

- Set `DISABLE_HTTPS=true`

Reverse proxy configuration examples can be found here: https://github.com/elabftw/elabdoc/tree/master/config_examples/.

## Option B: HTTPS mode with Let's Encrypt certificates

In order to request Let's Encrypt certificates, you need to install `certbot` and have your server publicly accessible. See the official Let's Encrypt documentation for your system: https://letsencrypt.org/getting-started/.

When requesting a new certificate, make sure that port 80 is open (and also port 443 for eLabFTW if it is the one you want to use). Once certbot is installed, the command to use might look like this:

`certbot certonly --standalone -d elab.example.org`

- Set `DISABLE_HTTPS=false`
- Set `ENABLE_LETSENCRYPT=true`
- Set `SERVER_NAME` with a correct value
- Uncomment the line `- /etc/letsencrypt:/ssl` in the `volumes:` part of the yml config file.

## Option C: HTTPS mode with custom certificates

Have the private key and certificate in PEM format in the folder `/etc/letsencrypt/live/SERVER_NAME/` where `SERVER_NAME` matches the `SERVER_NAME` configuration variable. The files need to be named `fullchain.pem` and `privkey.pem`.

The webserver in the container expects TLS certificates to be in a particular order and format. Make sure that your `fullchain.pem` file contains certificates in this order: `<certificate> <intermediate ca> <root ca>`, with PEM encoding.

- Set `DISABLE_HTTPS=false`
- Set `ENABLE_LETSENCRYPT=true`
- Set `SERVER_NAME` with a correct value
- Uncomment the line `- /etc/letsencrypt:/ssl` in the `volumes:` part of the yml config file

## Option D: HTTPS mode with self-signed certificate

:::warning
Only use this for testing purposes!
:::

The container can generate its own self-signed certificate. This certificate will not be trusted and users will see a warning that they'll need to ignore. Do not use this option.

- Set `DISABLE_HTTPS=false`.
- Set `ENABLE_LETSENCRYPT=false`.

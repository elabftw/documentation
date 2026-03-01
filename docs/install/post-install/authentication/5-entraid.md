---
sidebar_position: 5
title: Microsoft Entra ID
---

# Entra ID configuration

Microsoft's Entra ID can be used with eLabFTW. We can configure SAML authentication with it.

Note: this documentation is very much a work-in-progress. Contributions would be welcome.

## Entra ID panel

### Create application

The first step is to **Register an application**.

Set the name to eLabFTW or whatever you prefer.

Select supported account types and for the Redirect URI, add your eLabFTW FQDN followed by: `/index.php?acs`.

This should give you an App ID (UUIDv4).

### Setup SSO

From the SAML-based Sign-on panel register:

* Identifier (Entity ID): https://elabftw.example.com
* Reply URL: https://elabftw.example.com/index.php?acs


### Add users

Add users to the application so they can use it.

## eLabFTW configuration

Get the XML URL of the application from Entra ID, it should look like:

`https://login.microsoftonline.com/<uuid>/federationmetadata/2007-06/federationmetadata.xml?appid=<appid-uuid>`

In eLabFTW, on the Sysconfig Panel, in SAML, add that URL and click Refresh to create the IdP.

Configure the attributes like this:

* Email: http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name
* Firstname: http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname
* Lastname: http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name

Interesting Settings
====================

SLUMBER_USERNAME
----------------

Default: `test`

The username to use when connecting to the Read the Docs API. Used for hitting the API while building the docs.

SLUMBER_PASSWORD
----------------

Default: `test`

The password to use when connecting to the Read the Docs API. Used for hitting the API while building the docs.

USE_SUBDOMAIN
---------------

Default: `False`

Whether to use subdomains in URLs on the site, or the Django-served content.
When used in production, this should be ``True``, as Nginx will serve this content.
During development and other possible deployments, this might be ``False``.

PRODUCTION_DOMAIN
------------------

Default: `readthedocs.org`

This is the domain that gets linked to throughout the site when used in production.
It depends on `USE_SUBDOMAIN`, otherwise it isn't used.

MULTIPLE_APP_SERVERS
--------------------

Default: `undefined`

This is a list of application servers that built documentation is copied to. This allows you to run an independent build server, and then have it rsync your built documentation across multiple front end documentation/app servers.

DEFAULT_PRIVACY_LEVEL
---------------------

Default: `public`

What privacy projects default to having. Generally set to `public`. Also acts as a proxy setting for blocking certain historically insecure options, like serving generated artifacts directly from the media server.

INDEX_ONLY_LATEST
-----------------

Default: `False`

In search, only index the `latest` version of a Project. 

DOCUMENT_PYQUERY_PATH
---------------------

Default: `div.document`

The Pyquery path to an HTML element that is the root of your document. 
This is used for making sure we are only searching the main content of a document.

USE_PIP_INSTALL
---------------

Default: `False`

Whether to use `pip install .` or `python setup.py install` when installing packages into the Virtualenv. Default is to use `python setup.py install`.


PUBLIC_DOMAIN
-------------

Default: `settings.PRODUCTION_DOMAIN`

A special domain for serving public documentation.
If set, public docs will be linked here instead of the `PRODUCTION_DOMAIN`.

ALLOW_ADMIN
-----------

Default: `True`

Whether to include `django.contrib.admin` in the URL's.

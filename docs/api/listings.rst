========
Listings
========

API calls for handling listings

Get my listings
~~~~~~~~~~~~~~~

Get my own listings (GET request)::

    https://api.neoplace.io/api/auth/article/mypublished

*HEADERS*

**Authorization** Bearer {{token_access}}

Create a new listing
~~~~~~~~~~~~~~~~~~~~

Create a new listing (POST request)::

    https://api.neoplace.io/api/auth/article/new

*HEADERS*

| **Authorization** Bearer {{token_access}}
| **Content-Type** application/x-www-form-urlencoded

*BODY*

| **title** {{title}}
| **subtitle** {{subtitle}}
| **type** {{category}}
| **description**: {{description}}
| **price**: {{price}}
| **ean**: {{ean}}
| **urlPicture**: {{ipfs_hash1, ipfs_hash2, ...}}
| **latitude**: {{latitude}}
| **longitude** {{longitude}}
| **currency** {{currency}}
| **brand** {{brand}}
| **model** {{model}}
| **condition** {{condition}}
| **tags** {{tag1, tag2, tag3, ...}}
| **status** {{status}}

Update a listing
~~~~~~~~~~~~~~~~~~~~

Update a listing (POST request)::

    https://api.neoplace.io/api/auth/article/update

*HEADERS*

| **Authorization** Bearer {{token_access}}
| **Content-Type** application/x-www-form-urlencoded

*BODY*

| **title** {{title}}
| **subtitle** {{subtitle}}
| **type** {{category}}
| **description**: {{description}}
| **price**: {{price}}
| **ean**: {{ean}}
| **urlPicture**: {{ipfs_hash1, ipfs_hash2, ...}}
| **latitude**: {{latitude}}
| **longitude** {{longitude}}
| **currency** {{currency}}
| **brand** {{brand}}
| **model** {{model}}
| **condition** {{condition}}
| **tags** {{tag1, tag2, tag3, ...}}
| **status** {{status}}
| **id** {{article_id}}



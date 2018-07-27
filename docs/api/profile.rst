=======
Profile
=======

API calls for handling your profile.

Get my profile
~~~~~~~~~~~~~~

Get my profile::

    https://api.neoplace.io/api/auth/user/content

*HEADERS*

**Authorization** Bearer {{token_access}}

Update my profile
~~~~~~~~~~~~~~~~~

Get my profile::

    https://api.neoplace.io/api/auth/user/profil/update

*HEADERS*

| **Authorization** Bearer {{token_access}}
| **Content-Type** application/x-www-form-urlencoded

*BODY*

| **username** {{username}}
| **firstname** {{firstname}}
| **lastname** {{lastname}}
| **title** {{title}}
| **description** {{description}}
| **cryptoMethod** {{cryptomethod(ETH)}}
| **currencyMethod** {{currencymethoed(USD)}}
| **telegram** {{telegram_username}}
| **address** {{my_address}}
| **pictureProfilUrl** {{ipfs_hash}}~

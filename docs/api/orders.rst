======
Orders
======

API calls for handling orders.

Get my sales
~~~~~~~~~~~~

Get my sales::

    https://api.neoplace.io/api/auth/article/mysales

*HEADERS*

**Authorization** Bearer {{token_access}}

Get my purchases
~~~~~~~~~~~~~~~~

Get my purchases::

    https://api.neoplace.io/api/auth/article/mypurchases

*HEADERS*

**Authorization** Bearer {{token_access}}

Buy an item
~~~~~~~~~~~~

Buy an item (use our NeoPlace library to interact with our smart contract and generate the transaction hash)::

    https://api.neoplace.io/api/auth/article/buy

*HEADERS*

| **Authorization** Bearer {{token_access}}
| **Content-Type** application/x-www-form-urlencoded

*BODY*

| **articleid** {{item_id}}
| **name** {{buyer_name}}
| **address** {{shipping_address}}
| **tx** {{ethereum_transaction_hash}}

Dispatch an item
~~~~~~~~~~~~~~~~~

Inform and update the status order that the item has been dispatched::

    https://api.neoplace.io/api/auth/article/send

*HEADERS*

| **Authorization** Bearer {{token_access}}
| **Content-Type** application/x-www-form-urlencoded

*BODY*

| **articleid** {{item_id}}

Confirm reception
~~~~~~~~~~~~~~~~~

Confirm the reception order and unlock funds to the seller (use our NeoPlace library to interact with our smart contract and generate the transaction hash)::

    https://api.neoplace.io/api/auth/article/receive

*HEADERS*

| **Authorization** Bearer {{token_access}}
| **Content-Type** application/x-www-form-urlencoded

*BODY*

| **articleid** {{item_id}}
| **tx** {{ethereum_transaction_hash}}~

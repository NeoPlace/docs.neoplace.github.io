==============
Authentication
==============

Identification
~~~~~~~~~~~~~~
To start using the API, you need first to get a token.

To get a token, we are not using traditional email/password registration processes, we use a new authentication method: a cryptographically-secure login flow using the MetaMask extension or web3 library.
The basic idea is that it’s cryptographically easy to prove the ownership of an account by signing a piece of data using a private key.

First you need to get a `nonce` for your ethereum address::

    https://api.neoplace.io/subscribe/address?publicAddress={{ethereum_address}}

Response::

    {
        "publicAddress":"{{ethereum_address}}",
        "nonce":"xxxxxxxx"
    }

Sign the message
~~~~~~~~~~~~~~~~
Once you receive the `nonce` in the response from the API call above, sign the message with your private key by running the following code::

    web3.personal.sign(nonce, web3.eth.coinbase, callback);

Obtain authentication token
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Once you signed the message with your private key, make another API call with with both ethereum address and signature (curl method or equivalent)::

    curl --request POST \
        --url 'https://api.neoplace.io/login' \
        --data '{
            "pubKey": "{{ethereum_address}}",
            "signature": "{{signed_message}}"
        }'

The authentication API verifies that your signed message complies with your public address, if it successes, your will receive your authentication in the Response headers::

    Authorization: Bearer {{token_generated}}

Then the token needs to be included in the request header following RFC 2617::

    Authorization: Bearer {{token_generated}}


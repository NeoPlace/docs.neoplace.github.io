=========
Inventory
=========

API calls for handling inventory

Get all inventory
~~~~~~~~~~~~~~~~~

Get a list of all published articles (GET request)::

    https://api.neoplace.io/api/article/published

Get inventory by category
~~~~~~~~~~~~~~~~~~~~~~~~~

Get a list of published articles of a category.

1st level category (GET request)::

    https://api.neoplace.io/api/article/published/{{category_level1}}

2nd level category (GET request)::

    https://api.neoplace.io/api/article/published/{{category_level1}}/{{category_level2}}

Get main categories
~~~~~~~~~~~~~~~~~~~~

Get a list of main categories (GET request)::

    https://api.neoplace.io/api/article/categories/parent

Get all categories
~~~~~~~~~~~~~~~~~~

Get a list of all categories (GET request)::

    https://api.neoplace.io/api/article/categories

Get article details
~~~~~~~~~~~~~~~~~~~

Get article details (GET request)::

    https://api.neoplace.io/api/article/{{id}}

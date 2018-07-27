=========
Inventory
=========

API calls for handling inventory

Get all inventory
~~~~~~~~~~~~~~~~~

Get a list of all published articles::

    https://api.neoplace.io/api/article/published

Get inventory by category
~~~~~~~~~~~~~~~~~~~~~~~~~

Get a list of published articles of a category.

1st level category::

    https://api.neoplace.io/api/article/published/{{category_level1}}

2nd level category::

    https://api.neoplace.io/api/article/published/{{category_level1}}/{{category_level2}}

Get main categories
~~~~~~~~~~~~~~~~~~~~

Get a list of main categories::

    https://api.neoplace.io/api/article/categories/parent

Get all categories
~~~~~~~~~~~~~~~~~~

Get a list of all categories::

    https://api.neoplace.io/api/article/categories

Get article details
~~~~~~~~~~~~~~~~~~~

Get article details::

    https://api.neoplace.io/api/article/{{id}}

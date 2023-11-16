Lookup
================================

https://github.com/theonetruenerd/VenusPackages/blob/main/Lookup.pkg

The lookup library provides one function which allows you to locate items in an array and get their index.

- :ven:func:`Lookup`

.. ven:function:: Lookup(array array, variable item)

  Input an array and a value to look up. If the value occurs in the array, it will return the 1-based index. If it doesn't occur in the array, it will return a 0. 

  :params array: The array to search
  :params item: The variable to search for
  :type array: Array
  :type item: Variable
  :return: 1-based index if found, 0 if not found
  :rtype: Variable


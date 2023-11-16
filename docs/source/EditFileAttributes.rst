EditFileAttributes
===============================

https://github.com/theonetruenerd/VenusPackages/blob/main/EditFileAttributes.pkg

The Edit File Attributes library adds the following functions: 

- :ven:func:`Make_Hidden`
- :ven:func:`Make_ReadOnly`
- :ven:func:`Remove_Hidden`
- :ven:func:`Remove_ReadOnly`

.. ven:function:: Make_Hidden(variable Filename)

  Applies the hidden attribute to the file found at the path specified.

  :params filename: The path to the file that is going to be modified.
  :type filename: Variable
  :return: None
  :rtype: N/A

.. ven:function:: Make_ReadOnly(variable Filename)

  Applies the read only attribute to the file found at the path specified.

  :params filename: The path to the file that is going to be modified.
  :type filename: Variable
  :return: None
  :rtype: N/A

.. ven:function:: Remove_Hidden(variable Filename)

  Removes the hidden attribute from the file found at the path specified.

  :params filename: The path to the file that is going to be modified.
  :type filename: Variable
  :return: None
  :rtype: N/A

.. ven:function:: Remove_ReadOnly(variable Filename)

  Removes the read only attribute from the file found at the path specified.

  :params filename: The path to the file that is going to be modified.
  :type filename: Variable
  :return: None
  :rtype: N/A

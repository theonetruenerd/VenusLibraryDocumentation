EditFileAttributes
===============================

The Edit File Attributes library adds the following functions: 

- :py:func:`Make_Hidden`
- :py:func:`Make_ReadOnly`
- :py:func:`Remove_Hidden`
- :py:func:`Remove_ReadOnly`

.. py:function:: Make_Hidden(variable Filename)

  Applies the hidden attribute to the file found at the path specified.

  :params filename: The path to the file that is going to be modified.
  :type filename: Variable
  :return: None
  :rtype: N/A

.. py:function:: Make_ReadOnly(variable Filename)

  Applies the read only attribute to the file found at the path specified.

  :params filename: The path to the file that is going to be modified.
  :type filename: Variable
  :return: None
  :rtype: N/A

.. py:function:: Remove_Hidden(variable Filename)

  Removes the hidden attribute from the file found at the path specified.

  :params filename: The path to the file that is going to be modified.
  :type filename: Variable
  :return: None
  :rtype: N/A

.. py:function:: Remove_ReadOnly(variable Filename)

  Removes the read only attribute from the file found at the path specified.

  :params filename: The path to the file that is going to be modified.
  :type filename: Variable
  :return: None
  :rtype: N/A

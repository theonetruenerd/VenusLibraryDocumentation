Windows (from HSLExtensions)
=========================================

https://github.com/theonetruenerd/VenusPackages/blob/main/Windows.pkg

The windows library from HSLExtensions adds functions related to registries and special directories. The functions it adds are as follows:

- :py:func:`GetRegistryValue`
- :py:func:`GetSpecialDirectory`
- :py:func:`SetRegistryValue`

.. py:function:: GetRegistryValue(variable i_intHKey, variable i_strKey, variable i_strValueName, variable o_varValue)

  This function reads a value from the specified registry

  :params i_intHKey: The main key of the registry. 1 = ClassesRoot, 2 = CurrentUser, 3 = LocalMachine, 4 = Users, 5 = CurrentConfig.
  :params i_strKey: The key to the path (e.g. SOFTWARE\Phoenix\Directories\Methods)
  :params i_strValueName: The name of the value to be read
  :params o_varValue: The value which was read (type according to value type)
  :type i_intHKey: Integer
  :type i_strKey: String
  :type i_strValueName: String
  :type o_varValue: Variable
  :return: Boolean showing whether the key exists (hslTrue) or not (hslFalse)
  :rtype: Boolean

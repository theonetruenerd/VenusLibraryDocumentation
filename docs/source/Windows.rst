Windows (from HSLExtensions)
=========================================

https://github.com/theonetruenerd/VenusPackages/blob/main/Windows.pkg

The windows library from HSLExtensions adds functions related to registries and special directories. The functions it adds are as follows:

- :ven:func:`GetRegistryValue`
- :ven:func:`GetSpecialDirectory`
- :ven:func:`SetRegistryValue`

.. ven:function:: GetRegistryValue(variable i_intHKey, variable i_strKey, variable i_strValueName, variable o_varValue)

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

.. ven:function:: GetSpecialDirectory(variable i_intSpecialDirectory)

  This function gets the specified special directory

  :params i_intSpecialDirectory: The type of the special directory. 1 = WindowsDirectory, 2 = SystemDirectory, 3 = TemporaryDirectory.
  :type i_intSpecialDirectory: Integer
  :return: The special directory
  :rtype: String

.. ven:function:: SetRegistryValue(variable i_intHKey, variable i_strKey, variable i_strValueName, variable i_varValue, variable i_intValueType)

  This function writes a value to the specified registry

  :params i_intHKey: The main key of the registry. 1 = ClassesRoot, 2 = CurrentUser, 3 = LocalMachine, 4 = Users, 5 = CurrentConfig.
  :params i_strKey: The key to the path (e.g. SOFTWARE\Phoenix\Directories\Methods)
  :params i_strValueName: The name of the value to be read
  :params i_varValue: The value which was will be written in
  :params i_intValueType: The type of the value. 1 = String, 2 = Number, 3 = Binary, 4 = ExpandableString
  :type i_intHKey: Integer
  :type i_strKey: String
  :type i_strValueName: String
  :type o_varValue: Variable
  :return: Boolean showing whether the function was successful (hslTrue) or not (hslFalse)
  :rtype: Boolean

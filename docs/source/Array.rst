Array (from HSLExtensions)
=========================

The array library from HSLExtensions adds functions to help manipulate 1-D arrays. The following functions are added:

- :py:func:`Append`
- :py:func:`CompareArrays`
- :py:func:`Concat`
- :py:func:`ContainsDuplicates`
- :py:func:`ContainsValue`
- :py:func:`ConvertToBooleanArray`
- :py:func:`ConvertToFloatArray`
- :py:func:`ConvertToIntegerArray`
- :py:func:`ConvertToStringArray`
- :py:func:`Copy`
- :py:func:`FindValue`
- :py:func:`InitializeAllValues`
- :py:func:`IsBooleanArray`
- :py:func:`IsEmpty`
- :py:func:`IsFloatArray`
- :py:func:`IsIntegerArray`
- :py:func:`IsStringArray
- :py:func:`Sort`

.. py:function:: Append(array io_arrValuesA, array i_arrValuesB)

  This function updates the array io_arrValuesA to add all the values from i_arrValuesB at the end of the array.

  :params io_arrValuesA: The array to which the values will be added 
  :params i_arrValuesB: The array from which the values will be added
  :type io_arrValuesA: Array
  :type i_arrValuesB: Array
  :return: None
  :rtype: N/A

.. py:function:: CompareArrays(array i_arrExpectedValues, array i_arrActualValues, array o_arrMissingValues, array o_arrNotExpectedValues)

  This function compares two arrays and outputs arrays of values which are missing from the first array but present in the second, and values which are present in the second array but not in the first.

  :params i_arrExpectedValues: The first array, which the second array will be checked against, usually is the array of expected values
  :params i_arrActualValues: The second array, which will use the first array as a template when comparing against, usually is your "actual" array
  :params o_arrMissingValues: An output array of values which are present in the first array but not the second 
  :params o_arrNotExpectedValues: An output array of values which are present in the second array but not the first (i.e. unexpected values in your actual data)
  :type i_arrExpectedValues: Array
  :type i_arrActualValues: Array
  :type o_arrMissingValues: Array
  :type o_arrNotExpectedValues: Array
  :return: True if both arrays contain the same values (resulting in empty output arrays), false if arrays don't contain the same values (in which case the output arrays will have data in them)
  :rtype: Boolean

.. py:function:: Concat(array i_arrValuesA, array i_arrValuesB)

  This function appends one array to the other and then returns the concatenated array. The difference between this and the :py:func:`Append` function is that the Append function updates an existing array, whereas this function doesn't change the existing arrays and instead returns a new array.

  :params i_arrValuesA: The array to which the values will be added
  :params i_arrValuesB: The array from which the values will be added
  :type i_arrValuesA: Array
  :type i_arrValuesB: Array
  :return: A new array which is the concatenated version of the input arrays
  :rtype: Array

.. py:function:: ContainsDuplicates(array i_arrValues)

  This function checks whether the input array has multiple of the same value in it

  :params i_arrValues: The array to be checked
  :type i_arrValues: Array
  :return: An array with all values which appear more than once in the input array
  :rtype: Array

.. py:function:: ContainsValue(array i_arrValues, variable i_varValue)

  This function determines whether a value exists in an array without returning its index

  :params i_arrValues: The array to be searched
  :params i_varValue: The value to be searched for
  :type i_arrValues: Array
  :type i_varValue: Variable
  :return: True if the value is present, false otherwise
  :rtype: Boolean

.. py:function:: ConvertToBooleanArray(i_arrValues, o_blnSuccessfullyConverted)

  This function converts the input array to an array with boolean values. If it is not possible to convert one or more values of the input array, the output will be false and the output array will be empty

  :params i_arrValues: The array to be converted
  :params o_blnSuccessfullyConverted: A boolean which tells you whether the conversion was successful or not
  :type i_arrValues: Array
  :type o_blnSuccessfullyConverted: Boolean
  :return: The boolean version of the input array
  :rtype: Boolean

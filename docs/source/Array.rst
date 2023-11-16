Array (from HSLExtensions)
=========================

https://github.com/theonetruenerd/VenusPackages/blob/main/Array.pkg

The array library from HSLExtensions adds functions to help manipulate 1-D arrays. The following functions are added:

- :ven:func:`Append`
- :ven:func:`CompareArrays`
- :ven:func:`Concat`
- :ven:func:`ContainsDuplicates`
- :ven:func:`ContainsValue`
- :ven:func:`ConvertToBooleanArray`
- :ven:func:`ConvertToFloatArray`
- :ven:func:`ConvertToIntegerArray`
- :ven:func:`ConvertToStringArray`
- :ven:func:`Copy`
- :ven:func:`FindValue`
- :ven:func:`InitializeAllValues`
- :ven:func:`IsBooleanArray`
- :ven:func:`IsEmpty`
- :ven:func:`IsFloatArray`
- :ven:func:`IsIntegerArray`
- :ven:func:`IsStringArray`
- :ven:func:`Sort`

.. ven:function:: Append(array io_arrValuesA, array i_arrValuesB)

  This function updates the array io_arrValuesA to add all the values from i_arrValuesB at the end of the array.

  :params io_arrValuesA: The array to which the values will be added 
  :params i_arrValuesB: The array from which the values will be added
  :type io_arrValuesA: Array
  :type i_arrValuesB: Array
  :return: None
  :rtype: N/A

.. ven:function:: CompareArrays(array i_arrExpectedValues, array i_arrActualValues, array o_arrMissingValues, array o_arrNotExpectedValues)

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

.. ven:function:: Concat(array i_arrValuesA, array i_arrValuesB)

  This function appends one array to the other and then returns the concatenated array. The difference between this and the :ven:func:`Append` function is that the Append function updates an existing array, whereas this function doesn't change the existing arrays and instead returns a new array.

  :params i_arrValuesA: The array to which the values will be added
  :params i_arrValuesB: The array from which the values will be added
  :type i_arrValuesA: Array
  :type i_arrValuesB: Array
  :return: A new array which is the concatenated version of the input arrays
  :rtype: Array

.. ven:function:: ContainsDuplicates(array i_arrValues)

  This function checks whether the input array has multiple of the same value in it

  :params i_arrValues: The array to be checked
  :type i_arrValues: Array
  :return: An array with all values which appear more than once in the input array
  :rtype: Array

.. ven:function:: ContainsValue(array i_arrValues, variable i_varValue)

  This function determines whether a value exists in an array without returning its index

  :params i_arrValues: The array to be searched
  :params i_varValue: The value to be searched for
  :type i_arrValues: Array
  :type i_varValue: Variable
  :return: True if the value is present, false otherwise
  :rtype: Boolean

.. ven:function:: ConvertToBooleanArray(array i_arrValues, variable o_blnSuccessfullyConverted)

  This function converts the input array to an array with boolean values. If it is not possible to convert one or more values of the input array, the output will be false and the output array will be empty. Cannot interact with strings, will convert a non-zero int or float into a 1, and will turn a 0 float into a 0.

  :params i_arrValues: The array to be converted
  :params o_blnSuccessfullyConverted: A boolean which tells you whether the conversion was successful or not
  :type i_arrValues: Array
  :type o_blnSuccessfullyConverted: Boolean
  :return: The boolean version of the input array
  :rtype: Array

.. ven:function:: ConvertToFloatArray(array i_arrValues, variable o_blnSuccessfullyConverted)

  This function converts the input array to an array with float values. If it is not possible to convert one or more values of the input array, the output will be false and the output array will be empty. Cannot interact with strings, will convert any int into a float. 

  :params i_arrValues: The array to be converted
  :params o_blnSuccessfullyConverted: A boolean which tells you whether the conversion was successful or not
  :type i_arrValues: Array
  :type o_blnSuccessfullyConverted: Boolean
  :return: The float version of the input array
  :rtype: Array

.. ven:function:: ConvertToIntArray(array i_arrValues, variable o_blnSuccessfullyConverted)

  This function converts the input array to one with integer values. If it is not possible to convert one or more values of the input array, the output will be false and the output array will be empty. Cannot interact with strings, will round any floats to the nearest integer.

  :params i_arrValues: The array to be converted
  :params o_blnSuccessfullyConverted: A boolean which tells you whether the conversion was successful or not
  :type i_arrValues: Array
  :type o_blnSuccessfullyConverted: Boolean
  :return: The integer version of the input array
  :rtype: Array

.. ven:function:: ConvertToStringArray(array i_arrValues)

  This function converts the input array to one with string values. 

  :params i_arrValues: The array to be converted
  :type i_arrValues: Array
  :return: The float version of the input array
  :rtype: Array

.. ven:function:: Copy(array i_arrValues)

  This function will output an exact copy of the input array. 

  :params i_arrValues: The array to be copied
  :type i_arrValues: Array
  :return: A copy of the input array
  :rtype: Array

.. ven:function:: FindValue(array i_arrValues, variable i_varValue)

  This function will lookup the input variable within the input array and return a 1-based array of the indices of all positions that the input variable was found.

  :params i_arrValues: The array to be searched
  :params i_varValue: The variable to be searched for
  :type i_arrValues: Array
  :type i_varValue: Variable
  :return: An array of all the locations that the input variable was found
  :rtype: Array

.. ven:function:: InitializeAllValues(array io_arrValues, variable i_varValue)

  This function sets all values within an array to the input variable. Does not work on empty arrays. 

  :params io_arrValues: The array in which all values will be converted. 
  :params i_varValue: The variable to which all values will be converted.
  :type io_arrValues: Array
  :type i_varValue: Variable
  :return: None
  :rtype: N/A

.. ven:function:: IsBooleanArray(array i_arrValues)

  This function checks whether all values in the array are booleans.

  :params i_arrValues: The array to be checked
  :type i_arrValues: Array
  :return: A boolean of whether the input array is all booleans or not
  :rtype: Boolean

.. ven:function:: IsEmpty(array i_arrValues)

  This function checks whether the input array is empty

  :params i_arrValues: The array to be checked
  :type i_arrValues: Array
  :return: A boolean of whether the input array is empty or not
  :rtype: Boolean

.. ven:function:: IsFloatArray(array i_arrValues)

  This function checks whether all values in the array are floats.

  :params i_arrValues: The array to be checked
  :type i_arrValues: Array
  :return: A boolean of whether the input array is all floats or not
  :rtype: Boolean

.. ven:function:: IsIntegerArray(array i_arrValues)

  This function checks whether all values in the array are integers.

  :params i_arrValues: The array to be checked
  :type i_arrValues: Array
  :return: A boolean of whether the input array is all integers or not
  :rtype: Boolean

.. ven:function:: IsStringArray(array i_arrValues)

  This function checks whether all values in the array are strings.

  :params i_arrValues: The array to be checked
  :type i_arrValues: Array
  :return: A boolean of whether the input array is all strings or not
  :rtype: Boolean

.. ven:function:: Sort(array i_arrValues, variable i_intSortMode, o_bSuccessfulSorted)

  This function outputs a sorted version of the array using the Shakersort sorting algorithm. All values in the array must share the same type for this function to work. Sort mode can either be 1 or 2, 1 is ascending and 2 is descending. 

  :params i_arrValues: The array containing the values to be sorted  
  :params i_intSortMode: Whether the array is to be sorted in ascending (1) or descending (2) order
  :params o_bSuccesfulSorted: A boolean of whether the sort was successful or not
  :type i_arrValues: Array
  :type i_intSortMode: Variable
  :type o_bSuccesfulSorted: Boolean
  :return: A sorted copy of the array
  :rtype: Array

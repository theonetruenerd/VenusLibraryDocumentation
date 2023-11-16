String (from HSLExtensions)
===================================

https://github.com/theonetruenerd/VenusPackages/blob/main/String.pkg

The String library from HSLExtensions adds a few functions to facilitate easier manipulation of strings. It adds the following functions:

  - :ven:func:`ConvertToAsciiArray`
  - :ven:func:`ConvertToCharArray`
  - :ven:func:`FromAsciiArray`
  - :ven:func:`Join`
  - :ven:func:`JoinWithDelimiter`
  - :ven:func:`Split`
  - :ven:func:`Trim`

.. ven:function:: ConvertToAsciiArray(variable i_strValue)

  This function converts the input string into an array with the regarding ASCII codes. If the input parameter is not a string the function returns an empty array.

  :params i_strValue: The input string to be converted into an array
  :type i_strValue: Variable
  :return: An array of ASCII codes, or an empty array if the input parameter is not a string
  :rtype: Array

.. ven:function:: ConvertToCharArray(variable i_strValue)

  This function converts the input string into an array with the regarding characters. If the input parameter is not a string the function returns an empty array.

  :params i_strValue: The input string to be converted into an array
  :type i_strValue: Variable
  :return: An array of characters (strings with length 1), or an empty array if the input parameter is not a string
  :rtype: Array

.. ven:function:: FromAsciiArray(array i_arrAsciiValues)

  This function converts an input array with ASCII codes into a string. If the input parameter is not an array with ASCII codes, the function returns an empty string.

  :params i_arrAsciiValues: The input array of ASCII codes to be converted into a string
  :type i_arrAsciiValues: Array
  :return: The output string formed by the concatenation of the converted versions of the ASCII codes. An empty string if the input parameter is not an array with ASCII codes.
  :rtype: Variable

.. ven:function:: Join(array i_arrValues)

  This function joins an array of strings into a single string. Can be used to concatenate any number of strings into a single one. If the input parameter is not an array with strings, the function returns an empty string.

  :params i_arrValues: The array of strings to be concatenated
  :type i_arrValues: Array
  :return: The concatenated form of all the strings in the array, or an empty string if the input parameter is not an array of strings
  :rtype: Variable

.. ven:function:: JoinWithDelimiter(array i_arrValues, variable i_strDelimiter)

  This function joins an array of strings into a single string and adds a delimiter between each substring. If the input parameter is not an array with strings, the function returns an empty string.

  :params i_arrValues: The input array of strings to be concatenated
  :params i_strDelimiter: The delimiter to be inserted between each substring
  :type i_arrValues: Array
  :type i_strDelimiter: Variable
  :return: The concatenated strings from the array, with delimiters between each substring. An empty string if the input parameter is not an array of strings.
  :rtype: Variable

.. ven:function:: Split(variable i_strValue, variable i_strDelimiter, variable i_bTrimWhitespaces)

  This function splits a string into substrings, forming an array of strings. The input string is split based on a delimiter that the user inputs. 

  :params i_strValue: The input string to be split into substrings
  :params i_strDelimiter: The delimiter to be used to split the string
  :params i_bTrimWhitespaces: Boolean determining whether leading and trailing whitespaces will be removed or not
  :type i_strValue: Variable
  :type i_strDelimiter: Variable
  :type i_bTrimWhitespaces: Boolean
  :return: An array of strings containing each substring formed from splitting the original string
  :rtype: Array

.. ven:function:: Trim(variable i_strValue)

  This function trims leading and trailing whitespace characters from the input string. If the input parameter is not a string the function returns an empty string.

  :params i_strValue: The input string to trim
  :type i_strValue: Variable
  :return: The trimmed string
  :rtype: Variable

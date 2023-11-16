HSLStrLib
==========================================

https://github.com/theonetruenerd/VenusPackages/blob/main/HSLStrLib.pkg

HSL String Library provides the following functions: 

- :ven:func:`StrAsciiToStr`
- :ven:func:`StrConcat2`
- :ven:func:`StrConcat4`
- :ven:func:`StrConcat8`
- :ven:func:`StrConcat12`
- :ven:func:`StrEvaluateExpr`
- :ven:func:`StrFillLeft`
- :ven:func:`StrFillRight`
- :ven:func:`StrFind`
- :ven:func:`StrFStr`
- :ven:func:`StrFStrEx`
- :ven:func:`StrFVal`
- :ven:func:`StrGetLength`
- :ven:func:`StrGetType`
- :ven:func:`StrHexIStr`
- :ven:func:`StrIsDigit`
- :ven:func:`StrIStr`
- :ven:func:`StrIVal`
- :ven:func:`StrLeft`
- :ven:func:`StrMakeLower`
- :ven:func:`StrMakeLowerCopy`
- :ven:func:`StrMakeUpper`
- :ven:func:`StrMakeUpperCopy`
- :ven:func:`StrMid`
- :ven:func:`StrReplace`
- :ven:func:`StrReverseFind`
- :ven:func:`StrRight`
- :ven:func:`StrSpanExcluding`
- :ven:func:`StrStrToAscii`
- :ven:func:`StrTrimLeft`
- :ven:func:`StrTrimRight`

..  ven:function:: StrAsciiToStr(variable asciiCode)

    Converts the given ASCII Code (an integer) to a character (string).

    :param asciiCode: The ASCII code to convert
    :type asciiCode: Integer
    :return: The ASCII code as a string
    :rtype: String

.. ven:function:: StrConcat2(variable Var1, variable Var2)

    Combines two strings into a new string

    :param Var1: The first string to be combined
    :param Var2: The second string to be combined
    :type Var1: String
    :type Var2: String
    :return: The combined string of Var1 + Var2
    :rtype: String

.. ven:function:: StrConcat4(variable Var1, variable Var2, variable Var3, variable Var4)

    Combines four strings into a new string

    :param Var1: The first string to be combined
    :param Var2: The second string to be combined
    :param Var3: The third string to be combined
    :param Var4: The fourth string to be combined
    :type Var1: String
    :type Var2: String
    :type Var3: String
    :type Var4: String
    :return: The combined string of Var1 + Var2 + Var3 + Var4
    :rtype: String

.. ven:function:: StrConcat8(variable Var1, variable Var2, variable Var3, variable Var4, variable Var5, variable Var6, variable Var7, variable Var8)

    Combines eight strings into a new string

    :param Var1: The first string to be combined
    :param Var2: The second string to be combined
    :param Var3: The third string to be combined
    :param Var4: The fourth string to be combined
    :param Var5: The fifth string to be combined
    :param Var6: The sixth string to be combined
    :param Var7: The seventh string to be combined
    :param Var8: The eighth string to be combined
    :type Var1: Variable
    :type Var2: Variable
    :type Var3: Variable
    :type Var4: Variable
    :type Var5: Variable
    :type Var6: Variable
    :type Var7: Variable
    :type Var8: Variable
    :return: The combined string of Var1 + Var2 + Var3 + Var4 + Var5 + Var6 + Var7 + Var8
    :rtype: String

.. ven:function:: StrConcat12(variable Var1, variable Var2, variable Var3, variable Var4, variable Var5, variable Var6, variable Var7, variable Var8, variable Var9, variable var10, variable var11, variable var12)

    Combines twelve strings into a new string

    :param Var1: The first string to be combined
    :param Var2: The second string to be combined
    :param Var3: The third string to be combined
    :param Var4: The fourth string to be combined
    :param Var5: The fifth string to be combined
    :param Var6: The sixth string to be combined
    :param Var7: The seventh string to be combined
    :param Var8: The eighth string to be combined
    :param Var9: The ninth string to be combined
    :param Var10: The tenth string to be combined
    :param Var11: The eleventh string to be combined
    :param Var12: The twelfth string to be combined
    :type Var1: Variable
    :type Var2: Variable
    :type Var3: Variable
    :type Var4: Variable
    :type Var5: Variable
    :type Var6: Variable
    :type Var7: Variable
    :type Var8: Variable
    :type Var9: Variable
    :type Var10: Variable
    :type Var11: Variable
    :type Var12: Variable
    :return: The combined string of Var1 + Var2 + Var3 + Var4 + Var5 + Var6 + Var7 + Var8 + Var9 + Var10 + Var11 + Var12
    :rtype: Variable

.. ven:function:: StrEvaluateExpr(variable expression)

    This function evaluates an expression within a string. All variables involved must have global scope. 

    :params expression: The expression to evaluate as a string
    :type expression: Variable
    :return: The value of the expression if the function succeeds, otherwise a runtime error
    :rtype: Variable

.. ven:function:: StrFillLeft(variable str, variable character, variable width)

    This function fills leading characters to the string

    :params str: The string to be modified
    :params character: The user-defined character to be filled
    :params width: The width to be filled
    :type str: Variable
    :type character: Variable
    :type width: Integer
    :return: The modified string
    :rtype: Variable

.. ven:function:: StrFillRight(variable str, variable character, variable width)

    This function fills trailing characters to the string

    :params str: The string to be modified
    :params character: The user-defined character to be filled
    :params width: The width to be filled
    :type str: Variable
    :type character: Variable
    :type width: Integer
    :return: The modified string
    :rtype: Variable

.. ven:function:: StrFind(variable str, variable subStr)

    This function searches the string for the first match of the sub-string.

    :params str: The string to be searched
    :params subStr: The substring to be searched for
    :type str: Variable
    :type subStr: Variable
    :return: The zero-based index of the first character in this string object that matches the requested sub-string or characters. -1 if the sub-string is not found.
    :rtype: Integer

.. ven:function:: StrFStr(variable number)

    This function converts the floating point number input into the corresponding character string. 

    :params number: The float to be converted into a string
    :type number: Float
    :return: The string form of the float
    :rtype: Variable

.. ven:function:: StrFStrEx(variable number, variable languageSpecific, variable precision)

    This function converts the floating point number input into the corresponding character string

    :params number: The float to be converted into a string.
    :params languageSpecific: Boolean which specifies whether the decimal symbol in the Regional Settings should be used to write the string representation of the floating point number.
    :params precision: The total number of significant digits to be used for the floating-point display
    :type number: Float
    :type languageSpecific: Boolean
    :type precision: Integer
    :return: The string representation of the floating point number
    :rtype: Variable

.. ven:function:: StrFVal(variable str)

    Converts the sequence of digits, contained in the character string str, into the corresponding floating point number. Conversion aborts at the first character in str, which is not a digit or not one of the characters +, -, e, E.

    :params str: The string to be converted
    :type str: Variable
    :return: THe float representation of the input string. Null if the string cannot be converted. DBL_MAX if the conversion results in an overflow. DBL_MIN if the conversion results in an underflow. 
    :rtype: Float or variable

.. ven:function:: StrGetLength(variable str)

    Returns the number of characters in a string object (without '\0').

    :params str: The string being read
    :type str: Variable
    :return: The length of the string
    :rtype: Integer

.. ven:function:: StrGetType(variable var)

    This function retrieves the type of the value of a variable

    :params var: A reference to a variable (int, float or string)
    :type var: Variable
    :return: One of the following string-valued constants that indicates the type of the value of a variable. i = hslInteger, f = hslFloat, s = hslString, null = no type
    :rtype: Variable

.. ven:function:: StrHexIStr(variable number)

    Converts the input integer into the corresponding hexadecimal character string

    :params number: The integer to be converted
    :type: Integer
    :return: The hexadecimal string representation of the integer
    :rtype: String

.. ven:function:: StrIsDigit(variable character)

    The StrIsDigit function determines if the specified input string (which should be a character) is a digit or not.

    :params character: The input character to be a tested, as a string
    :type character: Variable
    :return: Boolean showing whether the character is a digit (1) or not (0)
    :rtype: Boolean

.. ven:function:: StrIsStr(variable number)

    The StrIStr function converts the input integer into the corresponding character string

    :params number: The integer to be converted
    :type number: Variable
    :return: The string representation of the integer number
    :rtype: Variable

.. ven:function:: StrIVal(variable str)

    The StrIVal function converts the input sequence of digits into the corresponding integer. The input string is treated as a decimal, unless it begins with an 0x in which case it is interpreted as hexadecimal.            Conversion aborts at the first character in the input which is neither a digit nor one of the characters "+" or "-".

    :params str: The input sequence of digits to be converted
    :type str: Variable
    :return: The numeric value of the sequence of digits contained in the character string, as an integer. Null if the character string cannot be converted into a number. LONG_MAX = 2147483647 if the conversion results in an overflow. LONG_MIN = -2147483647 - 1 if the conversion results in an underflow.
    :rtype: Variable

.. ven:function:: StrLeft(variable str, variable count)

    The StrLeft function extracts the first (leftmost) characters of a string and returns a copy of the extracted substring. The number of characters extracted is equal to the input variable "count". If "count" is longer than the string, the entire string is returned.

    :params str: The input string from which the substring is to be extracted
    :params count: The number of characters to be extracted
    :type str: Variable
    :type count: Variable
    :return: A string containing a copy of the specified range of characters. Can be an empty string.
    :rtype: Variable

.. ven:function:: StrMakeLower(variable str)

    The StrMakeLower function converts the original string to its lowercase form.

    :params str: The string to be converted
    :type str: Variable
    :return: The original string converted to lowercase
    :rtype: Variable

.. ven:function:: StrMakeLowerCopy(variable str)

    The StrMakeLowerCopy function returns a copy of the original string converted to lowercase.

    :params str: The string to be copied
    :type str: Variable
    :return: A copy of the original string converted to lowercase
    :rtype: Variable

.. ven:function:: StrMakeUpper(variable str)

    The StrMakeUpper function converts the original string to its uppercase form.

    :params str: The string to be converted
    :type str: Variable
    :return: The original string converted to uppercase
    :rtype: Variable

.. ven:function:: StrMakeUpperCopy(variable str)

    The StrMakeUpperCopy function returns a copy of the original string converted to uppercase.

    :params str: The string to be copied
    :type str: Variable
    :return: A copy of the original string converted to uppercase
    :rtype: Variable

.. ven:function:: StrMid(variable str, variable first, variable count)

    The StrMid function extracts a substring of length "count" characters from the input variable "str", starting at position "first" which is 0-based. The function returns a copy of the extracted substring.

    :params str: The string from which the substring is to be extracted
    :params first: The first character to be extracted (0-based)
    :params count: The number of characters to be extracted
    :type str: Variable
    :type first: Variable
    :type count: Variable
    :return: A string containing a copy of the specified range of characters, can be empty
    :rtype: Variable

.. ven:function:: StrReplace(variable str, variable oldSubStr, variable newSubStr)

    The StrReplace function searches a string for a specified substring and replaces it with another specified substring.

    :params str: The string to be edited
    :params oldSubStr: The substring to be replaced by newSubStr
    :params newSubStr: The substring to replace oldSubStr
    :type str: Variable
    :type oldSubStr: Variable
    :type newSubStr: Variable
    :return: The number of replaced instances of oldSubStr. Zero if the string is unchanged.
    :rtype: Variable

.. ven:function:: StrReverseFind(variable str, variable subStr)

    The StrReverseFind function searches a string object for the last match of a sub-string

    :params str: The string to be searched
    :params subStr: The substring to be searched for
    :type str: Variable
    :type subStr: Variable
    :return: The zero-based index of the last character in this string that matches the requested substring or characters. -1 if the substring is not found.
    :rtype: Variable

.. ven:function:: StrRight(variable str, variable count)

    The StrRight function extracts the last (rightmost) characters of a string and returns a copy of the extracted substring. The number of characters extracted is equal to the input variable "count". If "count" is longer than the string, the entire string is returned.

    :params str: The input string from which the substring is to be extracted
    :params count: The number of characters to be extracted
    :type str: Variable
    :type count: Variable
    :return: A string containing a copy of the specified range of characters. Can be an empty string.
    :rtype: Variable

.. ven:function:: StrSpanExcluding(variable str, variable subStr)

    The StrSpanExcluding function can be used to search the string for the first occurrence of any character in the specified set subStr. StrSpanExcluding extracts and returns all characters preceding the first occurrence of a character from subStr (in other words, the character from subStr and all characters following it in the string, are not returned). If no character from subStr is found in the string, then StrSpanExcluding returns the entire string.

    :params str: The string to be searched
    :params subStr: A string containing the set of characters to be searched for
    :type str: Variable
    :type subStr: Variable
    :return: A sub-string containing characters in the string that are not in subStr, beginning with the first character in the string and ending with the first character found in the string that is also in subStr (that is, starting with the first character in the string and up to but excluding the first character in the string that is found subStr). It returns the entire string if no character in subStr is found in the string.
    :rtype: Variable

.. ven:function:: StrStrToAscii(variable character)

    The StrStrToAscii function converts the given character (as a string) into an ASCII code (as an integer)

    :params character: The character to convert, inputted as a string
    :type character: Variable
    :return: The ASCII code for the given character as an integer, -1 if the function fails
    :rtype: Variable

.. ven:function:: StrTrimLeft(variable str, variable character)

    The StrTrimLeft function trims leading whitespace characters from the string (removes newline, space, tab, and user-defined characters)

    :params str: The string to trim
    :params character: A string containing user-defined characters to be trimmed (may be empty, in which case only newline, space and tabs will be trimmed)
    :type str: Variable
    :type character: Variable
    :return: None
    :rtype: N/A

.. ven:function:: StrTrimRight(variable str, variable character)

    The StrTrimRight function trims lagging whitespace characters from the string (removes newline, space, tab, and user-defined characters)

    :params str: The string to trim
    :params character: A string containing user-defined characters to be trimmed (may be empty, in which case only newline, space and tabs will be trimmed)
    :type str: Variable
    :type character: Variable
    :return: None
    :rtype: N/A

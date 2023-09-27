HSL String Library - unfinished
==========================================

https://github.com/theonetruenerd/VenusPackages/blob/main/HSLStrLib.pkg

HSL String Library provides the following functions: 

- :py:func:`StrAsciiToStr`
- :py:func:`StrConcat2`
- :py:func:`StrConcat4`
- :py:func:`StrConcat8`
- :py:func:`StrConcat12`
- :py:func:`StrEvaluateExpr`
- :py:func:`StrFillLeft`
- :py:func:`StrFillRight`
- :py:func:`StrFind`
- :py:func:`StrFStr`
- :py:func:`StrFStrEx`
- :py:func:`StrFVal`
- :py:func:`StrGetLength`
- :py:func:`StrGetType`
- :py:func:`StrHexIStr`
- :py:func:`StrIsDigit`
- :py:func:`StrIStr`
- :py:func:`StrIVal`
- :py:func:`StrLeft`
- :py:func:`StrMakeLower`
- :py:func:`StrMakeLowerCopy`
- :py:func:`StrMakeUpper`
- :py:func:`StrMakeUpperCopy`
- :py:func:`StrMid`
- :py:func:`StrReplace`
- :py:func:`StrReverseFind`
- :py:func:`StrRight`
- :py:func:`StrSpanExcluding`
- :py:func:`StrStrToAscii`
- :py:func:`StrTrimLeft`
- :py:func:`StrTrimRight`

..  py:function:: StrAsciiToStr(variable asciiCode)

    Converts the given ASCII Code (an integer) to a character (string).

    :param asciiCode: The ASCII code to convert
    :type asciiCode: Integer
    :return: The ASCII code as a string
    :rtype: String

.. py:function:: StrConcat2(variable Var1, variable Var2)

    Combines two strings into a new string

    :param Var1: The first string to be combined
    :param Var2: The second string to be combined
    :type Var1: String
    :type Var2: String
    :return: The combined string of Var1 + Var2
    :rtype: String

.. py:function:: StrConcat4(variable Var1, variable Var2, variable Var3, variable Var4)

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

.. py:function:: StrConcat8(variable Var1, variable Var2, variable Var3, variable Var4, variable Var5, variable Var6, variable Var7, variable Var8)

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

.. py:function:: StrConcat12(variable Var1, variable Var2, variable Var3, variable Var4, variable Var5, variable Var6, variable Var7, variable Var8, variable Var9, variable var10, variable var11, variable var12)

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

.. py:function:: StrEvaluateExpr(variable expression)

    This function evaluates an expression within a string. All variables involved must have global scope. 

    :params expression: The expression to evaluate as a string
    :type expression: Variable
    :return: The value of the expression if the function succeeds, otherwise a runtime error
    :rtype: Variable

.. py:function:: StrFillLeft(variable str, variable character, variable width)

    This function fills leading characters to the string

    :params str: The string to be modified
    :params character: The user-defined character to be filled
    :params width: The width to be filled
    :type str: Variable
    :type character: Variable
    :type width: Integer
    :return: The modified string
    :rtype: Variable

.. py:function:: StrFillRight(variable str, variable character, variable width)

    This function fills trailing characters to the string

    :params str: The string to be modified
    :params character: The user-defined character to be filled
    :params width: The width to be filled
    :type str: Variable
    :type character: Variable
    :type width: Integer
    :return: The modified string
    :rtype: Variable

.. py:function:: StrFind(variable str, variable subStr)

    This function searches the string for the first match of the sub-string.

    :params str: The string to be searched
    :params subStr: The substring to be searched for
    :type str: Variable
    :type subStr: Variable
    :return: The zero-based index of the first character in this string object that matches the requested sub-string or characters. -1 if the sub-string is not found.
    :rtype: Integer

.. py:function:: StrFStr(variable number)

    This function converts the floating point number input into the corresponding character string. 

    :params number: The float to be converted into a string
    :type number: Float
    :return: The string form of the float
    :rtype: Variable

.. py:function:: StrFStrEx(variable number, variable languageSpecific, variable precision)

    This function converts the floating point number input into the corresponding character string

    :params number: The float to be converted into a string.
    :params languageSpecific: Boolean which specifies whether the decimal symbol in the Regional Settings should be used to write the string representation of the floating point number.
    :params precision: The total number of significant digits to be used for the floating-point display
    :type number: Float
    :type languageSpecific: Boolean
    :type precision: Integer
    :return: The string representation of the floating point number
    :rtype: Variable

.. py:function:: StrFVal(variable str)

    Converts the sequence of digits, contained in the character string str, into the corresponding floating point number. Conversion aborts at the first character in str, which is not a digit or not one of the characters +, -, e, E.

    :params str: The string to be converted
    :type str: Variable
    :return: THe float representation of the input string. Null if the string cannot be converted. DBL_MAX if the conversion results in an overflow. DBL_MIN if the conversion results in an underflow. 
    :rtype: Float or variable

.. py:function:: StrGetLength(variable str)

    Returns the number of characters in a string object (without '\0').

    :params str: The string being read
    :type str: Variable
    :return: The length of the string
    :rtype: Integer

.. py:function:: StrGetType(variable var)

    This function retrieves the type of the value of a variable

    :params var: A reference to a variable (int, float or string)
    :type var: Variable
    :return: One of the following string-valued constants that indicates the type of the value of a variable. i = hslInteger, f = hslFloat, s = hslString, null = no type
    :rtype: Variable

.. py:function:: StrHexIStr(variable number)

    Converts the input integer into the corresponding hexadecimal character string

    :params number: The integer to be converted
    :type: Integer
    :return: The hexadecimal string representation of the integer
    :rtype: String

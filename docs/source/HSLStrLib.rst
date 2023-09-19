HSL String Library
==========================================

HSL String Library provides the following functions: 

- :py:func:`StrAsciiToStr`
- StrConcat2
- StrConcat4
- StrConcat8
- StrConcat12
- StrEvaluateExpr
- StrFillLeft
- StrFillRight
- StrFind
- StrFStr
- StrFStrEx
- StrFVal
- StrGetLength
- StrGetType
- StrHexIStr
- StrIsDigit
- StrIStr
- StrIVal
- StrLeft
- StrMakeLower
- StrMakeLowerCopy
- StrMakeUpper
- StrMakeUpperCopy
- StrMid
- StrReplace
- StrReverseFind
- StrRight
- StrSpanExcluding
- StrStrToAscii
- StrTrimLeft
- StrTrimRight

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
    :type Var1: String
    :type Var2: String
    :type Var3: String
    :type Var4: String
    :type Var5: String
    :type Var6: String
    :type Var7: String
    :type Var8: String
    :return: The combined string of Var1 + Var2 + Var3 + Var4 + Var5 + Var6 + Var7 + Var8
    :rtype: String

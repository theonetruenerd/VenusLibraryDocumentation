HSL String Library
==========================================

HSL String Library provides the following functions: 

- StrAsciiToStr
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
